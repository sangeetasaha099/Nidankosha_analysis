# 🩺 NidaanKosha Dataset Analysis

## Project Overview

This project provides a comprehensive exploratory analysis of the **NidaanKosha-100k-V1.0** dataset, a large collection of diagnostic test results from patients across India. The focus is primarily on assessing risk factors associated with cardiovascular diseases and diabetes.

## Dataset Source

- **Dataset Name:** NidaanKosha-100k-V1.0  
- **Provider:** Eka Care  
- **Source:** [Hugging Face Dataset Link](https://huggingface.co/datasets/ekacare/NidaanKosha-100k-V1.0)

## Objective

- Analyse demographic patterns (age, gender)
- Evaluate diagnostic trends (cholesterol, glucose)
- Identify cardiovascular and diabetic risk factors
- Generate actionable insights for public health and clinical decision-making

## Project Workflow

- **Data Acquisition**
  - Downloaded dataset from Hugging Face

- **Data Preprocessing**
  - Cleaned and formatted relevant columns (age, gender, test_name, values)

- **Exploratory Data Analysis (EDA)**
  - Analysed age and gender distributions
  - Examined cholesterol and glucose level distributions
  - Calculated lipid ratios for cardiovascular risk assessment
  - Classified risk categories

- **Visualization**
  - Generated heatmaps for age-gender risk profiles
  - Developed pie and bar charts for risk level summaries

- **Reporting**
  - Compiled analysis and insights into a formal report

## Technologies Used

- Python (pandas, numpy, matplotlib, seaborn)
- Jupyter Notebook
- Hugging Face datasets
- Markdown

---

# 📊 Detailed Analysis & Insights

**Diagnostic test analysis of ~6.8M patient records from across India** — provided by Eka Care, sourced via [Hugging Face](https://huggingface.co/datasets/ekacare/NidaanKosha-100k-V1.0).

Focused on **cardiac health** (cholesterol) and **diabetes risk** (fasting glucose) across a 100k-patient sample.

---

## 📋 Dataset Fields

| Field | Description |
|---|---|
| `document_id` | Unique identifier for the document |
| `age` / `gender` | Patient demographics |
| `test_name` | Name of the medical test conducted |
| `display_ranges` | Reference ranges for the test results |
| `value` / `unit` | Result and measurement unit |
| `specimen` | Type of specimen analysed (e.g. blood) |
| `loinc` | LOINC code associated with the test |

---

## 👥 Patient Demographics

<details open>
<summary><b>Age & Gender Distribution</b> — click to collapse</summary>
<br>

Patients range from **17 to 105 years**, with the majority falling between **30 and 65**. Of the 100,000 patients, **42% are female** and **58% are male**.

<img src="assets/charts/age_distribution.png" width="49%"> <img src="assets/charts/gender_distribution.png" width="49%">

**Age groups used throughout this analysis:**
- `13–20 yrs` — Teens & Young Adults
- `21–40 yrs` — Adults
- `41–60 yrs` — Middle-aged
- `>60 yrs` — Seniors

<img src="assets/charts/age_gender_heatmap.png" width="100%">

Most patients fall in the **41–60** age group, with **males** the largest segment within it.

</details>

---

## ❤️ Cholesterol Analysis

Cholesterol tests (lipid panel) measure **LDL** ("bad"), **HDL** ("good"), **triglycerides**, and **total cholesterol**. High LDL/triglycerides and low HDL raise cardiovascular disease (CVD) risk.

<details>
<summary><b>All Patients — Cholesterol Distributions</b></summary>
<br>

Reference ranges: Total < 200 mg/dL · LDL < 100 mg/dL · HDL > 40 mg/dL · Triglycerides < 149 mg/dL

<img src="assets/charts/total_cholesterol_all.png" width="49%"> <img src="assets/charts/ldl_cholesterol_all.png" width="49%">
<img src="assets/charts/hdl_cholesterol_all.png" width="49%"> <img src="assets/charts/triglycerides_all.png" width="49%">

A significant share of patients sit **at or near the borderline range** — an early warning sign for CVD risk if unaddressed.

</details>

<details>
<summary><b>Patients Below 19 Years</b></summary>
<br>

Reference ranges: Total < 170 mg/dL · LDL < 110 mg/dL · HDL > 45 mg/dL · Triglycerides < 90 mg/dL

<img src="assets/charts/total_cholesterol_under19.png" width="49%"> <img src="assets/charts/ldl_cholesterol_under19.png" width="49%">
<img src="assets/charts/hdl_cholesterol_under19.png" width="49%"> <img src="assets/charts/triglycerides_under19.png" width="49%">

</details>

<details>
<summary><b>Patients Above 19 Years — Male</b></summary>
<br>

Reference ranges: Total < 200 mg/dL · LDL < 100 mg/dL · HDL > 40 mg/dL · Triglycerides < 150 mg/dL

<img src="assets/charts/total_cholesterol_male.png" width="49%"> <img src="assets/charts/ldl_cholesterol_male.png" width="49%">
<img src="assets/charts/hdl_cholesterol_male.png" width="49%"> <img src="assets/charts/triglycerides_male.png" width="49%">

</details>

<details>
<summary><b>Patients Above 19 Years — Female</b></summary>
<br>

Reference ranges: Total < 200 mg/dL · LDL < 100 mg/dL · HDL > 50 mg/dL · Triglycerides < 150 mg/dL

<img src="assets/charts/total_cholesterol_female.png" width="49%"> <img src="assets/charts/ldl_cholesterol_female.png" width="49%">
<img src="assets/charts/hdl_cholesterol_female.png" width="49%"> <img src="assets/charts/triglycerides_female.png" width="49%">

</details>

---

## 📊 Cardiovascular Risk Ratios

<details>
<summary><b>Ratio Definitions & Risk Classification</b></summary>
<br>

| Ratio | Ideal | Acceptable | High Risk |
|---|---|---|---|
| Total Cholesterol / HDL | ≤ 3.5 | 3.5 – 5 | > 5 |
| LDL / HDL | < 2.5 | 2.5 – 3.5 | > 3.5 |
| HDL / LDL | > 1.0 | 0.5 – 1.0 | < 0.5 |
| Triglycerides / HDL | < 2.0 | 2.0 – 3.0 | > 3.0 |

</details>

<details open>
<summary><b>Risk Distribution Across Patients</b></summary>
<br>

<img src="assets/charts/cv_risk_pie.png" width="49%"> <img src="assets/charts/highrisk_by_age_gender.png" width="49%">

**29.2%** of patients are **high-risk**, **39.5%** are acceptable, and **31.3%** are at ideal levels. High-risk counts peak in the **41–60** age group, and are notably higher among **males**.

</details>

---

## 🍬 Fasting Glucose & Diabetes Risk

Fasting glucose (after ≥8 hrs fasting) screens for diabetes/prediabetes and monitors glucose control.

| Category | Range |
|---|---|
| Low Blood Sugar (Hypoglycemia) | < 70 mg/dL |
| Normal | 70–99 mg/dL |
| Prediabetes | 100–125 mg/dL |
| Diabetes | ≥ 126 mg/dL |

<details open>
<summary><b>Glucose Category Breakdown & Diabetic Risk by Demographics</b></summary>
<br>

<img src="assets/charts/fasting_glucose_pie.png" width="100%">

**51.9%** Normal · **24.6%** Prediabetes · **22.8%** Diabetes · **0.8%** Hypoglycemia

<img src="assets/charts/age_diabetic_heatmap.png" width="49%"> <img src="assets/charts/gender_diabetic_heatmap.png" width="49%">

Diabetes prevalence peaks in the **41–60** age group, with a higher overall count among **male** patients.

</details>

---

## 🔑 Key Findings

- The majority of patients fall within the **41–60 years** age group
- A significant proportion of patients show cholesterol and glucose values **at or near borderline thresholds** — an early-warning signal, not yet overt disease
- **~29.2%** of patients fall into the **high cardiovascular risk** category based on lipid ratios
- **~47.4%** of patients are prediabetic or diabetic based on fasting glucose
- Risk is concentrated in the **41–60 age group**, with a **higher prevalence in males** across both cardiac and diabetic markers
- These patterns point to a strong case for **early screening and preventive intervention** at a population level

---

## 📁 Repo Structure

```
Nidankosha_analysis/
├── assets/
│   └── charts/                        # All chart images used above
├── Code/
│   └── nidaankosha-analysis.ipynb     # Analysis notebook
├── nidaankosha_analysis_website/      # Static site version
├── Result/
│   └── Report.pdf                     # Formal report
├── README.md                          # This file
```

---

*Analysis based on the NidaanKosha-100k-V1.0 dataset by Eka Care.*