# Gold Recovery Prediction in a Mining Process

## Project Overview

This project focuses on developing machine learning models to predict gold recovery rates during different stages of an industrial gold extraction process. Accurate recovery predictions allow mining companies to monitor production performance, identify inefficiencies, and optimize operational decisions without requiring measurements that may be unavailable in real time.

The project involves extensive data preprocessing, exploratory data analysis, feature selection, and regression modeling to estimate both **rougher recovery** and **final recovery** based on process parameters collected throughout the extraction and purification stages.

---

## Business Problem

Mining companies rely on recovery metrics to evaluate the efficiency of their extraction processes. However, recovery values are not always immediately available, and some key variables may be missing from production datasets.

The objective of this project is to build predictive models capable of estimating recovery values using the available operational data, enabling more effective monitoring and optimization of the production process.

---

## Dataset

The dataset contains information collected from multiple stages of the gold extraction process, including:

* Raw material characteristics
* Flotation process parameters
* Primary and secondary purification stages
* Concentrations of gold, silver, and lead
* Process feed particle sizes
* Recovery measurements

The project includes separate training and test datasets, with some target-related variables intentionally omitted from the test set.

---

## Project Workflow

### 1. Data Exploration

* Examined dataset structure and feature availability.
* Verified the recovery calculation using the provided formula.
* Identified missing variables in the test dataset.
* Analyzed distributions of process variables and mineral concentrations.

### 2. Data Preprocessing

* Removed observations containing invalid recovery values.
* Investigated missing values and physically impossible zero concentrations.
* Imputed missing feature values using forward-fill methods.
* Retained only the features available in both training and test datasets.
* Verified consistency between training and test distributions.

### 3. Feature Analysis

* Analyzed gold, silver, and lead concentrations across processing stages.
* Evaluated particle size distributions in flotation and purification processes.
* Investigated outliers and measurement inconsistencies.

### 4. Model Development

Several regression models were evaluated to predict:

* Rougher Recovery
* Final Recovery

Model performance was assessed using the **Symmetric Mean Absolute Percentage Error (sMAPE)** metric, which is commonly used for evaluating prediction accuracy in industrial forecasting problems.

---

## Key Findings

* Gold concentration increases progressively throughout the extraction process.
* Silver concentration decreases as purification advances.
* Lead concentration remains relatively stable across stages.
* Numerous zero values were identified and determined to be physically unrealistic, indicating potential measurement or recording errors.
* Training and test datasets exhibited similar feature distributions, supporting the validity of the predictive modeling approach.
* Proper handling of missing values and invalid observations significantly improved dataset quality.

---

## Best Model

After evaluating multiple regression approaches, the **Random Forest Regressor** achieved the best predictive performance for both recovery targets.

Although it required greater computational resources than alternative models, it consistently produced the most accurate recovery estimates.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* SciPy
* Jupyter Notebook

---

## Skills Demonstrated

* Data Cleaning and Preprocessing
* Exploratory Data Analysis (EDA)
* Feature Engineering
* Industrial Process Analytics
* Regression Modeling
* Model Evaluation with sMAPE
* Missing Value Handling
* Outlier Detection
* Business-Oriented Data Science

---

## Business Impact

The resulting model provides a practical solution for estimating recovery values when direct measurements are unavailable. This enables more effective process monitoring, supports operational decision-making, and helps identify opportunities for improving extraction efficiency.

By combining domain knowledge, data preprocessing, and machine learning techniques, this project demonstrates how predictive analytics can generate value in industrial and manufacturing environments.

---

## Conclusion

This project successfully developed a predictive system for estimating rougher and final gold recovery rates using operational process data. Through rigorous data cleaning, feature selection, and model evaluation, a robust machine learning solution was created that can support process optimization and operational efficiency in the mining industry.

The results highlight the importance of data quality, appropriate preprocessing techniques, and model selection when building predictive systems for real-world industrial applications.
