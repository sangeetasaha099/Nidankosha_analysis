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

## Key Findings

- The majority of patients fall within the 41–60 years age group
- Significant borderline or high-risk cholesterol and glucose levels
- Higher cardiovascular and diabetic risk observed in males

