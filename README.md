# SQL_churn_prediction-

Customer churn prediction using SQL (SQLite) and Python 

An end‑to‑end data science project using **SQL (SQLite)** and **Python** in **Google Colab** to analyze customer behavior and predict churn in a telecom‑style setting.

## Project Overview

The goal of this project is to simulate a telecom customer database, explore churn patterns using SQL, and build machine‑learning models to predict which customers are likely to leave. The work is done entirely in Colab, so it is easy to reproduce and run from any machine.

## Workflow

1. **Data generation (Python)**  
   - Create a synthetic dataset of telecom customers with demographics, contract details, usage, and churn labels.  
   - Introduce realistic patterns such as higher churn for short‑tenure and month‑to‑month customers.

2. **Database creation (SQLite)**  
   - Load the dataset into a SQLite database (`churn.db`) and create a `customers` table.  
   - Treat the project like a small analytics database that can be queried with SQL.

3. **SQL‑based analysis**  
   - Write SQL queries to compute key metrics, such as:  
     - churn rate by contract type  
     - churn rate by tenure group  
     - overall churn percentage and basic KPIs  
   - Use the query results to build bar charts and distributions in Python.

4. **Feature engineering in SQL**  
   - Use SQL `CASE` expressions and simple one‑hot encoding to create a feature table (for example, contract type dummies and average monthly spend).  
   - Export the feature table into pandas for modeling.

5. **Machine‑learning models (scikit‑learn)**  
   - Train **Logistic Regression** and **Random Forest** classifiers to predict churn.  
   - Evaluate models using accuracy, precision, recall, confusion matrix, and a feature‑importance plot.

6. **Insights**  
   - Identify which features (such as contract type, tenure, monthly charges, and support calls) are most important for predicting churn.  
   - Show how SQL and Python can work together in a typical data‑science workflow.
  
##  Repository Contents

- `sql_churn_prediction.ipynb` – main Colab notebook with all steps: data generation, SQL queries, model training, and visualizations.  
- `churn.db` – SQLite database containing the `customers` table, ready for running the same SQL queries locally.  
- `customer_data.csv` – generated customer‑level data used to build the database.  
- `feature_importance.png` – bar chart of the top features driving churn predictions.

## How to run 

1. Open the notebook in **Google Colab** (either via “Open in Colab” from GitHub or by uploading `sql_churn_prediction.ipynb`).  
2. Run the cells from top to bottom.  
   - The notebook automatically regenerates the synthetic data, recreates the SQLite database, executes the SQL analysis, trains the models, and outputs the plots.  
3. Inspect the figures and tables to understand churn drivers and model performance.
