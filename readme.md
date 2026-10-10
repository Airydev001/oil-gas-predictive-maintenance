# Oil & Gas Predictive Maintenance Using Machine Learning

## Project Overview

Unexpected equipment failures in oil and gas facilities can lead to production downtime, increased maintenance costs, and operational risks.

This project explores how machine learning can help identify equipment observations associated with potential pump failure using simulated operating data.

A Random Forest classifier is trained using synthetic sensor readings, and its performance is evaluated using ROC-AUC, accuracy, precision, recall, F1-score, and a confusion matrix.

**Project status:** Learning prototype — synthetic data only.

## Engineering Problem

How can operating parameters such as temperature, vibration, pressure, flow rate, and operating hours be used to investigate potential pump failure risk?

## Objectives

- Generate and analyse synthetic equipment sensor data.
- Develop a binary classification model using Random Forest.
- Evaluate classification performance using ROC curves and AUC.
- Examine false positives and false negatives.
- Explore the trade-off between missed failures and unnecessary maintenance alerts.

## Technology Stack

- Python
- pandas and NumPy
- Matplotlib
- scikit-learn
- Jupyter Notebook

## Methodology

1. Generate synthetic sensor readings.
2. Create illustrative failure labels using a simulated risk formula.
3. Split the data into training and test sets.
4. Train a Random Forest classifier.
5. Generate predicted failure probabilities.
6. Evaluate ROC-AUC and classification metrics.
7. Interpret the results from an engineering and maintenance perspective.

## Initial Results

| Metric | Result |
|---|---:|
| ROC-AUC | 0.802 |
| Test accuracy | 71.5% |
| Failure-class precision | 71.3% |
| Failure-class recall | 73.4% |
| Failure-class F1-score | 72.3% |
| Test observations | 400 |

The confusion matrix was:

| | Predicted normal | Predicted failure |
|---|---:|---:|
| Actual normal | 137 | 60 |
| Actual failure | 54 | 149 |

These results represent a simulated experiment, not validated performance on real oil and gas equipment.

## Business and Engineering Applications

A validated predictive maintenance model could help maintenance teams:

- Prioritize equipment inspections.
- Identify potentially abnormal operating conditions.
- Investigate early indicators of equipment deterioration.
- Support maintenance planning and downtime reduction.

Model predictions should complement established inspection procedures, equipment monitoring, and safety systems.

## Limitations

The dataset is synthetic, and failure labels are generated from an illustrative formula based on the same features used by the model. Consequently, the reported metrics do not demonstrate real-world predictive capability.

Further work would require real, appropriately labelled equipment data, time-aware validation, leakage prevention, threshold analysis, and assessment of the financial and operational costs of incorrect predictions.

## Future Improvements

- Evaluate different classification thresholds.
- Compare Random Forest with Logistic Regression.
- Investigate class imbalance using realistic failure rates.
- Add feature importance analysis.
- Build a maintenance monitoring dashboard.
- Validate the approach on an appropriate real-world dataset.

## Author's Learning Objective

This project is part of my ongoing learning journey in Python, data engineering, and machine learning, with an interest in applying data-driven methods to industrial engineering challenges.