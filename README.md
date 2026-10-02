# Student Performance Indicator

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Flask](https://img.shields.io/badge/Flask-Web%20Framework-black)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Frontend](https://img.shields.io/badge/Frontend-TailwindCSS-06B6D4)

An end-to-end Machine Learning web application designed to predict a student's mathematics performance based on their demographic background, parental education level, and previous test scores. 

This project implements a modular, production-ready machine learning pipeline, complete with a clean, responsive web interface for real-time predictions.

---

## 📌 Project Overview

Understanding the factors that influence academic performance is crucial for educational development. This application takes in various student features—such as gender, race/ethnicity, parental level of education, lunch type, test preparation course completion, reading score, and writing score—and utilizes a trained regression model to forecast their math score.

## 🚀 Key Features

* **End-to-End ML Pipeline:** Modular architecture separating data ingestion, transformation, and model training components.
* **Interactive Web Interface:** A modern, responsive frontend built with Tailwind CSS and HTML to easily input student data and view predictions.
* **Robust Backend:** Powered by a lightweight Flask application routing predictions through the trained ML model.
* **Comprehensive Exploratory Data Analysis (EDA):** Jupyter notebooks detailing the statistical analysis and model selection process.

---

## 🛠️ Technology Stack

**Backend & Machine Learning:**
* Python
* Flask (Web Server)
* Scikit-Learn (Model Training & Preprocessing)
* Pandas & NumPy (Data Manipulation)
* CatBoost / XGBoost (Advanced Regression Modeling)

**Frontend:**
* HTML5
* Tailwind CSS (via CDN)
* Vanilla JavaScript

---

## 📂 Project Structure

The repository follows a professional, modular structure for scalability and maintainability:

```text
student-performance-indicator-main/
├── artifacts/                # Contains generated models and preprocessors (model.pkl, preprocessor.pkl)
├── notebook/                 # Jupyter notebooks for EDA and Model Training
│   ├── data/                 # Raw dataset (stud.csv)
│   ├── 1 . EDA STUDENT PERFORMANCE .ipynb
│   └── 2. MODEL TRAINING.ipynb
├── src/                      # Core source code for the ML pipeline
│   ├── components/           # Data ingestion, transformation, and model trainer modules
│   ├── pipeline/             # Prediction and training pipeline scripts
│   ├── exception.py          # Custom exception handling
│   ├── logger.py             # Application logging configuration
│   └── utils.py              # Helper functions
├── templates/                # Frontend HTML files (index.html, home.html)
├── app.py                    # Flask application entry point
├── requirements.txt          # Python package dependencies
└── setup.py                  # Package configuration for the src module
```
## ⚙️ Installation & Setup

Follow these steps to run the project locally on your machine.

**1. Clone the repository**
```bash
git clone https://github.com/akshitgarg08/student-performance-indicator.git
cd student-performance-indicator-main
```

**2. Create a Virtual Environment (Recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

**3. Install Dependencies**
Install all required Python packages listed in the `requirements.txt` file.
```bash
pip install -r requirements.txt
```

**4. Run the Application**
Start the Flask server.
```bash
python app.py
```

**5. Access the Web App**
Open your web browser and navigate to:
```text
http://127.0.0.1:5000/
```

---

## 📊 Model Training

If you wish to retrain the model with new data:
1. Replace or update the dataset located in `notebook/data/stud.csv`.
2. Execute the `data_ingestion.py` component to trigger the training pipeline.
3. The new model and preprocessor will be automatically saved in the `artifacts/` directory as `model.pkl` and `preprocessor.pkl`.
