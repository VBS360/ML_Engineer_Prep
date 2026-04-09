# 📅 Day 16 – Model Deployment using Flask & Render

## 🎯 Objective

To convert a trained ML model into a real-world usable system by creating an API and deploying it on the cloud.

---

# 🚀 Project Overview

Built and deployed a **Churn Prediction System** that:

* Accepts user input
* Processes it using trained model logic
* Returns real-time predictions via API

---

# 🧠 Step-by-Step Implementation

## 🔹 1. Final Model Selection

* Chose **Logistic Regression (class_weight='balanced')**
* Reason:

  * Better recall (important for churn)
  * More stable across cross-validation
  * Interpretable and reliable

---

## 🔹 2. Model Saving

```python
import joblib

joblib.dump(model_LR2, "churn_model.pkl")
joblib.dump(X.columns.tolist(), "columns.pkl")
```

* `churn_model.pkl` → trained model
* `columns.pkl` → feature structure for inference

---

## 🔹 3. Flask API Creation

Created `app.py`:

```python
from flask import Flask, request, jsonify
import joblib
import pandas as pd

app = Flask(__name__)

model = joblib.load("churn_model.pkl")
columns = joblib.load("columns.pkl")

@app.route("/")
def home():
    return "Churn Prediction API is running"

@app.route("/predict", methods=["POST"])
def predict():
    data = request.json

    input_df = pd.DataFrame([data])
    input_df = pd.get_dummies(input_df)
    input_df = input_df.reindex(columns=columns, fill_value=0)

    prediction = model.predict(input_df)[0]

    return jsonify({
        "prediction": int(prediction)
    })

if __name__ == "__main__":
    app.run(debug=True)
```

---

## 🔹 4. Requirements File

Created `requirements.txt`:

```
flask
joblib
numpy
pandas
scikit-learn
```

---

## 🔹 5. Local Testing

* Ran Flask server:

```bash
python app.py
```

* Tested API using Python script:

```python
import requests

url = "http://127.0.0.1:5000/predict"

response = requests.post(url, json=data)
print(response.json())
```

* Successfully received prediction output

---

## 🔹 6. Deployment on Render 🌍

### Steps:

1. Created `Procfile`

```
web: python app.py
```

2. Updated app for production:

```python
import os

if __name__ == "__main__":
    port = int(os.environ.get("PORT", 5000))
    app.run(host="0.0.0.0", port=port)
```

3. Pushed project to GitHub
4. Connected repository to Render
5. Deployed as Web Service

---

## 🌐 Live API

👉 https://churn-deployment-oyki.onrender.com

---

# 🧪 API Usage

## Endpoint:

```
POST /predict
```

## Input:

* JSON format
* Must match training feature structure

## Output:

```json
{
  "prediction": 0
}
```

---

# 🧠 Key Concepts Learned

* Model serialization using joblib
* Flask API creation
* Handling real-time input data
* One-hot encoding during inference
* Column alignment using reindex
* REST API fundamentals
* Cloud deployment using Render

---

# 💼 Business Impact

* Converted ML model into a usable system
* Enabled real-time churn prediction
* Can be integrated into applications for customer retention strategies

---

# 🔥 Key Learnings

* Deployment is as important as model building
* Input preprocessing must match training pipeline
* APIs make ML models usable in production
* Cloud hosting enables real-world accessibility

---

# 🚀 Outcome

* Successfully built and deployed an end-to-end ML system
* Gained practical experience in ML engineering workflow
* Ready to explain deployment concepts in interviews

---

**Status:** ✅ Completed Day 16
