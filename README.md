# Predict-Patient-Readmission-plpweek5AI

🏥 Patient Readmission Predictor
A machine learning-powered web app that predicts whether a patient is likely to be readmitted within 30 days of hospital discharge. Built using Streamlit, trained in Google Colab, and deployable via ngrok or Replit.

🚀 Project Overview
Hospital readmissions can result in increased costs, resource strain, and poor patient outcomes. This application assists healthcare providers by identifying patients at high risk of readmission, enabling proactive intervention.

🔍 Features
Predicts readmission risk using clinical and demographic data

User-friendly form to input patient info

Instant risk assessment with confidence scores

Trained on simulated patient data for demonstration

Lightweight and deployable in browser (Colab/Replit)

🧠 Machine Learning Model
Model: Logistic Regression (with class_weight='balanced')

Training: Simulated dataset of 500 patients

Features Used:

Age

Gender

Number of previous admissions

Length of stay

Chronic illness status

Discharge type

📦 Tech Stack
Tool	Purpose
Python	Core programming language
Streamlit	Frontend UI for the web app
scikit-learn	ML model training & evaluation
pandas, numpy	Data manipulation and preprocessing
ngrok	Public tunneling (for Colab)

✅ Usage Instructions
🔹 Option 1: Run on Google Colab
Open your Colab Notebook.

Install dependencies:

python
Copy
Edit
!pip install streamlit pyngrok scikit-learn pandas numpy
Write the app.py using %%writefile.

Run the Streamlit app with ngrok:

python
Copy
Edit
from pyngrok import ngrok
public_url = ngrok.connect(8501)
!streamlit run app.py &>/content/logs.txt &
print("App URL:", public_url)
Open the displayed URL in your browser.

🔹 Option 2: Run on Replit
Go to https://replit.com → Create a new Python Repl.

Create two files:

app.py → Paste the full Streamlit code.

requirements.txt:

nginx
Copy
Edit
streamlit
scikit-learn
pandas
numpy
In the Replit shell, run:

arduino
Copy
Edit
streamlit run app.py
🔐 Ethical Considerations
This app uses simulated data and should not be used for real medical decisions.

Complies with privacy-by-design principles; no real patient data is used.

For real deployment, compliance with HIPAA or GDPR is essential.

📈 Future Improvements
Integrate with real hospital EHR systems

Deploy model as a REST API (Flask or FastAPI)

Add visual analytics (e.g., risk history, trends)

Support for uploading CSV records for bulk predictions

👨‍⚕️ Built With Purpose
This project is part of an AI Development Workflow assignment focused on healthcare applications, ethics, deployment, and real-world implementation.

