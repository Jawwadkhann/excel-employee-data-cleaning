# 📊 Excel Data Cleaning & Executive Dashboard Project

## 🚀 Project Overview
This project showcases a complete end-to-end data preparation and business intelligence process using **Microsoft Excel**. The raw, uncleaned dataset contained common corporate data entry errors, such as compound dimensions, formatting inconsistencies, mixed data types, and missing values. The primary objective was to cleanse, transform, and structure this data to build an interactive, analysis-ready reporting dashboard.

---

## 🛠️ Data Cleaning Process & Formulas Used
Here is the step-by-step data pipeline transformation executed on the workforce dataset:

* **Separated Compound Columns**: Utilized the `Text to Columns` feature to cleanly separate mixed strings (e.g., "Department-Region") into two dedicated dimensions: `Department` and `Region`.
* **Standardized Text Dimensions**: Applied a nested `=PROPER(TRIM())` formula across the `First_Name` and `Last_Name` fields to systematically strip out accidental whitespace errors and enforce uniform casing.
* **Repaired Inconsistent Dates**: Converted text-formatted strings in the `Join_Date` column into actual system-recognized dates using the `Text to Columns` date parsing tool.
* **Sanitized Financial Inconsistencies**: Handled text currency symbols (`$`, `,`) and missing markers (`N/A`) within the `Salary` column using `Find & Replace` to force a pure numeric format.
* **Imputed Missing Values**: Resolved null fields in quantitative metrics. Missing records in the `Age` field were imputed using the dataset's baseline **Median Age (30)** to avoid metric distortion, while missing salaries were evaluated against the **Average Salary ($85,000)** metric.

---

## 📈 Executive Dashboard Analysis
After cleansing the data, pivot tables and dynamic charts were generated to surface organizational insights:

### 💰 Average Salary by Department
![Average Salary](Average_salary.png)

### 👥 Employee Headcount by Region
![Employee Headcount](employee_headcount.png)

---

## 📂 Repository Structure
* `Excel Project Dataset.xlsx`: Contains the raw dataset tab, the cleaned dataset pipeline tab, and the executive dashboard calculations.
* `README.md`: Explains the data cleaning logic and hosts the visual portfolio dashboard.
