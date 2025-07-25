# 🧠 Self-Driving Car AI Model

An end-to-end deep learning project that simulates a self-driving car's lane detection and autonomous navigation capability using a CNN-based architecture inspired by NVIDIA's model.

---

## 🚗 Project Overview

This project involves:

- Simulated driving with data collection from three camera angles (center, left, right)
- Preprocessing image data and applying augmentations
- Training three progressively complex CNN models
- Evaluating performance across different circuits
- Addressing overfitting and optimizing training

---

## 📸 Data Collection Strategy

- Used three cameras (center, left, right)
- Collected driving data by manually navigating two circuits
- Maintained moderate speed and avoided abrupt steering
- Reversed driving direction for data diversity
- Slowed near curves, signs, and hills to enrich training samples

---

## 🏗️ Model Architectures

All models were based on NVIDIA’s self-driving architecture and improved progressively:

### 🔹 Model 1
- **Architecture**: Basic CNN + Dropout  
- **Parameters**: 252,219  
- **Size**: 0.97 MB  
- **Outcome**: Underperformed, showed zig-zag behavior and needed retraining

### 🔹 Model 2
- **Architecture**: CNN + BatchNorm + L2 Regularization  
- **Parameters**: 253,011  
- **Size**: 0.97 MB  
- **Outcome**: Improved stability and generalization across Circuit 1

### 🔹 Model 3
- **Architecture**: CNN + BatchNorm + He Initialization + Deeper Dense Layers (512 → 256 → 128)  
- **Parameters**: 888,301  
- **Size**: 3.40 MB  
- **Outcome**: Smoothest loss curve, best training performance, but suffered from overfitting and failed to generalize to Circuit 2

---

## 🔄 Data Augmentation Techniques

To prevent overfitting and improve model robustness, the following augmentations were applied:

- Image Cropping  
- Random Brightness Adjustment  
- Random Shadow Overlays  
- Random Shifting  
- Random Flipping

---

## 🧪 Final Verdict: Best Model

✅ **Model 2 was the best performing model overall.**  
It provided the best balance of:

- Lightweight architecture
- Stability during autonomous driving
- Less overfitting
- Generalization to unseen track conditions

⚠️ While **Model 3** demonstrated stronger learning capacity, it overfit the training data and failed to complete Circuit 2 reliably.  
❌ **Model 1** was unstable and inconsistent in driving behavior.

---

