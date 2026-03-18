Santander Customer Satisfaction - Decision Tree Classification

This project trains a Decision Tree classifier to predict customer satisfaction using the Santander dataset. It generates predictions, probabilities, and classification reports for both training and test data, and saves all outputs to a single Excel file.

Project Structure
project/
│
├─ data/
│  ├─ train.csv       # Training dataset (not included in Git)
│  ├─ test.csv        # Test dataset (not included in Git)
│  └─ Output_Santander.xlsx  # Predictions and reports (generated)
│
├─ santander_decision_tree.py  # Main Python script
└─ README.md

Requirements
Python 3.8+
pandas
numpy
scikit-learn
openpyxl

Install dependencies with: pip install pandas numpy scikit-learn openpyxl

Usage
1. Place your train.csv and test.csv files in the data/ folder.
train.csv must include a TARGET column.
test.csv may or may not include TARGET.
2. Run the script: python santander_decision_tree.py
3. Output:
Predictions and probabilities for train/test sets
Classification reports (if target exists)
All saved in data/Output_Santander.xlsx with separate sheets:
1. Train_Predictions
2. Test_Predictions
3. Train_Report (if available)
4. Test_Report (if available)

Notes
If the TARGET column is missing or empty, training and predictions are skipped for that dataset.