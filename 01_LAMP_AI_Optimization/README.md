# Synthetic LAMP Data Analysis and Machine Learning

## Project Overview

This educational project demonstrates data analysis, visualization,
classification, and cross-validation using a synthetic LAMP dataset.

## Dataset

- Number of records: 240
- Number of columns: 7
- Data source: Artificially generated data
- Experimental validation: None

## Predictive Features

- Temperature_C
- Mg_mM
- Primer_GC_percent

## Target Variable

Result: Synthetic Positive or Negative classification.

## Models Evaluated

- Logistic Regression
- Random Forest
- Polynomial Logistic Regression
- Majority-class baseline

## Evaluation Methods

- Train-test split
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Stratified five-fold cross-validation

## Main Cross-Validation Results

Polynomial Logistic Regression achieved the highest mean ROC-AUC
among the three trained classifiers in this run.

The results are exploratory and based entirely on synthetic data.

## Important Limitations

The target labels were generated using an artificial mathematical
rule. These results do not demonstrate real LAMP assay performance,
BST-SK polymerase activity, diagnostic sensitivity, or optimal
reaction conditions.

The test set was inspected during model comparison. Therefore,
its metrics should not be considered an untouched final evaluation.

## Reproducibility

The synthetic dataset was generated using a fixed random seed.
The saved model was fitted on the training split.

## Future Work

Future work should use experimentally measured and appropriately
documented data, a predefined validation strategy, and independent
experimental validation before making biological conclusions.

## Tools and Technologies

- Python
- Google Colab
- pandas and NumPy for data handling
- Matplotlib for data visualization
- scikit-learn for machine learning and model evaluation
- joblib for model serialization
- Git and GitHub for version control and project documentation

## Project Structure

- `data/`: Synthetic dataset used in the analysis.
- `results/`: Model comparison and cross-validation results.
- `models/`: Saved trained model.
- `figures/`: Data visualization outputs.

## Skills Demonstrated

- Data quality assessment and descriptive statistics
- Exploratory data analysis
- Binary classification and baseline comparison
- Model evaluation using multiple metrics
- Stratified cross-validation
- Reproducible computational workflow
- Scientific documentation and interpretation of limitations
