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

### 🔹 ML Pipeline Overview  

![Pipeline](https://raw.githubusercontent.com/github/explore/main/topics/machine-learning/machine-learning.png)  

- Data Preprocessing (cleaning, encoding, scaling)  
- Regression Model (Random Forest / Linear Regression / XGBoost)  
- Exported ML pipeline as `pipe.pkl`  

---

### 🔹 Model Performance  

![Results](https://raw.githubusercontent.com/plotly/datasets/master/graph/iris-data.png)  

- **R² Score:** 0.87  
- **MAE:** 4,200 ₹  
- **RMSE:** 6,100 ₹  

*(Numbers are placeholders – replace with your results!)*  

---

### 🔹 Web/App Interface (Optional)  

If deployed with Render:  

![App Demo](https://laptop-price-predictor-1-m544.onrender.com/)  

Users can enter laptop specs and instantly get a predicted price.  

---

## 🛠️ Tech Stack  

- **Python 3.8+**  
- **Scikit-learn, Pandas, NumPy**  
- **Pickle** for model serialization  
- **Matplotlib / Seaborn** for visualization  
- **Render** (for deployment)  

---

## 📂 Project Structure  
Laptop_price_predictor/
│
├── main.py # Entry script for prediction
├── requirements.txt # Dependencies
├── setup.sh # Setup script
├── df.pkl # Processed dataset
├── pipe.pkl # Trained ML pipeline
├── Procfile # Deployment file
└── README.md # Documentation

## ⚙️ Installation & Setup  

1. Clone the repository:  
git clone https://github.com/Riddhima8/Laptop_price_predictor.git
cd Laptop_price_predictor

2.Create a virtual environment:
python -m venv venv
source venv/bin/activate     # Linux/Mac
venv\Scripts\activate        # Windows

3. Install dependencies:
pip install -r requirements.txt

4. Run the script:
python main.py

📈 Results
✔️ Accurate predictions for a wide range of laptops
✔️ Handles categorical + numerical features
✔️ Easy to extend with new datasets

🚀 Future Improvements
Collect larger and more updated datasets

Experiment with deep learning models

Add features like battery life, weight, display quality

Build a full-fledged web UI for real-time predictions


