# Santander Customer Satisfaction - Decision Tree Classification

## Overview
This project trains a Decision Tree classifier to predict customer satisfaction using the Santander dataset. It generates predictions, probabilities, and classification reports for both training and test data, and saves all outputs to a single Excel file.

## Project Structure
```
project/
│
├─ data/
│  ├─ train.csv               # Training dataset
│  ├─ test.csv                # Test dataset
│  └─ Output_Santander.xlsx   # Predictions and reports (generated)
│
├─ Santander Customer Satisfaction.ipynb  # Main Python script
└─ README.md
```

## Requirements
- Python 3.8+  
- Libraries: `pandas`, `numpy`, `scikit-learn`, `openpyxl`  

Install dependencies:
```
pip install pandas numpy scikit-learn openpyxl
```

## Usage
1. Place your `train.csv` and `test.csv` files in the `data/` folder  
   - `train.csv` must include a `TARGET` column  
   - `test.csv` may or may not include `TARGET`  

2. Run the script:  
```
Santander Customer Satisfaction.ipynb
```

3. Output saved in `data/Output_Santander.xlsx` with separate sheets:  
   - `Train_Predictions` – Predictions and probabilities for training set  
   - `Test_Predictions` – Predictions and probabilities for test set  
   - `Train_Report` – Classification report for training set (if target exists)  
   - `Test_Report` – Classification report for test set (if target exists)  

## Notes
- If the `TARGET` column is missing or empty, training and predictions are skipped for that dataset  
