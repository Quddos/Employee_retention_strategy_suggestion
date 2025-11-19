# Employee_retention_strategy_suggestion
🧠 Employee Retention Prediction System (AI-Powered HRM)  Intelligent HR Decision Support System for predicting employee retention using Machine Learning, Explainable AI (SHAP), and a Progressive Web App (PWA) interface built with Next.js. Developed to empower HR departments with data-driven insights and actionable retention strategies.

🚀 Overview
Project Link: https://employee-seven-roan.vercel.app/
PWA application code: https://github.com/Quddos/employee

The Employee Retention Prediction System enables HR professionals to make evidence-based workforce decisions by analyzing employee attributes and predicting their likelihood to stay or leave.

It combines:

🧩 AI-based predictive analytics

⚡ Explainable AI (SHAP)

💡 Next.js PWA user interface

🌐 FastAPI microservice backend

☁️ Cloud-native deployment (Vercel + Render)

Through a clean and interactive dashboard, HR managers can input details such as age, salary, experience, and department, and instantly receive:

🎯 Retention classification (“Likely to Stay” / “Likely to Leave”)

📊 SHAP-based feature contribution visualization (why the model made its decision)

🧰 Tech Stack
Layer	Technology	Purpose
Frontend (Web App)	🖥️ Next.js 14
 + Tailwind CSS
 + next-pwa
	Progressive Web App (PWA) interface for HR data input
Backend (API)	⚙️ FastAPI
	RESTful API for ML inference and SHAP analysis
Machine Learning Engine	🤖 Scikit-learn
, SHAP
	Model training, classification, and explainability
Model Persistence	💾 Joblib
	Saving and loading serialized ML models
Deployment	☁️ Vercel
 (Frontend) + Render
 (Backend)	Cloud hosting & continuous deployment
Version Control	🧭 GitHub
	Repository hosting and collaboration
🧩 Architecture Overview
   +-------------------------------+
   |        HR Web Interface       |
   | (Next.js + Tailwind + PWA)    |
   +---------------+---------------+
                   |
                   v
   +-------------------------------+
   |      Next.js API Route        |
   |     (/api/predict endpoint)   |
   +---------------+---------------+
                   |
                   v
   +-------------------------------+
   |       FastAPI Backend         |
   | (Model Inference + SHAP)      |
   +---------------+---------------+
                   |
                   v
   +-------------------------------+
   |   Trained ML Model (Scikit)   |
   | (.pkl files: model, encoder)  |
   +-------------------------------+

⚙️ Core Features

✅ Employee Retention Prediction — Classifies employee likelihood to stay or leave.
✅ Explainable AI — SHAP analysis highlights which factors influenced predictions.
✅ Modern HR UI — Clean dashboard for seamless data entry and insights.
✅ PWA Enabled — Works offline and across devices.
✅ Cloud Deployed — Scalable and accessible anywhere.
✅ Modular Design — Easy integration with HRM/ERP systems.

🧑‍💼 Use Case

Designed for:

HR professionals analyzing workforce retention patterns

Data analysts studying employee churn dynamics

Organizations optimizing retention strategies through AI-driven insights

🧠 Machine Learning Workflow

Data Preparation — Feature cleaning, encoding, scaling

Model Training — Classification using Scikit-learn

Explainability — SHAP for model transparency

Serialization — Model and encoders stored via Joblib

Deployment — FastAPI for inference + Next.js for interaction

User Interaction — HR inputs data via PWA form → Instant AI prediction

🧪 API Specification (FastAPI)

POST /predict

Request Example:

{
  "age": 32,
  "gender": "Female",
  "department": "Finance",
  "salary": 72000,
  "years_at_company": 3.8
}


Response Example:

{
  "prediction": "Likely to Stay",
  "confidence": 0.91,
  "shap_values": {
    "age": -0.04,
    "salary": 0.18,
    "years_at_company": 0.29
  }
}

☁️ Deployment Architecture
Component	Platform	Notes
Backend API	Render (Free Tier)	FastAPI app with model inference
Frontend PWA	Vercel	Next.js PWA, proxying API calls
Model Files	Stored in Backend Repo	.pkl model, encoder, and scaler
🧱 Folder Structure
employee-retention-ai/
├── backend/
│   ├── main.py
│   ├── requirements.txt
│   ├── employee_retention_model.pkl
│   ├── encoder.pkl
│   └── scaler.pkl
│
└── frontend/
    ├── app/
    │   ├── api/predict/route.ts
    │   └── EmployeeRetentionForm.tsx
    ├── public/manifest.json
    ├── package.json
    └── next.config.js

🔮 Future Enhancements

🧬 Integration with Gemini API for adaptive strategy recommendations

📊 HR analytics dashboard (retention trends, insights)

🔐 Authentication & role-based access (HR/Admin)

🧠 Continuous model retraining pipeline

🌍 Multilingual UI for global HR teams

💻 Getting Started
1️⃣ Clone Repository
git clone https://github.com/Quddos/Employee_retention_strategy_suggestion.git

2️⃣ Setup Backend
cd backend
pip install -r requirements.txt
uvicorn main:app --reload

3️⃣ Setup Frontend
cd frontend
npm install
npm run dev

🤝 Collaboration & Contact

This project welcomes researchers, developers, and HR tech innovators to collaborate on advancing AI-powered HR systems.

📧 Email: raheemquddus@gmail.com

💬 Let’s collaborate to build transparent, ethical, and intelligent HR analytics solutions.

🏷️ Keywords

AI in HRM • Employee Retention • Explainable AI • SHAP • Next.js • FastAPI • Vercel • Render • Machine Learning • PWA
