# ❤️ Heart Failure Prediction

This project focuses on predicting the risk of heart failure using machine learning and deploying it as a Flask web application. It demonstrates an end-to-end data science workflow — from data cleaning and model training to web-based deployment — built using real clinical data.

---

## 🧠 Overview
The goal of this project is to help healthcare professionals identify patients at risk of heart failure based on various medical parameters. Using the UCI Heart Failure Clinical Records dataset, the project applies advanced machine learning algorithms to generate accurate and interpretable predictions. The resulting model is integrated into a user-friendly web interface where users can input patient details and instantly receive a prediction.

---

## 🧰 Tools & Technologies
- Python (Pandas, NumPy, Scikit-learn, XGBoost)
- Visualization: Matplotlib, Seaborn
- Model Deployment: Flask
- Frontend: HTML, CSS
- Model Storage: Pickle (.pkl)

---

## 🎯 Objectives
- Clean and preprocess clinical heart failure data
- Perform exploratory data analysis (EDA) and identify key predictors
- Build and tune an XGBoost classification model
- Evaluate model performance using metrics such as Accuracy and ROC-AUC
- Deploy the trained model as an interactive Flask web app

---

## 📂 Project Structure
Heart_Failure_Prediction/
│
├── heart failure prediction.ipynb → Model training & evaluation  
├── heart_failure_clinical_records_dataset.csv → Dataset used  
├── app.py → Flask backend application  
├── index.html → Frontend web interface  
├── trained_model.pkl → Trained XGBoost model  
├── scaler.pkl → Data scaler for preprocessing  
├── default_feature_values.pkl → Default feature values for input fields  
└── README.md → Project documentation

---

## 📊 Dataset
Source: UCI Heart Failure Clinical Records Dataset  
Records: 299 patients  
Features: 12 clinical attributes  
Target Variable: DEATH_EVENT (1 = Death, 0 = Survived)

Key Features:
- Age — Age of the patient  
- Anaemia — 1 = Yes, 0 = No  
- Creatinine Phosphokinase — Level of CPK enzyme in blood  
- Ejection Fraction — % of blood leaving the heart per contraction  
- Serum Creatinine — Level of creatinine in blood  
- Serum Sodium — Blood sodium level  
- High Blood Pressure — 1 = Yes, 0 = No  
- Time — Follow-up period (in days)  
- DEATH_EVENT — Target variable (1 = death, 0 = survived)

---

## ⚙️ How to Run the Project

1️⃣ Install Dependencies  
Make sure Python is installed, then run this command:  
pip install flask numpy pandas scikit-learn xgboost matplotlib seaborn  

2️⃣ Run the Flask Application  
Execute the following in your terminal:  
python app.py  

3️⃣ Open in Browser  
Once running, open your browser and go to:  
http://127.0.0.1:5000/  

4️⃣ Use the Application  
- Input patient details (age, ejection fraction, serum creatinine, etc.)  
- Click "Predict Heart Failure"  
- The app returns High Risk or Low Risk, along with the probability.

---

## 📈 Model Performance
Algorithm: XGBoost Classifier  
Accuracy: ~85%  
ROC-AUC: ~0.90  
Key Predictors: Ejection Fraction, Serum Creatinine, Age  

The model was validated using cross-validation and tuned for maximum accuracy without overfitting.

---

## 🧩 Web Application Features
- Clean and intuitive HTML-based input form  
- Real-time prediction on form submission  
- Color-coded output:  
  - 🟥 High Risk — High probability of heart failure  
  - 🟩 Low Risk — Low probability of heart failure  
- Uses trained_model.pkl and scaler.pkl for predictions

---

## 💡 Key Insights
- Ejection Fraction and Serum Creatinine are strong indicators of heart failure risk.  
- Lower ejection fraction (<40%) significantly increases the chance of failure.  
- Early detection can support preventive healthcare measures and improve outcomes.

---

## 🚀 Future Enhancements
- Add SHAP/LIME explainability for feature importance visualization  
- Deploy on Heroku, Render, or AWS for public access  
- Add database integration for patient records (PostgreSQL/SQLite)  
- Improve web UI using Bootstrap or React  

---

## 🏁 Summary
This project demonstrates a complete data science lifecycle:  
Data Cleaning → EDA → Model Training → Evaluation → Deployment  

It integrates machine learning with a web interface, providing a real-world healthcare solution that supports clinical decision-making through data-driven insights.

##Author
Pranathi Doddamani
