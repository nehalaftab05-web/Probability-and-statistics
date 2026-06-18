# Probability-and-statistics
# Glycemic Analytics: A Statistical Analysis of Diabetes Risk Indicators
An interactive data science and predictive analytics application designed to evaluate clinical risk factors associated with diabetes using the Pima Indians Diabetes dataset. This project combines comprehensive exploratory data analysis, mathematical probability modeling, and machine learning to estimate population trends and evaluate patient risk factors.
For a exhaustive dive into the mathematical proofs, full distribution curves, and deep academic evaluations, refer to the accompanying report file: **Glycemic_Analytics_Premium_Report.pdf**.
## 📋 Project Overview & Abstract
This project applies core descriptive, inferential, and predictive statistical workflows to a medical dataset containing **768 patient records** and **9 clinical variables**. The engineering architecture encompasses data quality assessment, statistical distribution modeling, confidence interval estimations, and an interactive prediction engine.
### Key Insights
 * **Class Imbalance:** The baseline data consists of a 65.1% non-diabetic and 34.9% diabetic split.
 * **Primary Biomarker:** Plasma glucose concentration emerges as the strongest linear correlate to diabetic status.
 * **Predictive Capability:** A localized logistic regression model using only **Glucose** and **BMI** as features achieves a **76.6% test-set accuracy**.
 * **Data Integrity Note:** Multiple features contain zero values (e.g., Insulin, Skin Thickness) that clinically indicate missing observations, emphasizing the real-world necessity for statistical preprocessing.
## 🛠 Features & System Architecture
### 1. Interactive Dashboard Interface
Built as a modular web application, the dashboard enables real-time file uploads (diabetes.csv) and dynamic interaction with data visualization layers.
### 2. Exploratory Data Analysis (EDA) Portal
 * **Stratified Visualizations:** Employs outcome-stratified boxplots, right-skewed histograms, and high-contrast pie charts to map variable spreads.
 * **Correlation Heatmaps:** Features a full pairwise linear correlation matrix highlighting feature-to-outcome dependencies.
### 3. Inferential & Probability Engine
 * **Confidence Intervals:** Automatically calculates and marks 95% Confidence Intervals via the standard error formula:
   
 * **Theoretical Overlays:** Demonstrates canonical distribution scenarios against the dataset variables, tracking Normal, Poisson (\lambda=8), Uniform, and Binomial (n=10, p=0.5) models.
### 4. Predictive Live Simulator
Includes an interactive inference block where users adjust parameters (such as Glucose levels and BMI) via sliders to instantly calculate log-odds and output risk probabilities using a underlying Sigmoid threshold curve.
## 📊 Dataset Specifications
The application processes the **Pima Indians Diabetes Database** sourced from Kaggle/UCI.
| Variable | Type | Description |
|---|---|---|
| **Pregnancies** | Integer | Number of times pregnant |
| **Glucose** | Continuous | Plasma glucose concentration (mg/dL) |
| **BloodPressure** | Continuous | Diastolic blood pressure (mm Hg) |
| **SkinThickness** | Continuous | Triceps skin fold thickness (mm) |
| **Insulin** | Continuous | Two-hour serum insulin (mu U/ml) |
| **BMI** | Continuous | Body Mass Index — \text{weight (kg)} / \text{height (m)}^2 |
| **DiabetesPedigreeFunction** | Continuous | Diabetes pedigree function score (family history index) |
| **Age** | Integer | Age in years |
| **Outcome** | Binary | Target class: 0 = Non-Diabetic, 1 = Diabetic |
## 📉 Statistical Performance & Modeling
### Logistic Regression Model
The predictive engine runs on an interpretable logistic regression pipeline utilizing the two most statistically significant predictors: **Glucose** and **BMI**.
#### Model Equation:
#### Coefficient Breakdown:
 * **Intercept (-7.7309):** Baseline log-odds when both variables equal zero.
 * **Glucose (0.0348):** Each 1 \text{ mg/dL} increase in plasma glucose raises the log-odds of a positive diagnosis by 0.0348.
 * **BMI (0.0842):** Each 1-unit increase in BMI scale metrics raises the log-odds of a positive diagnosis by 0.0842.
### Evaluation Metrics (Test-Set)
| Metric | Value | Technical Interpretation |
|---|---|---|
| **Accuracy** | 76.6% | Overall share of correct predictions across both classes. |
| **Precision (Diabetic)** | 69.4% | Proportion of flagged positive cases that were genuinely diabetic. |
| **Recall (Diabetic)** | 61.8% | Sensitivity metric; percentage of actual diabetic patients successfully caught. |
| **F1-Score (Diabetic)** | 65.4% | Balanced harmonic mean optimizing both precision and recall margins. |
#### Confusion Matrix Matrix:
 * **True Negatives (Non-Diabetic):** 84
 * **False Positives:** 15
 * **False Negatives:** 21
 * **True Positives (Diabetic):** 34
## 🚀 Future Optimizations & Roadmap
To expand upon the statistical foundation documented in Glycemic_Analytics_Premium_Report.pdf, the following development iterations are recommended:
 1. **Missing Data Imputation:** Move beyond zero-value omission by comparing predictive performance against MICE or K-Nearest Neighbors imputation strategies.
 2. **Classification Threshold Optimization:** Implement ROC-AUC analysis to shift the default 0.5 classification threshold down, prioritizing higher recall metrics to minimize clinically missed diabetic cases.
 3. **Advanced Classifiers:** Introduce non-linear ensembles (e.g., Random Forests or Gradient Boosted Trees) to evaluate high-dimensional relationships across variables like Age and Diabetes Pedigree Function.
## 👥 Core Project Contributors
 * **Hadia Awan** – Group Leader
 * **M Saim Naveed** – Group Member
 * **Ahmed Naeem** – Group Member
 * **Hamna Faisal** – Group Member
 * **Nehal Aftab** – Group Member
> **Note:** For specific code execution architectures, package dependencies (streamlit, pandas, numpy, statsmodels, matplotlib, seaborn), and step-by-step mathematical proofs of the utilized probability density functions, reference the comprehensive **Glycemic_Analytics_Premium_Report.pdf** document.
>
