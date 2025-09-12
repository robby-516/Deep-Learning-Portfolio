# 🧠 MNIST CNN Classifier

## 📝 Problem Statement
The objective of this project is to classify **handwritten digits (0–9)** from the **MNIST dataset** using a Convolutional Neural Network (CNN).  
This task is a classic benchmark in computer vision and deep learning.

---

## 🔎 Approach
1. **Data Loading**: MNIST dataset (60,000 training + 10,000 testing images) was loaded using TensorFlow/Keras.  
2. **Preprocessing**:
   - Normalized pixel values to range `[0,1]`.  
   - Reshaped images from `(28,28)` to `(28,28,1)` for CNN compatibility.  
   - Converted labels to **one-hot encoding**.  
3. **Model Architecture**:
   - 3 Convolutional layers (`Conv2D`) with ReLU activation.  
   - 2 MaxPooling layers for spatial downsampling.  
   - Dense layers for classification.  
   - Output layer with **Softmax** for 10 classes.  
4. **Training**: Model trained for **5 epochs** with batch size **64**, using **Adam optimizer**.  
5. **Evaluation**: Performance measured on the test dataset.  

---

## 📈 Output
- **Test Accuracy**: ~`98.98%` (varies slightly per run).  

---

## ✅ Key Insights
- CNNs are highly effective in capturing spatial features from images.  
- Even a relatively shallow CNN achieves near state-of-the-art results on MNIST.  
- This project builds the foundation for more complex vision tasks (like CIFAR-10 and ImageNet).  

---
