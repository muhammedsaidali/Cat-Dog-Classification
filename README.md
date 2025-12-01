<h1 align="center">🐱🐶 Cats vs Dogs Classification — CNN, Augmentation & Transfer Learning</h1>

This project explores how different deep-learning approaches perform on a binary image classification task (cats vs dogs) across varying dataset sizes.

The experiments include:

- **CNN built from scratch**
- **CNN with data augmentation**
- **Transfer Learning using ResNet50**

All tests were performed on **Small (500)**, **Medium (2000)**, and **Full (11000)** image datasets.

---

## 📂 Project Structure

├── data/ # Dataset (Small / Medium / Full)
├── models/ # Saved trained models
├── notebooks/ # Google Colab notebooks
├── results/ # Plots, confusion matrices, reports
├── README.md
└── requirements.txt

---

## 🚀 Experiments Overview

### **1. CNN From Scratch**
- Trained a custom convolutional neural network on raw images.
- **Small dataset accuracy:** ~65%
- **Medium dataset accuracy:** ~65%
- Suffered from overfitting and poor generalization due to limited data.

---

### **2. CNN + Data Augmentation**
Augmented images using:
- Rotation  
- Zoom  
- Horizontal flip  
- Width/height shift  

Augmentation results:
- **Small dataset:** 500 → 1750 images  
- **Medium dataset:** 2000 → 7000 images  

Performance improvements:
- **Accuracy increased to ~80–82%**
- Reduced overfitting but still limited by model capacity.

---

### **3. Transfer Learning (ResNet50)**
- Used ImageNet-pretrained **ResNet50** (feature extraction + fine-tuning).
- Achieved **~98% accuracy** on all dataset sizes.
- Required minimal training data to generalize well.
- Produced stable validation curves and very low loss.

---

## 📊 Key Findings

- **CNNs struggle on small datasets** due to weak feature extraction and overfitting.  
- **Augmentation helps**, but cannot replace real dataset diversity.  
- **Transfer learning dominates** because pretrained models already understand low-level & mid-level features.  
- Increasing dataset size improves stability, but **transfer learning already reaches maximum accuracy early**.

---

## 🧪 Results Summary

| Method                         | Small Dataset | Medium Dataset | Full Dataset |
|-------------------------------|---------------|----------------|--------------|
| CNN (Scratch)                 | ~65%          | ~65%           | —            |
| CNN + Augmentation            | ~80%          | ~82%           | —            |
| Transfer Learning (ResNet50)  | **~98%**      | **~98%**       | **~98%**     |

---

## 🛠️ Tech Stack
- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib & Seaborn  
- Scikit-learn  
- Google Colab  

---

## 📷 Sample Outputs
- Training/validation accuracy curves  
- Training/validation loss curves  
- Confusion matrices  
- Classification reports  

(All included in the `results/` directory)

---

## 🧩 Conclusion

Transfer learning is the most effective method for cat–dog classification.
It achieves near-perfect accuracy, requires less data, and generalizes extremely well compared to models trained from scratch

---

## 📌 How to Run

**Clone the repository:**
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

