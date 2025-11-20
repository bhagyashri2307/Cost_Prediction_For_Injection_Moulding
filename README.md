# 📌 Manufacturing Cost Calculation for Injection Moulding

## A Mechanical Engineering Project with Python Automation & Machine Learning

This project automates the manufacturing cost estimation process for injection-moulded components, replacing slow, error-prone manual calculations with a fast, accurate, data-driven system.

Using STL model processing, dataset creation, Random Forest regression, and a Streamlit app, the system predicts the total cost per part using only three inputs:

👉 **Length, Width, Height**

---

## 🔍 Project Motivation

Traditional cost estimation in injection moulding requires:

- Manual volume/weight calculations  
- Material usage calculations  
- Parts-per-cycle estimation  
- Cycle time and cycle cost computation  
- Final cost-per-part evaluation  

These steps take significant time and are prone to human error.

### This project solves that by:
- ✔ Automating dataset generation from STL models  
- ✔ Computing all required parameters programmatically  
- ✔ Training a machine learning model to predict cost  
- ✔ Offering a user-friendly app to get instant cost estimates  

---

## 🧩 Project Workflow

### 1️⃣ Dataset Creation from STL Models
**File:** `dataset_creation.ipynb`

- 30 STL mould models were collected.  
- Code extracts computed:  
  - Length  
  - Width  
  - Height  
  - Volume  
  - Weight  
  - Parts per cycle  
  - Raw material per cycle  
  - Cycle cost per cycle  
  - Cycle cost per part  
  - Total cost per part  

➡ All computed values saved to `dataset.csv`.  
This automated pipeline ensures accurate and consistent data recording.

---

### 2️⃣ Machine Learning Model Training
**File:** `model_training.ipynb`

- Loaded `dataset.csv`  
- Input features: **Length, Width, Height**  
- Target variable: **Total cost per part**  
- Algorithm: **RandomForestRegressor (sklearn)**  

Performed:  
- Train/Test split  
- Model training  
- Evaluation using **MAE, MSE, R²**  
- Exported trained model as `model.pkl`  

➡ The model captures nonlinear relationships between geometry and manufacturing cost.

---

### 3️⃣ Cost Prediction Web App
**File:** `app.py`

- Built using **Streamlit**  
- Loads the trained model  
- Accepts 3 user inputs:  
  - Length  
  - Width  
  - Height  

➡ Predicts and displays **total cost per part instantly**.  

This provides manufacturers an easy, real-time, decision-support tool.

---

## 📁 Repository Structure


├── dataset_creation.ipynb # Dataset extraction from STL files ├── model_training.ipynb # Model training and evaluation ├── app.py # Streamlit app for prediction ├── dataset.csv # Final dataset (extracted + computed data) ├── model.pkl # Trained RandomForest model ├── project_report.pdf # Official project documentation └── README.md # Project explanation



### 📂 Explanation of Files
- **dataset_creation.ipynb** → Jupyter notebook for extracting geometric and manufacturing parameters from STL files.  
- **model_training.ipynb** → Notebook for training and evaluating the Random Forest regression model.  
- **app.py** → Streamlit web app that predicts manufacturing cost per part based on user inputs.  
- **dataset.csv** → Final dataset containing computed values (length, width, height, volume, weight, cycle cost, etc.).  
- **model.pkl** → Serialized trained Random Forest model for deployment.  
- **project_report.pdf** → Official project documentation with methodology, results, and analysis.  
- **README.md** → Project overview and usage instructions.  

---

## 🧮 Technologies Used

### Mechanical / Manufacturing
- Injection moulding cost models  
- Material density & volume calculations  
- Cycle time cost modeling  

### Programming & Data
- Python  
- NumPy, Pandas  
- numpy-stl  
- Scikit-learn (**RandomForestRegressor**)  
- Streamlit
  
---

## 📊 Results & Evaluation
- Dataset of **30 STL models** processed  
- Model achieved **good predictive accuracy**  
- Streamlit UI tested with multiple real cases  

## 🚀 Key Features
- ✔ Real-time cost estimation  
- ✔ Accurate ML-based predictions  
- ✔ Automated STL geometry extraction  
- ✔ Fully scalable for new mould designs  
- ✔ Easy-to-use UI for engineers & managers  

---

## 🔮 Future Enhancements
Based on the report’s future scope:
- Add material selection options  
- Include cycle cooling, mold life, and complexity factors    
- Integrate with CAD tools (SolidWorks/Creo)  
- Use advanced ML models (XGBoost, ANN)  
- Real-time cost updates using fluctuating material prices  

---

## 🏁 Conclusion
This project demonstrates how **Mechanical Engineering Principles** can be integrated with **Python Automation** and **Machine Learning** to create a powerful, accurate cost estimation tool.

It provides a **fast, scalable, and error-free solution** for cost prediction — a major improvement over traditional manual methods.

