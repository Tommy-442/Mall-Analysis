# Mall-Analysis
# Customer Segmentation Project (Databricks)

## 📌 Project Overview
This project demonstrates a complete data engineering workflow using Databricks, Pandas, and PySpark.  
As a junior data engineer, my goal was to:

1. Load raw customer segmentation data into Databricks
   
2. Clean and transform the dataset using Pandas and PySpark
   
3. Save the cleaned and enriched data for further analytics

## 🛠️ Project Workflow
### 1. Load Dataset

- Dataset
  
- Upload CSV to Databricks → `/FileStore/tables/Mall_Customers.csv`
  
- Load into:

- Pandas DataFrame → `pd.read_csv()`
    
- Spark DataFrame → `spark.read.csv()`


### 2. Data Cleaning
- Drop rows with missing values

- Rename columns for consistency:

   - `Annual Income (k$)` → `Income`

  - `Spending Score (1-100)` → `SpendingScore`

- Standardize the gender column to lowercase

### 3. Data Transformation

- Create `IncomeLevel` column:

  - Low → Income < 40  

  - Medium → 40 ≤ Income < 70  

  - High → Income ≥ 70  

- Generate `FullName` column to simulate unique customer IDs

### 4. Data Enrichment

- Add derived features for analytics (e.g., Income Level, Full Name)
