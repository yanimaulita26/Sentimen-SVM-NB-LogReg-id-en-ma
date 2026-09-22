# IJAIN: SVM, Naive Bayes, and Logistic Regression for Trilingual Sentiment Classification

Reproducibility package for the IJAIN proceedings paper's 3-classifier comparison (Support Vector Machine, Naive Bayes, and Logistic Regression) on trilingual (Indonesian, English, Malay) binary sentiment classification.

## Structure

```
├── data/          7 CSV files, 2-class (positive/negative) aligned dataset
├── code/
│   └── run_ijain_svm_nb_logreg.py    Trains/evaluates SVM, Naive Bayes, Logistic Regression. CPU only.
└── results/
    └── hasil_IJAIN_SVM_NB_LogReg.json
```

## How to Reproduce

```bash
cd code
pip install pandas scikit-learn numpy
python run_ijain_svm_nb_logreg.py
```

## Verification Log

This script was independently re-executed from a clean environment. All 9 output values (3 classifiers × 3 languages: accuracy and F1-macro) were checked against the values reported in the IJAIN paper and matched to 4 decimal places. SVM and Naive Bayes values were additionally cross-checked against the companion SVM+Naive Bayes-only package and found to be identical, confirming consistency across both experiment scopes.

## Results Summary

| Language | Model | Accuracy | F1-Macro |
|---|---|---|---|
| Indonesian | SVM | 0.8849 | 0.8847 |
| Indonesian | Logistic Regression | 0.8816 | 0.8815 |
| Indonesian | Naive Bayes | 0.8454 | 0.8449 |
| English | Naive Bayes | 0.8717 | 0.8716 |
| English | Logistic Regression | 0.8651 | 0.8650 |
| English | SVM | 0.8618 | 0.8612 |
| Malay | SVM | 0.7537 | 0.6897 |
| Malay | Logistic Regression | 0.7510 | 0.6852 |
| Malay | Naive Bayes | 0.7211 | 0.6149 |

## Companion Repository

A related package covers the narrower SVM + Naive Bayes-only comparison. It is available at:
https://github.com/yanimaulita26/Sentimen-SVM-NB-id-en-ma

## This Repository

https://github.com/yanimaulita26/Sentimen-SVM-NB-LogReg-id-en-ma

