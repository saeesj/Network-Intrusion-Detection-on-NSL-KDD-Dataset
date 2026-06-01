# Network Intrusion & Cyber Threat Detection System
Multi-class classification of cyberattacks on network traffic data 
using machine learning.

## Overview
Built a threat detection system on the KDD Cup dataset to classify 
network traffic into four attack categories — DoS, Probe, R2L, and 
U2R — and normal traffic. Benchmarked multiple ML algorithms and 
selected the optimal model per attack category.

## Attack Categories
| Label | Type | Description |
|-------|------|-------------|
| 0 | Normal | Legitimate traffic |
| 1 | DoS | Denial of Service |
| 2 | Probe | Surveillance/scanning |
| 3 | R2L | Remote to Local |
| 4 | U2R | User to Root |

## Methodology
- Preprocessing: Label Encoding + One-Hot Encoding
- Feature Selection: ANOVA F-test + Recursive Feature Elimination (RFE)
- Reduced 123 features to 13 critical risk indicators per category
- Models: Decision Tree, KNN, SVM, Voting Ensemble
- Evaluation: 10-fold cross-validation (Accuracy, Precision, Recall, F-measure)

## Results
| Attack | Best Model | Accuracy | F-measure |
|--------|-----------|----------|-----------|
| DoS | Voting Ensemble | 99.7% | 0.997 |
| Probe | Voting Ensemble | 99.2% | 0.988 |
| R2L | Decision Tree | 97.5% | 0.971 |
| U2R | Decision Tree | 99.7% | 0.877 |

## Tech Stack
Python · Scikit-learn · Pandas · NumPy · Matplotlib

## Dataset
KDD Cup 1999 — 125,973 training records, 22,544 test records, 42 features

## How to Run
1. Open `IDSnew.ipynb` in Google Colab
2. Upload `KDDTrain+_2.csv` and `KDDTest+_2.csv` to Google Drive
3. Update file paths in the first cell
4. Run all cells sequentially
