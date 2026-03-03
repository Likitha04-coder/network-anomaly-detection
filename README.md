\# 🔒 Network Anomaly Detection System using CICIDS2017



!\[Python](https://img.shields.io/badge/Python-3.8+-blue.svg)

!\[ML](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange.svg)

!\[DL](https://img.shields.io/badge/Deep%20Learning-TensorFlow%2FKeras-red.svg)

!\[Status](https://img.shields.io/badge/Status-Completed-brightgreen.svg)



---



\## 📌 Project Overview



A comprehensive \*\*Machine Learning \& Deep Learning\*\* based \*\*Network Intrusion Detection System (NIDS)\*\* built using the \*\*CICIDS2017\*\* dataset. The system uses a \*\*two-layer architecture\*\* to first detect if network traffic is malicious, then classify the specific attack type among \*\*14 different attack categories\*\*.



---



\## 🎯 Objectives



\- Detect \*\*Benign vs Malicious\*\* network traffic (Binary Classification)

\- Classify \*\*14 types of network attacks\*\* (Multi-class Classification)

\- Predict \*\*time to next attack\*\* (Regression)

\- Compare \*\*ML vs Deep Learning\*\* model performance



---



\## 📊 Dataset



| Detail | Value |

|--------|-------|

| \*\*Dataset\*\* | CICIDS2017 (Canadian Institute for Cybersecurity) |

| \*\*Total Records\*\* | 2,830,743+ |

| \*\*Files\*\* | 8 CSV files |

| \*\*Features\*\* | 85 network flow features |

| \*\*Attack Types\*\* | 14 + Benign |



\### Attack Types:

| # | Attack Type |

|---|-------------|

| 1 | FTP-Patator |

| 2 | SSH-Patator |

| 3 | DoS Slowloris |

| 4 | DoS Slowhttptest |

| 5 | DoS Hulk |

| 6 | DoS GoldenEye |

| 7 | Heartbleed |

| 8 | Web Attack — Brute Force |

| 9 | Web Attack — XSS |

| 10 | Web Attack — SQL Injection |

| 11 | Infiltration |

| 12 | Bot |

| 13 | DDoS |

| 14 | PortScan |



---



\## 🏗️ Project Architecture



```

Input Network Traffic

&nbsp;       |

&nbsp;       v

+---------------------+

|  Layer 1: Binary     |

|  BENIGN vs ATTACK    |

|  (RandomForest/XGB)  |

+---------+-----------+

&nbsp;         |

&nbsp;   +-----+-----+

&nbsp;   |           |

&nbsp;BENIGN     ATTACK

&nbsp;   |           |

&nbsp;   v           v

&nbsp; Done   +---------------------+

&nbsp;        |  Layer 2: Multi-class|

&nbsp;        |  Attack Type (14)    |

&nbsp;        |  (DL / RF / XGB)     |

&nbsp;        +---------------------+

```



---



\## 🔬 Methodology



\### 1. Data Loading \& Preprocessing

\- Loaded \*\*8 CSV files\*\* from CICIDS2017 dataset

\- Handled \*\*NaT timestamps\*\* and missing values

\- Cleaned column names and encoded categorical features

\- Created \*\*Binary\_Label\*\* (0: BENIGN, 1: ATTACK)

\- Created \*\*Attack\_Type\*\* column for multi-class classification



\### 2. Exploratory Data Analysis (EDA)

\- Distribution analysis of network features

\- Correlation heatmaps

\- Class distribution visualization

\- Temporal analysis (hour, minute patterns)

\- Univariate \& Bivariate analysis



\### 3. Feature Engineering

\- Label Encoding for categorical features

\- Standard Scaling for numerical features

\- Removed \*\*highly correlated features\*\* (>0.9 with target) to prevent data leakage

\- Final feature set: \*\*87 features\*\*



\### 4. Model Training \& Evaluation



\#### Layer 1: Binary Classification (BENIGN vs ATTACK)

\- Random Forest Classifier

\- Logistic Regression

\- XGBoost Classifier

\- LightGBM Classifier

\- \*\*5-Fold Stratified Cross Validation\*\*



\#### Layer 2: Multi-class Attack Classification

\- Random Forest Classifier

\- XGBoost Classifier

\- LightGBM Classifier

\- \*\*Deep Learning: MLP (Multi-Layer Perceptron)\*\*

\- \*\*Deep Learning: LSTM (Long Short-Term Memory)\*\*



\### 5. Time to Next Attack Prediction

\- Random Forest Regressor

\- Predicts time gap between attacks



---



\## 📈 Results



\### Layer 1: Binary Classification (BENIGN vs ATTACK)



| Model | Accuracy | Precision | Recall | F1-Score | AUC |

|-------|----------|-----------|--------|----------|-----|

| \*\*Random Forest\*\* | \*\*99.98%\*\* | 99.98% | 99.98% | 99.98% | 1.0000 |

| \*\*XGBoost\*\* | \*\*99.99%\*\* | 99.99% | 99.99% | 99.99% | 1.0000 |

| \*\*LightGBM\*\* | \*\*99.99%\*\* | 99.99% | 99.99% | 99.99% | 1.0000 |

| Logistic Regression | 80.27% | 81.27% | 80.26% | 80.10% | 0.8872 |



\### Layer 2: Multi-class Attack Classification



| Model | Accuracy |

|-------|----------|

| \*\*MLP (Deep Learning)\*\* | \*\*99.55%\*\* |

| \*\*LSTM (Deep Learning)\*\* | \*\*98.01%\*\* |

| Random Forest | 99.26%+ |



\### Time to Next Attack Prediction



| Metric | Value |

|--------|-------|

| MAE | 583.38 minutes |

| RMSE | 3366.42 minutes |

| \*\*R2 Score\*\* | \*\*0.958\*\* |



---



\## 🛠️ Tech Stack



| Category | Tools |

|----------|-------|

| \*\*Language\*\* | Python 3.8+ |

| \*\*Data Processing\*\* | Pandas, NumPy |

| \*\*Visualization\*\* | Matplotlib, Seaborn |

| \*\*Machine Learning\*\* | Scikit-learn, XGBoost, LightGBM |

| \*\*Deep Learning\*\* | TensorFlow, Keras |

| \*\*Model Saving\*\* | Joblib |

| \*\*Environment\*\* | Jupyter Notebook, Anaconda |



---



\## 📁 Project Structure



```

Network-Anomaly-Detection/

|

├── Assignment-Final.ipynb        # Complete notebook (EDA + ML + DL)

├── README.md                     # Project documentation

├── .gitignore                    # Ignore large files

|

├── time\_to\_next\_attack\_model.pkl # Saved regression model

├── time\_to\_next\_attack\_features.pkl # Saved feature list

|

└── TrafficLabelling/             # Dataset folder (not uploaded)

&nbsp;   ├── Friday-WorkingHours-Afternoon-DDos.pcap\_ISCX.csv

&nbsp;   ├── Friday-WorkingHours-Afternoon-PortScan.pcap\_ISCX.csv

&nbsp;   ├── Friday-WorkingHours-Morning.pcap\_ISCX.csv

&nbsp;   ├── Monday-WorkingHours.pcap\_ISCX.csv

&nbsp;   ├── Thursday-WorkingHours-Afternoon-Infilteration.pcap\_ISCX.csv

&nbsp;   ├── Thursday-WorkingHours-Morning-WebAttacks.pcap\_ISCX.csv

&nbsp;   ├── Tuesday-WorkingHours.pcap\_ISCX.csv

&nbsp;   └── Wednesday-workingHours.pcap\_ISCX.csv

```



---



\## 🚀 How to Run



\### 1. Clone the Repository

```bash

git clone https://github.com/Likitha04-coder/Network-Anomaly-Detection.git

cd Network-Anomaly-Detection

```



\### 2. Install Dependencies

```bash

pip install pandas numpy matplotlib seaborn scikit-learn xgboost lightgbm tensorflow joblib

```



\### 3. Download Dataset

\- - Download CICIDS2017 from: \[CICIDS2017 Dataset](https://www.unb.ca/cic/datasets/ids-2017.html)

\- Place CSV files in `TrafficLabelling/` folder



\### 4. Run the Notebook

```bash

jupyter notebook Assignment-Final.ipynb

```



---



\## 📊 Sample Predictions



| # | Layer 1 Prediction | Layer 2 Attack Type |

|---|-------------------|---------------------|

| 1 | Benign | N/A |

| 2 | Benign | N/A |

| 3 | Benign | N/A |

| 4 | Attack | PortScan |

| 5 | Attack | DoS Hulk |

| 6 | Attack | DDoS |

| 7 | Attack | DoS GoldenEye |

| 8 | Attack | FTP-Patator |

| 9 | Attack | SSH-Patator |

| 10 | Attack | Web Attack — Brute Force |



---



\## 🔑 Key Findings



1\. \*\*Tree-based models\*\* (RF, XGB, LGBM) achieved near-perfect accuracy (\*\*99.99%\*\*) for binary classification

2\. \*\*Deep Learning MLP\*\* achieved \*\*99.55%\*\* accuracy for multi-class attack classification

3\. \*\*Logistic Regression\*\* struggled with the dataset (\*\*80.27%\*\*), showing non-linear patterns

4\. \*\*Two-layer architecture\*\* provides both detection and classification in one pipeline

5\. \*\*Time-to-next-attack prediction\*\* achieved \*\*R2 = 0.958\*\*, useful for proactive defense



---



\## ⚠️ Notes



\- Dataset is \*\*NOT included\*\* in this repo due to size (~2.8GB)

\- Download from the official CICIDS2017 source

\- GPU recommended for deep learning models but CPU works too

\- 200K sampled rows used for faster training



---



\## 👤 Author



\*\*Likitha Puttaraju\*\*



\- 📧 Email: likithap2404@gmail.com

\- 💼 LinkedIn: \[Likitha Puttaraju](https://linkedin.com/in/likitha-putta-raju-904a551b0)

\- 🐙 GitHub: \[@Likitha04-coder](https://github.com/Likitha04-coder)



---



\## 📜 License



This project is for \*\*educational and research purposes only\*\*.



---



\## ⭐ If you found this useful, give it a star!

```



---





