\# 🛡️ Network Anomaly Detection System



A \*\*3-Layer Machine Learning Pipeline\*\* for detecting, classifying, and predicting network intrusions using the UNSW-NB15 dataset.



---



\## 📋 Project Overview



| Layer | Task | Model | Performance |

|-------|------|-------|-------------|

| \*\*Layer 1\*\* | Binary Classification (Normal vs Attack) | Random Forest | ~95% Accuracy |

| \*\*Layer 2\*\* | Multi-class Attack Type Classification | Random Forest | ~90% Accuracy |

| \*\*Layer 3\*\* | Time-to-Next-Attack Regression | XGBoost + HGBR Ensemble | Optimized MAE |



---



\## 🏗️ Architecture



Incoming Network Traffic → Layer 1 (Normal vs Attack) → Layer 2 (Attack Type) → Layer 3 (Time to Next Attack)



---



\## 🔧 Tech Stack



\- Python 3.x

\- scikit-learn

\- XGBoost

\- pandas / numpy

\- matplotlib / seaborn



---



\## 📊 Dataset



\*\*UNSW-NB15\*\* - A comprehensive network intrusion detection dataset



---



\## 🚀 How to Run



1\. Clone the repository

2\. pip install scikit-learn xgboost pandas numpy matplotlib seaborn jupyter

3\. jupyter notebook Assignment-Final.ipynb



---



\## 👩‍💻 Author



\*\*Likitha\*\* - \[GitHub Profile](https://github.com/Likitha04-coder)



