# 🏠 Housing Price Prediction – Linear & Random Forest Models

## 📌 Project Overview
This project implements **Linear Regression**, **Ridge Regression**, and **Random Forest Regression** to predict housing prices using the **Housing Price Prediction** dataset.  
The main goal is to compare model performances and improve accuracy through **feature engineering**.  

---

## 📂 Dataset
**Source:** [Kaggle – Housing Price Prediction Dataset](https://www.kaggle.com/datasets/harishkumardatalab/housing-price-prediction)   

### Original Columns:  
- `price`, `area`, `bedrooms`, `bathrooms`, `stories`,   
  `mainroad`, `guestroom`, `basement`, `hotwaterheating`,  
  `airconditioning`, `parking`, `prefarea`, `furnishingstatus`  

### Engineered Features:  
- **`price_per_sqft`** – Price per square foot   
- **`total_rooms`** – Sum of bedrooms and bathrooms  
- **`luxury_score`** – Total number of premium amenities (binary sum)  
- **`house_size`** – Categorized property size (`Small`, `Medium`, `Large`, `Very Large`)  

---

## ⚙️ Preprocessing Steps  
1. **Encoding:**  
   - Converted `yes/no` columns to `1/0`  
   - Mapped `furnishingstatus` to integers   
   - Encoded `house_size` categories to numeric values  
2. **Feature Engineering:** Added `price_per_sqft`, `total_rooms`, `luxury_score`, and `house_size`  
3. **Scaling:** Applied StandardScaler to numeric features for regression models  
4. **Train-Test Split:** 80% training, 20% testing  

---

## 📊 Models Used  
- **Linear Regression** (Baseline + with engineered features)   
- **Ridge Regression**  
- **Random Forest Regressor**  

---

## 🚀 Results

| Model                | MAE (₹)   | RMSE (₹)   | R²     |  
|----------------------|-----------|-----------|--------|  
| Linear Regression    | 4.45 L    | 6.34 L    | 0.8629 |  
| Ridge Regression     | 4.45 L    | 6.32 L    | 0.8640 |  
| Random Forest        | 2.12 L    | 3.42 L    | 0.9601 |  

---

## 📈 Key Observations  
- **Feature engineering** was the biggest contributor to improved accuracy (R² jumped from ~0.65 to 0.96 for Random Forest).  
- **Random Forest** outperformed Linear & Ridge Regression by capturing non-linear relationships.  
- **Linear Regression** still gave strong results and is better for interpretability.  

---

## 📌 Conclusion  
- Use **Random Forest** for best predictive accuracy.  
- Use **Linear Regression** for simpler, interpretable models.  
- Keep the engineered features for future datasets — they significantly improve performance.  

---

## 🛠️ Tools & Libraries  
- Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- Google Colab for implementation  

---

## 📜 How to Run  
1. Clone the repository
   ```bash
   git clone https://github.com/yourusername/housing-price-prediction.git
   cd housing-price-prediction
3. Run the notebook in Jupyter or Google Colab.

## 📬 Contact  
Author: Hemanth Yarra  
LinkedIn: [hemanth-yarra](https://www.linkedin.com/in/hemanth-yarra-5a1775305/)  
Email: yarrahemanth5@gmail.com  
 
