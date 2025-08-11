# 📂 Dataset Folder

This folder contains all the datasets used in the **Machine Learning Course** for practical exercises and coding demonstrations.

## 📑 Overview
The datasets in this folder are utilized for:
- Data analysis
- Visualization (Matplotlib, Seaborn)
- Preprocessing (handling missing values, train-test split, standardization)
- Machine Learning model training and evaluation

## 📜 Contents
| File Name | Description | Format |
|-----------|-------------|--------|
| `BostonHousing.csv` | Housing dataset used for regression analysis and feature scaling | CSV |
| `credit_data.csv` | Dataset containing customer credit information for classification tasks | CSV |
| `credit.csv` | Credit-related dataset for preprocessing and predictive modeling | CSV |
| `diabetes.csv` | Diabetes dataset for classification and data preprocessing | CSV |
| `diabetes.xlsx` | Excel version of the diabetes dataset for spreadsheet-based loading | XLSX |
| `iris_data.csv` | Classic Iris flower dataset for classification and visualization | CSV |
| `Placement_Dataset.csv` | Dataset containing student placement records for classification and analysis | CSV |
| `Screen Time Data.csv` | Dataset tracking daily screen time for time-series or behavioral analysis | CSV |

## 📌 Usage Example
Load a dataset in your Jupyter Notebook or Python script:

```python
import pandas as pd

df = pd.read_csv("dataset/BostonHousing.csv")
print(df.head())
