❤️ Heart Failure Prediction
📘 Overview

This project predicts the risk of heart failure using a machine learning model trained on clinical patient data.
It includes a Flask web application that allows users to input medical parameters and instantly receive a risk prediction.
The aim is to assist healthcare professionals in identifying high-risk patients early for better diagnosis and treatment.

🧠 Objective

To build a predictive model that estimates the likelihood of heart failure based on key medical attributes such as:

Age

Ejection Fraction

Serum Creatinine

High Blood Pressure

Follow-up Time

The final model was deployed as a simple, interactive Flask web app.

🧰 Tools & Technologies

Programming: Python (Pandas, NumPy, Scikit-learn, XGBoost)

Visualization: Matplotlib, Seaborn

Deployment: Flask

Frontend: HTML, CSS

Model Storage: Pickle

📂 Project Structure

📁 Heart_Failure_Prediction/
│
├── heart failure prediction.ipynb → Model training & evaluation
├── heart_failure_clinical_records_dataset.csv → Dataset used
├── app.py → Flask backend app
├── index.html → Frontend web interface
├── trained_model.pkl → Trained XGBoost model
├── scaler.pkl → Scaler for preprocessing
├── default_feature_values.pkl → Default values for input fields
└── README.md → Project documentation

📊 Dataset

Source: UCI Heart Failure Clinical Records Dataset

Records: 299 patients
Features: 12 clinical variables
Target: DEATH_EVENT (1 = death, 0 = survived)

Feature Examples:

Feature	Description
Age	Age of the patient
Anaemia	1 = Yes, 0 = No
Creatinine Phosphokinase	Level of CPK enzyme in blood
Ejection Fraction	Percentage of blood leaving the heart per contraction
Serum Creatinine	Level of creatinine in blood
Serum Sodium	Blood sodium level
Time	Follow-up period (in days)
DEATH_EVENT	1 = death during follow-up, 0 = survived
⚙️ How to Run the Project
1️⃣ Install Dependencies

Make sure Python is installed, then install all required libraries:
pip install flask numpy pandas scikit-learn xgboost matplotlib seaborn

2️⃣ Run the Flask App

In your terminal, execute:
python app.py

3️⃣ Open in Browser

Visit:
http://127.0.0.1:5000/

4️⃣ Use the App

Enter patient details (age, ejection fraction, serum creatinine, etc.)

Click Predict Heart Failure

The app will return High Risk or Low Risk with probability percentage.

📈 Model Performance
Metric	Value
Algorithm	XGBoost Classifier
Accuracy	~85%
ROC-AUC	~0.90
Key Features	Ejection Fraction, Serum Creatinine, Age

The model was trained and tuned using cross-validation to achieve a balance between accuracy and interpretability.

🧩 Web Application

The web app (app.py + index.html) provides:

Simple input form for medical parameters

Instant predictions on form submission

Color-coded risk output (Red = High Risk, Green = Low Risk)

Uses trained_model.pkl and scaler.pkl for predictions

💡 Key Insights

Ejection Fraction and Serum Creatinine are the strongest predictors of heart failure.

Patients with low ejection fraction (<40%) have significantly higher risk.

Model predictions can support doctors in risk-based patient prioritization.

🚀 Future Enhancements

Add SHAP/LIME-based model explainability for interpretability.

Deploy the app on Heroku / AWS for global access.

Integrate a database backend for patient record storage.

Improve the web UI with Bootstrap or React for better styling.

🏁 Summary

This project demonstrates an end-to-end data science workflow:

Data Cleaning → Feature Engineering → Model Training → Deployment

It integrates machine learning and Flask to build a real-time healthcare prediction tool that could support early diagnosis and clinical decision-making.
