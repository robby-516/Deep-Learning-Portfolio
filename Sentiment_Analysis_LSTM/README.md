# 🎬 Sentiment Analysis on IMDb Reviews with LSTM

## 📝 Problem Statement
The goal of this project is to classify **movie reviews** from the **IMDb dataset** as either:
1. **Positive Review** 👍  
2. **Negative Review** 👎  

This demonstrates how **LSTM (Long Short-Term Memory)** networks can capture sequential dependencies in natural language.

---

## 🔎 Approach
1. **Dataset Preparation**:
   - Used the IMDb dataset with the **top 10,000 most frequent words**.  
   - Each review truncated/padded to a fixed length of **200 words**.  
   - Labels: `0` → Negative, `1` → Positive.  

2. **Model Architecture**:
   - `Embedding (10000 → 128)`  
   - `LSTM (128 units)`  
   - `Dense (1, sigmoid)`  

3. **Training**:
   - Optimizer: **Adam**  
   - Loss: **Binary Crossentropy**  
   - Metrics: **Accuracy**  
   - Trained for **5 epochs**, batch size **64**.  
   - Validation split = **20%**.  

4. **Evaluation**:
   - Tested on unseen IMDb reviews (25,000 test set).  

5. **Prediction**:
   - Model predicts sentiment for individual reviews.  
   - Example:  
     ```
     Positive Review
     Actual Label: 1
     ```

---

## 📈 Output
- **Test Accuracy**: ~`86%`  
- Model successfully predicts **positive/negative** sentiment on new reviews.  

---

## 📊 Visualization
Training vs Validation Accuracy (conceptual):  

![Accuracy Plot](accuracy_plot.png)  

*(The plot shows accuracy improving across epochs for both training and validation.)*

---

## ✅ Key Insights
- **LSTMs** are powerful for sequential data like text, as they capture dependencies across words.  
- Using an **embedding layer** allows the model to learn dense word representations.  
- The model achieves strong performance (~86%) with relatively simple architecture.  
- This project demonstrates how deep learning can be applied to **sentiment analysis** tasks.  

---
