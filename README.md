# CSA_project


Heart Disease Analysis Project
==============================

Overview
--------
Heart disease is one of the leading causes of death worldwide. Early detection and accurate diagnosis are critical for improving patient outcomes. This project applies machine learning techniques to analyze clinical and demographic attributes and predict the presence of heart disease.

Dataset
-------
- Records: 299 patients
- Features: 19 attributes
- Target Variable: Disease (0 = Disease Present, 1 = No Disease)
- Key Features:
  * Age (29–77 years, mean ~54.5)
  * Sex (~67% male, ~33% female)
  * Resting Blood Pressure (94–200 mmHg, mean ~131.7)
  * Serum Cholesterol (126–564 mg/dl, mean ~247.1)
  * Maximum Heart Rate (71–202 bpm, mean ~149.5)
  * ST Depression by Exercise (0–6.2, mean ~1.05)
  * Number of Vessels via Fluoroscopy (0–3, mean ~0.67)
  * Thalassemia defects (reversible ~38%, fixed ~6%)

The dataset is complete (no missing values) and balanced (~46% disease vs. ~54% no disease).

Project Structure
-----------------
Heart_diseases.ipynb   - Jupyter Notebook with analysis and modeling
requirements.txt       - Python dependencies
Dockerfile             - Container setup
readme.txt             - Project documentation
data/                  - Dataset (CSV file)

Setup Instructions
------------------
1. Clone the repository:
   git clone https://github.com/your-username/heart-disease-analysis.git
   cd heart-disease-analysis

2. Install dependencies:
   pip install -r requirements.txt

3. Run Jupyter Notebook:
   jupyter notebook
   Open Heart_diseases.ipynb in your browser.

Run with Docker
---------------
1. Build the image:
   docker build -t heart-disease-analysis .

2. Run the container:
   docker run -p 8888:8888 heart-disease-analysis

3. Copy the Jupyter Notebook URL from the terminal and open it in your browser.

Analysis Highlights
-------------------
- Exploratory Data Analysis (EDA): Distribution plots, correlation heatmaps
- Feature Importance: Top predictors include max heart rate, vessel count, ST depression, age, and resting BP
- Model: Random Forest Classifier
- Accuracy: ~83%
- ROC Curve: AUC = 0.93 (excellent discriminatory ability)
- Confusion Matrix: Balanced sensitivity and specificity

Results
-------
- Exercise-related and imaging features are the strongest predictors of heart disease.
- The Random Forest model achieved 83% accuracy and strong recall across both classes.
- ROC AUC of 0.93 confirms excellent predictive capability.

Future Work
-----------
- Experiment with other algorithms (Logistic Regression, XGBoost, Neural Networks).
- Hyperparameter tuning for improved accuracy.
- Integration with clinical decision support systems.

