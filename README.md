# 🧠 Predicting 2-Month Mortality in Seriously Ill Hospital Patients

**A Clinical Decision Support Analysis Using the SUPPORT2 Dataset**

### 📍 By Yong Huang | Final Project, MS in Health Informatics & Analytics

📧 [Yonghuang@usf.edu](mailto:Yonghuang@usf.edu)

---

## 📘 Project Overview

This project explores whether we can predict 2-month mortality among seriously ill hospitalized patients using the **SUPPORT2** dataset. The goal is to assist clinicians in early decision-making and to enhance communication between healthcare providers, patients, and their families.

The SUPPORT study (Study to Understand Prognoses and Preferences for Outcomes and Risks of Treatments) collected comprehensive clinical and demographic data on over 9,000 patients across the U.S. This project applies data science techniques to assess the feasibility of predicting early mortality using variables available near the time of admission.

---

## 🎯 Problem Statement

**Can we use patient data at hospital admission to predict death within 2 months?**
Early identification of at-risk patients allows for timely conversations about care preferences and medical interventions.

---

## 🎯 Target Variable

* **Death2m**: A binary variable created for this project indicating whether the patient died within 2 months of hospital admission.

---

## 🗂️ Dataset Description

* **Source**: SUPPORT2 dataset (SAS Studio library)
* **Rows**: 9,105 patients
* **Features**: 40 variables

  * **Categorical**: 11 (including disease type, income, race, sex)
  * **Binary**: 5 (sex, death, diabetes, dementia, etc.)
  * **Continuous**: 29 (lab results, vitals, hospital metrics, etc.)

---

## 🔍 Data Exploration & Preparation

### Data Challenges Addressed:

* **Skewed Distributions**: Applied log10 transformations to positively skewed variables (e.g., charges, bilirubin, BUN, etc.).
* **Missing Values**:

  * Categorical variables like income and race assigned a “Missing” category.
  * Continuous variables were imputed using a combination of mean, median, and decision tree models (e.g., scoma).
* **Feature Engineering**:

  * Created new target variable `death2m` from multiple time/status fields.
  * Removed variables prone to data leakage (e.g., total charges, length of stay, etc.).
  * Selected medically relevant input variables while avoiding future knowledge.

---

## 🛠️ Modeling Approach

### Technique:

* **Decision Tree Modeling** using SAS Enterprise Miner

### Rationale:

* Handles both categorical and continuous variables
* Easy interpretability for healthcare stakeholders
* Robust to missing values and variable scaling

### Input Variables Included:

* Demographics: age, sex, race, income, education
* Disease Characteristics: dzgroup, ca, diabetes, dementia, num.co
* Clinical Vitals & Labs: scoma, meanbp, alb, bili, crea, sod, ph, glucose, wblc, hrt, resp, temp, pafi, bun, urine

### Evaluation:

* Tried multiple tree depths and pruning methods
* Compared performance across iterations  
* Added principal component analysis to optimize model accuracy

---

## 📈 Outcome & Value

* The decision tree model provided strong interpretability and reasonable predictive power.
* Demonstrated how structured hospital admission data can help predict short-term mortality.
* Supports the broader goal of integrating data science into clinical decision support.

---

## 📚 Skills Demonstrated

* Data Cleaning & Imputation
* Feature Engineering
* Decision Tree Modeling
* SAS Programming
* Principal Component Analysis
* Data Visualization (SAS Graphs)

---

## 📁 Files in This Repository


| File                               | Description                                 |
| ---------------------------------- | ------------------------------------------- |
| `README.md`                        | Project summary                             |
| `Process Flow_Project Support.pdf` | Process flow diagram                        |
| `support2SAScode`                  | SAS code used for data preparation/analysis |
| `project report.pdf`               | Final report (school project)  |


---

---

## 👩‍⚕️ About the Author

Yong Huang holds a Doctor of Pharmacy (PharmD) degree and is completing a Master's in Health Informatics & Analytics. With clinical and data experience, Yong is passionate about building data-driven tools that improve patient care and provider decision-making.

