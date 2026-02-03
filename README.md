# 🧠 Pixel Coordinate Regression using Deep Learning

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Deep%20Learning-orange)
![Regression](https://img.shields.io/badge/Task-Supervised%20Regression-green)
![Status](https://img.shields.io/badge/Status-Completed-success)


## 📌 Problem Statement
Given a **50×50 grayscale image** with **exactly one pixel having value 255**, predict the **(x, y) coordinates** of that pixel using **Deep Learning**.


## 🛠️ How I Solved This
- Treated the problem as a **supervised regression task**
- Generated a **synthetic dataset** with controlled pixel positions
- Used a **CNN without pooling layers** to preserve spatial information
- Trained the model to regress normalized `(x, y)` coordinates

## 🧪 Dataset Strategy
- Each image contains:
  - One pixel = `255`
  - All others = `0`
- Pixel position is **randomly and uniformly sampled**
- Images and labels are **normalized** for stable training

## 🧩 Model Architecture
- Convolution layers to detect the bright pixel
- **No pooling layers** (to avoid losing pixel location)
- Flatten + Dense layers for coordinate regression
- Loss function: **Mean Squared Error (MSE)**

## 🚀 Steps Followed
1. Generate synthetic dataset
2. Normalize images and coordinates
3. Build CNN regression model
4. Train with MSE loss
5. Evaluate using **Mean Pixel Error**
6. Visualize predictions vs ground truth

## 📊 Results
- **Mean Pixel Error:** ~`0.21 px`
- **Median Pixel Error:** ~`0.18 px`
- Near-perfect pixel localization on test data

## 📦 Tech Stack
- 🐍 Python  
- 🤖 TensorFlow / Keras  
- 📊 NumPy, Matplotlib, Scikit-learn  

## ✅ Conclusion
This project demonstrates how a **simple and well-designed CNN** can achieve **sub-pixel accuracy** when spatial information is preserved, highlighting the importance of architectural choices over model complexity.
