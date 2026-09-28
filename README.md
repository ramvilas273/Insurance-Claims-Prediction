# 🚗 Insurance Claims Prediction

A Machine Learning web application built with **Streamlit** to estimate the probability that a policyholder will file an insurance claim.

**Dataset Overview:**
The dataset utilized in this project comprises historical data on insurance claims, encompassing a variety of information about the policyholders, their demographics, past claim history, and other pertinent features. The dataset is structured to facilitate predictive modeling tasks aimed at accurately identifying the likelihood of future insurance claims.

## 🚀 Features

- Interactive insurance claim-risk prediction
- Estimated claim probability
- Higher-risk / lower-risk classification
- Vehicle model selection
- Subscription length, vehicle age, customer age and region density inputs
- Vehicle feature checkboxes
- Probability progress indicator
- Streamlit user interface

## 🧠 Input Features

### Policy & Customer

- Subscription length (years)
- Vehicle age (year)
- Customer age
- Region population density

### Vehicle

- Vehicle model

### Vehicle Features

- Has parking sensors
- Has front fog lights
- Has brake assist
- Has power steering
- Driver seat height adjustable
- Day/night rear-view mirror
- Has speed alert

Boolean selections are converted to `0` or `1` before prediction.

## 🤖 Machine Learning

The application loads these saved objects using Joblib:

```text
claim_model.pkl
model_columns.pkl
model_options.pkl
```

## 📊 Prediction Output

The app displays an **Estimated claim probability**, for example:

```text
Estimated claim probability
50.1%
```

If the model predicts `1`:

```text
⚠️ This policy is flagged as HIGHER risk of a claim.
```

If the model predicts `0`:

```text
✅ This policy is flagged as LOWER risk of claim.
```

A progress bar represents the estimated probability.

## 🖥️ Example Application

Example input:

```text
Subscription length: 8.40 years
Vehicle age: 4.50 years
Customer age: 65
Region population density: 9594
Vehicle model: M2
```

The user can enable or disable the available vehicle features and click **Predict claim risk**.

## 🛠️ Technologies Used

- Python
- Pandas
- Joblib
- Scikit-learn
- Streamlit
- Jupyter Notebook

## 📦 Installation

Install the required packages:

```bash
pip install -r requirements.txt
```

Main packages used by the Streamlit application:

```text
streamlit
pandas
joblib
scikit-learn
```

## ▶️ Run the Application

```bash
streamlit run app.py
```

## 🔄 Project Workflow

```text
Insurance Claims Dataset
        ↓
Data Preparation
        ↓
Feature Engineering / Encoding
        ↓
Model Training
        ↓
Model Evaluation
        ↓
Save Trained Model
        ↓
Streamlit Application
        ↓
User Input
        ↓
Claim Probability
        ↓
Risk Classification
```

## 🎯 Project Objective

The objective of this project is to demonstrate an end-to-end Machine Learning workflow for insurance claim-risk prediction, from preparing the dataset and training the model to saving the model and deploying an interactive Streamlit prediction application.

## ⚠️ Disclaimer

The prediction is a machine-learning estimate based on the data used to train the model. It should not be treated as a definitive assessment of an individual's actual insurance risk or claim outcome.

## 👨‍💻 Author

**Ram Vilas**
