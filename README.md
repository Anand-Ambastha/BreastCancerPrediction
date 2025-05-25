## 🧬 Breast Cancer Classification using Machine Learning
This project aims to accurately classify breast cancer tumors as Malignant (M) or Benign (B) using supervised machine learning models. The focus is on building a reliable and explainable model that performs well not only in accuracy but also in handling real-world data sensitivity using metrics like Precision, Recall, F1-Score, and Support.

##📂 Dataset Details
Source: UCI ML Repository – Breast Cancer Wisconsin (Diagnostic) Data Set

##Features: 
30 real-valued inputs derived from digital images of breast masses (radius, texture, perimeter, etc.)

##Target: Binary classification

-Malignant (M) → 1

-Benign (B) → 0

##🔍 Problem Statement
Early detection of breast cancer is crucial. This classification task helps predict the nature of the tumor and assists medical practitioners in diagnosis. We aim to create a model that minimizes false negatives (i.e., missing a malignant tumor).

##🧪 Models Implemented & Compared
-Logistic Regression

A simple, interpretable baseline model.

Performed decently but struggled with complex patterns.

-Random Forest Classifier

Ensemble model that improves accuracy by reducing variance.

Handled non-linearity better than Logistic Regression.

-XGBoost (Extreme Gradient Boosting) ✅

Final selected model.

Demonstrated the highest accuracy and balanced performance across all metrics.

##✅ Why XGBoost?
Good accuracy on test data.

The model must avoid classifying malignant tumors as benign..

Efficient training time and supports advanced tuning.

Feature importance and interpretation available.

##📈 Performance Metrics
In real-world healthcare scenarios, accuracy is not enough. We must also evaluate:

##Metric	Description
Precision	Of all predicted malignant cases, how many were truly malignant? (Low FP)
Recall	Of all actual malignant cases, how many were correctly predicted? (Low FN)
F1-Score	Harmonic mean of Precision and Recall. Balances both.
Support	Number of actual instances for each class in the test set.

These metrics were derived using classification_report from sklearn.metrics to ensure fairness and reliability in predictions.

##📊 Final Results (Approximate)
Model	Accuracy	Notes
Logistic Regression	~93%	Basic linear model
Random Forest	~94%	Good generalization
XGBoost	~94%	Best overall performance ✅

Note: You can view full classification reports inside the Jupyter notebook for per-class precision/recall.

##💡 Future Enhancements
Add ROC-AUC Curve and Confusion Matrix visualization.

Tune hyperparameters using GridSearchCV or Optuna.

Integrate model explainability tools like SHAP or LIME.

Save and deploy model using FastAPI or Flask.

🧰 How to Run
Clone the repo

bash
Copy code
git clone https://github.com/Anand-Ambastha/BreastCancerPrediction.git
cd BreastCancerPrediction
Install dependencies

bash
Copy code
pip install -r requirements.txt
Run the notebook
Open Breast_Cancer__Classification.ipynb in Jupyter/Colab and execute all cells.

🧠 Author
Anand Ambastha
