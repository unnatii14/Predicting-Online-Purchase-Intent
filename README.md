# Predicting Online Purchase Intent Using Machine Learning

This project applies machine learning models to predict whether a user will make a purchase based on their online session behavior on an e-commerce website.

---

## 📌 Problem Statement

Online shopping behavior provides key signals about purchase intent, such as time spent on pages, bounce rates, and visit patterns.  
By predicting whether a visitor is likely to make a purchase, businesses can improve targeting, recommendations, and conversions.

---

## 🛠️ Project Highlights

- Converted categorical columns (`Month`, `VisitorType`) and boolean columns (`Weekend`, `Revenue`) to numeric using `LabelEncoder`
- Performed exploratory data analysis to uncover trends (e.g., returning visitors have higher purchase intent)
- Scaled numerical features using `StandardScaler` to improve model performance
- Trained and evaluated multiple ML models:  
  `Logistic Regression`, `K-Nearest Neighbors (KNN)`, `Support Vector Classifier (SVC)`, `Decision Tree`, `Random Forest`
- Tuned KNN across `k = 1 to 50` to find optimal performance
- Tested impact of irrelevant features by adding random noise (curse of dimensionality)
- Applied `PCA` (Principal Component Analysis) for dimensionality reduction
- Used `SMOTE` to handle class imbalance in the target variable
- Evaluated models using accuracy, precision, recall, F1-score, and ROC AUC
- Verified consistency through `10-fold cross-validation`

---

## ✅ Key Results

- **Best Model: Random Forest**
  - Accuracy: **89.13%**
  - ROC AUC: **0.9218**
- KNN gave a strong baseline but performance declined with noise and dimensionality
- SMOTE significantly improved recall for minority class (buyers)
- Cross-validation showed stable and consistent results across folds

---

## 📈 Conclusion

Random Forest provided the best combination of performance and reliability.  
With proper preprocessing (label encoding, scaling), class balancing (SMOTE), and feature tuning (PCA, noise analysis), the model effectively predicts online purchase intent.  
This pipeline can be applied in real-world e-commerce systems to target potential buyers and optimize marketing efforts.

