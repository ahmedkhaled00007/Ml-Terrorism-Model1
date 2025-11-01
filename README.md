# Terrorism Attack Success Prediction

This project uses machine learning to analyze and predict whether a terrorist attack is likely to be successful based on the Global Terrorism Database (GTD).

We build a complete ML pipeline that includes data preprocessing, feature selection, model training, evaluation, and interpretation of results.

---

## Dataset

- Source: [Global Terrorism Database (GTD)](https://www.kaggle.com/datasets/START-UMD/gtd)
- Shape: ~180,000 rows, 135+ columns
- Target Variable: `success` (1 = successful attack, 0 = failed attempt)

---

## Project Workflow

1. Data Cleaning  
   - Replace placeholders like `Unknown`, `-99`, `9` with `NaN`  
   - Drop columns with excessive missing values

2. Exploratory Data Analysis (EDA)  
   - Analyze column types, missing values, and data distribution  
   - Understand imbalance in the target variable

3. Preprocessing  
   - Use `Pipeline` and `ColumnTransformer` to process numerical and categorical data  
   - Handle missing values, scaling, and encoding

4. Modeling  
   - Train and compare multiple models:  
     - Logistic Regression  
     - Random Forest  
     - Gradient Boosting  
     - AdaBoost  
   - Use evaluation metrics to compare performance

5. Evaluation  
   - Confusion Matrix  
   - Accuracy, Precision, Recall, F1-Score  
   - ROC Curve & AUC Score

---

## Best Model

- Overall Best (based on metrics): `AdaBoost`
- Most Practical (real-world relevance): `RandomForestClassifier`  
  - Higher recall for class 1 (successful attacks)  
  - Better for minimizing false negatives in critical situations

---

## Results (Random Forest)

| Metric      | Score   |
|-------------|---------|
| Accuracy    | 91.5%   |
| Precision   | 92.8%   |
| Recall      | 98.0%   |
| F1 Score    | 95.3%   |

---

## Conclusion

While AdaBoost showed strong general performance, Random Forest is more suitable for this terrorism dataset, where detecting successful attacks is a higher priority than overall accuracy.

---

## Requirements

```bash
pandas
numpy
scikit-learn
matplotlib
seaborn
imblearn (for SMOTE)
```

To install all dependencies:
```bash
pip install -r requirements.txt
```

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/yourusername/terrorism-attack-prediction.git
cd terrorism-attack-prediction
```

2. Run the Jupyter notebook:
```bash
jupyter notebook Terrorism.ipynb
```

---

## License

This project is open-source and available under the MIT License.

---

## Author

**Ahmed Khaled**  
Data Scientist | Data Analyst  
[LinkedIn](www.linkedin.com/in/ahmed-khaled-003845303) 
