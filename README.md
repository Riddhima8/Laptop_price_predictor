# 💻 Laptop Price Predictor  

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)  
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Regression-green)  
![Status](https://img.shields.io/badge/Status-Active-brightgreen)  

An end-to-end **machine learning project** that predicts the price of laptops based on their specifications such as brand, processor, RAM, GPU, storage, and more. 🚀  

---

## 📌 Motivation  

When buying or selling a laptop, deciding a fair price can be challenging.  
This project provides a **data-driven prediction model** to help buyers, sellers, and retailers estimate laptop prices quickly and accurately.  

---

## 📊 Demo  

### 🔹 Sample Dataset  
| Company | TypeName | RAM | CPU | GPU | SSD | Price (₹) |
|---------|----------|-----|-----|-----|-----|-----------|
| Dell    | Gaming   | 16  | i7  | GTX 1650 | 512 | 85,000 |
| HP      | Notebook | 8   | i5  | Intel UHD | 256 | 45,000 |

*(Data sample from training set)*  

---

## 🔄 Machine Learning Pipeline

Laptop Price Predictor follows this workflow:

1. **Data Collection**  
   - Dataset of laptop specifications and prices.

2. **Data Preprocessing**  
   - Handle missing values.  
   - Encode categorical features: Brand, CPU, GPU, TypeName.  
   - Scale numeric features: RAM, Storage.

3. **Model Training**  
   - Regression models: Random Forest / Linear Regression / XGBoost.  
   - Evaluate using R², MAE, RMSE.

4. **Pipeline Creation**  
   - Combine preprocessing + model into a single `Pipeline`.  
   - Save pipeline as `pipe.pkl`.

5. **Prediction**  
   - Load `pipe.pkl` in `main.py`.  
   - Input new laptop specifications.  
   - Output predicted price.

6. **Deployment **  
   - Using render


### 🔹 Model Performance  
 

- **R² Score:** 0.87  
- **MAE:** 4,200 ₹  
- **RMSE:** 6,100 ₹  

*(Numbers are placeholders – replace with your results!)*  

---

### 🔹 Web/App Interface (Optional)  

If deployed with **Flask / Streamlit / Heroku**:  

![App Demo](https://laptop-price-predictor-1-m544.onrender.com/)  

Users can enter laptop specs and instantly get a predicted price.  

---

## 🛠️ Tech Stack  

- **Python 3.8+**  
- **Scikit-learn, Pandas, NumPy**  
- **Pickle** for model serialization  
- **Matplotlib / Seaborn** for visualization  
- **Heroku / Flask / Streamlit** (for deployment)  

---


### File Descriptions

- **main.py**: Handles user input for laptop specifications and outputs predicted price.
- **requirements.txt**: Contains all necessary Python packages to run the project.
- **setup.sh**: Optional script to automate environment setup and dependency installation.
- **df.pkl**: Pickled cleaned dataset used for training.
- **pipe.pkl**: Pickled machine learning pipeline including preprocessing and trained model.
- **README.md**: Documentation with instructions, usage, and project details.


