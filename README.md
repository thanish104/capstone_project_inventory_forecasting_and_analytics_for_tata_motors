# Inventory Forecasting and Analytics for Tata Motors – Case Study (Dealership)

<small>
This repository contains the complete project for Inventory Forecasting and Analytics for Tata Motors Company – A Case Study for One Dealership, as part of the Capstone Project requirements for REVA Academy for Corporate Excellence (RACE).

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **📄 Project Overview**

<small>
Tata Motors, a leader in the automotive sector, operates within a complex supply chain with varied demand patterns and inventory challenges. This project leverages advanced analytics and machine learning to optimize spare parts forecasting for a dealership, aiming to minimize costs, avoid stockouts/excess inventory, and enhance customer satisfaction.
</small>

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **🎯 Objectives**

1. Build an inventory analytics ETL and dimensional data model

2. Automate data ingestion and movement using Azure Data Factory

3. Develop dashboards for historic and predictive analytics using Streamlit

4. Create robust demand forecasting models for spare parts (next 2-3 months)

5. Recommend actionable insights to business stakeholders

6. Calculate and report cost savings from best-fit models across inventory segments

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## **🏗️ Project Structure**

| Folder / File                                      | Description                                                        |
|----------------------------------------------------|--------------------------------------------------------------------|
| `data/`                                            | Contains preprocessed and raw datasets (CSV, Excel)                |
|`preprocessed_data/`                                | Contains the segmented data and pivot data
| `notebooks/`                                       | Jupyter/DB notebooks for analysis, EDA, and modeling            |
| `scripts/`                                         | SQL scripts for Snowflake warehousing layers             |
| `architecture/`                             | Project architecture and flow diagrams                             |
| `final_report/BA11_Capstone1-Project-Final-Report.docx` | Final project report with background, methodology, and results |
| `proposal/BA_Capstone-Project-Proposal.docx`       | Project proposal document                                          |
| `ppt/BA11_Capstone1-Project_Final-PPT.pptx`        | Final capstone presentation                                        |
| `model_code/Final_Model.html`                      | Main Python model implementation for forecasting                   |
| `model_outputs/performance_metric.csv`             | Output metrics (RMSE, MAE, R²) of all forecasting models           |
| `README.md`                                        | This file                                                          |

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ⚙️ Technical Workflow  

### 📥 Data Collection & Ingestion  
- Transactional data collected (**2022-01 to 2024-08**) from Tata Motors dealership.  
- Ingestion via **Azure Data Factory** to **Snowflake Cloud DWH** (see architecture diagrams).  

### 🗄️ Data Warehousing & Modeling  
- Multi-layered architecture: *Landing → Cleansed → History → Core → Presentation*.  
- **Star schema** with fact and dimension tables for KPIs, parts, dealer, time, and others.  

### 📊 Segmentation  
- **ABC Analysis** → Based on inventory value contribution.  
- **XYZ Classification** → Based on demand variability (*Coefficient of Variation*).  
- **FSN Classification** → Based on frequency of sales/movement.  

### 🤖 Machine Learning Models  
- Data segmented into **AFX, AFY, AFZ, BFX**, etc. (combining ABC, XYZ, FSN).  
- Forecasting models implemented:  
  - XGBoost Regression  
  - SARIMA / Auto ARIMA  
  - Holt-Winters Exponential Smoothing  
- **Model evaluation metrics**: MAPE, RMSE, MAE, R².  

### 📈 Visualization & Dashboards  
- **Streamlit Dashboard** for:  
  - Historic trends  
  - Inventory health  
  - Demand predictions  
  - Recommendations  

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 🚀 Key Results  

| Model         | RMSE   | MAE   | R²    |
|---------------|--------|-------|-------|
| XGBoost       | 156.49 | 14.45 | 0.84  |
| SARIMA        | 87.57  | 8.32  | 0.96  |
| Holt-Winters  | 129.82 | 14.71 | 0.89  |

✅ **SARIMA achieved the best accuracy for 3-month forecasts.**  

📦 Effective segmentation enables **targeted inventory control** for each product type.  

📊 Dashboard provides **actionable insights** for procurement and inventory managers.  

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 📂 How to Use  
- Clone the repo and review the folders: **`final_report/`**, **`notebooks/`**, **`scripts/`**, and **`model_code/`** for complete end-to-end context.  
- See architecture diagrams in **`images/architecture/`**.  
- Jupyter notebooks and scripts are **modular and well-commented**.  
- Forecast model outputs are available in **`model_outputs/`**.  

---

## 📚 References  
- Includes 15+ key journal and industry sources; full details are provided in the final report.  
- Notable: *Soni et al., "Inventory Forecasting Model Using Genetic Programming and Holt-Winter's Exponential Smoothing Method"* (IEEE, 2017).  

---

## 🙏 Acknowledgements  
- Project completed as part of the **Master of Science in Business Analytics** program, REVA University.  
- Guidance: **Dr. Jay Bharatheesh Simha**.  
- Industry support from **Tata Motors dealership stakeholders**.  

---

## 📝 License  
This project is submitted for **academic and research purposes**.  
All rights reserved by the author and institution.  

📌 For detailed process, results, and code, review the attached files and documentation in each folder/path.  


