# Santander Customer Satisfaction - Decision Tree Classification

## Overview
This project trains a Decision Tree classifier to predict customer satisfaction using the Santander dataset. It generates predictions, probabilities, and classification reports for both training and test data, and saves all outputs to a single Excel file.

## Dataset
The train and test datasets are not included in this repository due to file size. Download them from Kaggle and place them in the data/ folder:
https://www.kaggle.com/competitions/santander-customer-satisfaction/data

- `train.csv` — 370 anonymized numeric features and a `TARGET` column (~76,000 rows)
- `test.csv` — 370 anonymized numeric features, no `TARGET` column (~75,000 rows)

The target variable `TARGET` is binary: 0 = satisfied, 1 = unsatisfied. Around 96% of training customers are satisfied, so accuracy alone is not a reliable metric. Focus on precision, recall, and F1-score for class 1 in the classification report.

## Project Structure
```
project/
│
├─ data/
│  ├─ train.csv               # Training dataset (not included — download from Kaggle)
│  ├─ test.csv                # Test dataset (not included — download from Kaggle)
│  └─ Output_Santander.xlsx   # Predictions and reports (generated)
│
├─ santander_decision_tree.py  # Main Python script
├─ .gitignore
└─ README.md


## Requirements
- Python 3.8+
- Libraries: `pandas`, `numpy`, `scikit-learn`, `openpyxl`

Install dependencies:
```
pip install pandas numpy scikit-learn openpyxl
```

## Usage
1. Download `train.csv` and `test.csv` from Kaggle and place them in the `data/` folder
   - `train.csv` must include a `TARGET` column
   - `test.csv` may or may not include `TARGET`
2. Run the script:
```
python santander_decision_tree.py
```
3. Output saved in `data/Output_Santander.xlsx` with separate sheets:
   - `Train_Predictions` — predictions and probabilities for the training set
   - `Test_Predictions` — predictions and probabilities for the test set
   - `Train_Report` — classification report for the training set (if target exists)
   - `Test_Report` — classification report for the test set (if target exists)

## Notes
- If the `TARGET` column is missing or empty, training and predictions are skipped for that dataset
- The Kaggle test file has no `TARGET` column, so `Test_Report` will not be generated
- Predictions include both a hard class label and class probabilities (`Prob_Class_0`, `Prob_Class_1`)
- Kaggle test file does not include TARGET, so Test_Report will not be generated
- Predictions include:
  - Class label
  - Prob_Class_0
  - Prob_Class_1
