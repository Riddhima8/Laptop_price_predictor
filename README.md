# 💻 Laptop Price Predictor

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Regression-green)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikitlearn)
![Deployment](https://img.shields.io/badge/Deployment-Render-purple)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

An end-to-end **Machine Learning Regression Project** that predicts laptop prices based on hardware specifications such as processor, RAM, GPU, storage, display resolution, operating system, and brand.

The project covers the complete ML workflow — from **data preprocessing and feature engineering** to **model training, evaluation, pipeline creation, and deployment** using Streamlit and Render. 🚀

---

# 📌 Problem Statement

Laptop prices vary significantly depending on configuration and specifications.
For buyers, sellers, and retailers, estimating a fair market price manually can be inconsistent and time-consuming.

This project uses machine learning to build a **data-driven laptop price prediction system** capable of estimating prices from technical specifications with high accuracy.

---

# ✨ Features

* 📊 Data preprocessing and feature engineering
* 🤖 Multiple regression model training and comparison
* ⚡ Ensemble learning using Voting Regressor
* 🔍 Automated preprocessing pipeline using Scikit-learn
* 🌐 Streamlit web application for real-time predictions
* ☁️ Deployment on Render

---

# 📂 Dataset Features

The model uses laptop specifications including:

* Company / Brand
* Laptop Type
* RAM Size
* CPU Brand & Processor
* GPU Brand
* SSD / HDD Storage
* Operating System
* Screen Resolution
* IPS Display
* Touchscreen Support
* Screen Size & PPI

---

# 🔄 Machine Learning Workflow

## 1️⃣ Data Collection

* Imported laptop dataset containing specifications and prices.
* Cleaned inconsistent and redundant values.

---

## 2️⃣ Data Preprocessing

Performed extensive preprocessing and feature engineering:

* Handled missing values and duplicate entries
* Extracted:

  * CPU Brand
  * GPU Brand
  * Storage Information
  * IPS Display Feature
  * Touchscreen Feature
* Calculated:

  * Pixels Per Inch (PPI) from screen resolution
* Encoded categorical variables using:

  * One-Hot Encoding
* Applied log transformation on target variable for improved model performance

---

## 3️⃣ Model Training & Evaluation

Trained and evaluated multiple regression models:

* Linear Regression
* Ridge Regression
* Lasso Regression
* K-Nearest Neighbors
* Decision Tree Regressor
* Random Forest Regressor
* Extra Trees Regressor
* AdaBoost Regressor
* Gradient Boosting Regressor
* Support Vector Regressor (SVR)
* XGBoost Regressor
* Voting Regressor
* Stacking Regressor

### 📈 Best Model Performance

| Metric   | Score     |
| -------- | --------- |
| R² Score | **0.89**  |
| MAE      | **0.158** |

The final model used an ensemble-based **Voting Regressor** combining:

* Random Forest
* Gradient Boosting
* XGBoost
* Extra Trees

---

# ⚙️ ML Pipeline

Created reusable Scikit-learn pipelines using:

* `Pipeline`
* `ColumnTransformer`

The complete pipeline includes:

1. Feature preprocessing
2. Encoding
3. Model prediction

Serialized using:

* `pipe.pkl`

---

# 🌐 Deployment

The project is deployed using:

* **Streamlit** for frontend UI
* **Render** for cloud hosting

### 🔗 Live Demo

👉 https://laptop-price-predictor-1-m544.onrender.com/

Users can:

* Select laptop specifications
* Enter hardware details
* Instantly receive predicted laptop prices

---

# 🛠️ Tech Stack

## Languages & Libraries

* Python 3.8+
* Pandas
* NumPy
* Scikit-learn
* XGBoost

## Visualization

* Matplotlib
* Seaborn

## Deployment

* Streamlit
* Render

## Serialization

* Pickle

---

# 📁 Project Structure

```bash
Laptop-Price-Predictor/
│
├── app.py                 # Streamlit application
├── main.py                # Prediction logic
├── pipe.pkl               # Trained ML pipeline
├── df.pkl                 # Cleaned dataset
├── Laptop_price_predictor.ipynb
├── requirements.txt
├── setup.sh
└── README.md
```

---

# 🚀 Installation & Setup

## 1️⃣ Clone Repository

```bash
git clone https://github.com/Riddhima8/Laptop_price_predictor.git
cd Laptop_price_predictor
```

---

## 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 3️⃣ Run Streamlit App

```bash
streamlit run app.py
```

---

# 🖥️ Sample Prediction

| Feature   | Value           |
| --------- | --------------- |
| Brand     | Dell            |
| Processor | Intel Core i7   |
| RAM       | 16 GB           |
| GPU       | NVIDIA GTX 1650 |
| SSD       | 512 GB          |
| Type      | Gaming          |

### 💰 Predicted Price

₹85,000 (approx.)

---

# 📚 Key Learnings

Through this project, I gained practical experience in:

* Feature Engineering
* Regression Modeling
* Ensemble Learning
* Hyperparameter Tuning
* Scikit-learn Pipelines
* Model Serialization
* Streamlit Deployment
* End-to-End ML Workflow

---

# 🔮 Future Improvements

* Add deep learning-based regression models
* Improve UI/UX of Streamlit dashboard
* Add price trend visualization
* Integrate live e-commerce laptop data
* Deploy using Docker & CI/CD pipelines

---

# 👩‍💻 Author

**Riddhima Urankar**

* GitHub: https://github.com/Riddhima8

---
