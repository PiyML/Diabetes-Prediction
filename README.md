# Diabetes Prediction using Classical Machine Learning

## Project Overview
This project focuses on predicting the onset of diabetes using classical machine learning techniques applied to medical diagnostic data. The goal is to build a reliable and interpretable classification system that can assist in early diabetes screening while prioritising medically relevant evaluation metrics.

Two supervised learning algorithms are implemented and compared:
- Logistic Regression
- Linear Discriminant Analysis (LDA)

Special emphasis is placed on **recall** and **ROC–AUC**, as false negatives in medical diagnosis can have serious consequences.

---

## Problem Statement
Diabetes is a serious, life-threatening disease that requires early diagnosis to prevent severe health complications. Medical datasets often contain noisy, incomplete, and complex information, making manual analysis difficult. This project aims to leverage classical machine learning models to predict whether a patient is diabetic based on clinical measurements.

---

## Dataset
- **Dataset:** Pima Indians Diabetes Dataset  
- **Source:** UCI Machine Learning Repository / Kaggle  
- **Population:** Female patients of Pima Indian ancestry  

### Features
- Pregnancies  
- Glucose  
- BloodPressure  
- SkinThickness  
- Insulin  
- BMI  
- DiabetesPedigreeFunction  
- Age  

### Target Variable
- Outcome  
  - `0` → Non-diabetic  
  - `1` → Diabetic  

---

## ⚙️ Methodology
The project follows a complete machine learning pipeline:

1. Data exploration and understanding  
2. Handling missing and biologically invalid values  
3. Feature scaling and train–test split  
4. Model training using Logistic Regression and LDA  
5. Model evaluation using classification metrics  
6. Model comparison using ROC Curve and AUC  
7. Interpretation of feature importance  

---

## Data Preprocessing
- Identified medically invalid zero values in features such as Glucose, BMI, Insulin, etc.
- Replaced invalid zeros with `NaN`
- Imputed missing values using the **median** to reduce the impact of outliers
- Applied **StandardScaler** for feature normalization
- Prevented **data leakage** by fitting scalers only on training data

---

## Models Used

### Logistic Regression
- Discriminative model
- Estimates probability using a sigmoid function
- L2 regularization used to prevent overfitting
- Highly interpretable coefficients

### Linear Discriminant Analysis (LDA)
- Generative model
- Assumes normally distributed classes with shared covariance
- Effective on smaller datasets
- Maximises class separability

---

## Model Evaluation
Models were evaluated on an unseen test set using:
- Accuracy
- Precision
- Recall
- F1-score

**Recall was prioritised** due to the high cost of false negatives in medical diagnosis.

---

## ROC Curve & AUC
- ROC curves were plotted for both models
- Area Under the Curve (AUC) was computed
- **LDA achieved higher ROC–AUC**, indicating better class separation across thresholds

---

## Feature Importance
Logistic Regression coefficients were analysed for interpretability:
- **DiabetesPedigreeFunction** showed the strongest positive influence
- **BMI** and **Glucose** were significant predictors
- Negative coefficients indicated features associated with lower diabetes risk

These findings align well with established medical knowledge.

---

## Results Summary
- Both models performed reasonably well
- **LDA achieved higher recall and ROC–AUC**
- Logistic Regression offered better interpretability
- LDA was more suitable for diabetes screening

---

## Limitations
- Small dataset size limits generalisation
- Dataset restricted to a specific population group
- Only classical linear models were explored

---

## Future Improvements
- Train on larger and more diverse datasets
- Optimise decision thresholds to further improve recall
- Explore non-linear models (SVM, Random Forest, Gradient Boosting)
- Apply k-fold cross-validation
- Integrate additional clinical features for real-world deployment

---

## Conclusion
This project demonstrates how classical machine learning techniques can be effectively applied to medical diagnostic problems. While Logistic Regression provides strong interpretability, **Linear Discriminant Analysis is recommended for diabetes screening due to its superior recall and ROC–AUC**, making it more suitable for healthcare applications where minimising false negatives is critical.

---



##  Author
**Piyush Singh Bhadoriya**  
Data Science & Machine Learning Enthusiast  

---

## License
This project is for academic and educational purposes.

