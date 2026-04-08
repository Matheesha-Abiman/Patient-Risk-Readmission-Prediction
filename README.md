# Patient Risk Readmission Prediction

## Project Overview
This project focuses on analyzing and predicting the likelihood of diabetic patients being readmitted to the hospital within 30 days of their discharge. Readmission within an early timeframe (<30 days) often indicates complications, high-risk cases, or an escalation in medical urgency. 

The primary goal of this data analysis framework is to identify critical, complex cases and ultimately generate a custom **VCI (Vulnerability, Complexity, and Intensity) Risk Score**. This score helps stratify patients into Low, Medium, and High-Risk categories to better allocate medical resources and plan patient aftercare.

## Key Phases
1. **Data Cleaning and Preprocessing:** Handled missing variables, dropped sparse columns (such as patient weight), excluded expired records, and handled redundant duplicate rows.
2. **ICD-9 Diagnosis Scrape Integration:** Retrieved fast ICD-9 descriptions for the primary diagnoses to add comprehensive definitions to raw diagnosis codes via web scraping.
3. **Exploratory Data Analysis (EDA):** Generated insights based on various demographic features (age, gender, race) and medical indicators (insulin use vs other meds, medication dose changes, length of initial stay, lab tests). Views are saved in the `Project_Charts` directory.
4. **VCI Risk Level Stratification:** Calculated length of stay, admission acuity, comorbidity, and emergency metrics into a single custom unified VCI score to validate the correlation with actual early patient readmissions.

## Included Files
- `health.ipynb`: The main Jupyer Notebook covering data processing, visualizations, and risk score generation.
- `diabetic_data.csv`: The main source dataset containing patient interactions, demographics, and clinical attributes.
- `IDs_mapping.csv`: A dictionary containing text mapping information to decode internal dataset IDs.
- `final_processed_diabetic_data.csv`: The clean, output dataset enriched with custom diagnostic views and VCI score mappings.
- `Project_Charts/`: Contains visual charts derived from statistical findings in Phase 3 & 4. 

## Requirements
- Python 3.x
- Pandas
- Numpy
- Seaborn
- Matplotlib
- BeautifulSoup4 (for ICD-9 code scraping)
