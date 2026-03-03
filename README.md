\# 🛡️ Network Anomaly Detection Using Machine Learning



A machine learning-based intrusion detection system that analyzes network traffic to classify normal and malicious activities using the CICIDS2017 dataset.



---



\## 📌 Project Overview



This project builds a complete network anomaly detection pipeline that:

\- Loads and cleans ~2.8 million network traffic records

\- Handles encoding issues, missing values, and timestamp errors

\- Performs feature engineering and preprocessing

\- Trains machine learning models to detect network attacks

\- Classifies traffic into BENIGN and various attack types



---



\## 📥 Dataset



\*\*CICIDS2017 (Canadian Institute for Cybersecurity - Intrusion Detection System 2017)\*\*



Download from official source:

https://www.unb.ca/cic/datasets/ids-2017.html



\### Files Used:



| File Name | Description |

|-----------|-------------|

| Monday-WorkingHours.pcap\_ISCX.csv | Normal traffic |

| Tuesday-WorkingHours.pcap\_ISCX.csv | FTP-Patator, SSH-Patator |

| Wednesday-workingHours.pcap\_ISCX.csv | DoS, Heartbleed |

| Thursday-WorkingHours-Morning-WebAttacks.pcap\_ISCX.csv | Web Attacks |

| Thursday-WorkingHours-Afternoon-Infilteration.pcap\_ISCX.csv | Infiltration |

| Friday-WorkingHours-Morning.pcap\_ISCX.csv | Bot |

| Friday-WorkingHours-Afternoon-DDos.pcap\_ISCX.csv | DDoS |

| Friday-WorkingHours-Afternoon-PortScan.pcap\_ISCX.csv | Port Scan |



\- \*\*Total Records:\*\* ~2,830,743 rows

\- \*\*Features:\*\* 85 columns

\- \*\*Attack Types:\*\* BENIGN, DDoS, PortScan, Bot, Infiltration, Web Attack, FTP-Patator, SSH-Patator, DoS, Heartbleed



---



\## 🛠️ Tech Stack



| Tool | Purpose |

|------|---------|

| Python 3.x | Programming Language |

| Pandas | Data Loading and Cleaning |

| NumPy | Numerical Operations |

| Scikit-learn | Machine Learning Models |

| Matplotlib | Data Visualization |

| Seaborn | Statistical Plots |

| Jupyter Notebook | Development Environment |



---



\## 📁 Project Structure



network-anomaly-detection/

├── network\_anomaly\_detection.ipynb   # Main Jupyter Notebook

├── README.md                         # Project Documentation

├── requirements.txt                  # Python Dependencies

├── .gitignore                        # Ignored files

└── images/                           # Screenshots and Plots (optional)



---



\## ⚙️ Installation and Setup



\### 1. Clone the Repository



git clone https://github.com/YOUR\_USERNAME/network-anomaly-detection.git

cd network-anomaly-detection



\### 2. Install Dependencies



pip install -r requirements.txt



\### 3. Download Dataset

\- Visit: https://www.unb.ca/cic/datasets/ids-2017.html

\- Download the GeneratedLabelledFlows folder

\- Place CSV files in your preferred directory

\- Update the data\_dir path in the notebook



\### 4. Run Notebook



jupyter notebook network\_anomaly\_detection.ipynb



---



\## 🔄 Workflow



Raw CSV Files → Data Loading (8 CSV files combined) → Data Cleaning (NaT removal, encoding fixes) → Exploratory Data Analysis (EDA) → Feature Engineering and Preprocessing → Model Training and Evaluation → Results and Classification Report



---



\## 📊 Key Steps



1\. \*\*Data Loading\*\* - Combined 8 CSV files (~2.8M records)

2\. \*\*Cleaning\*\* - Removed 288,602 NaT timestamp rows from WebAttacks file

3\. \*\*Encoding Fix\*\* - Handled ISO-8859-1 encoding issues

4\. \*\*EDA\*\* - Analyzed attack distribution and feature correlations

5\. \*\*Preprocessing\*\* - Scaling, encoding, train-test split

6\. \*\*Modeling\*\* - Trained ML classifiers for anomaly detection

7\. \*\*Evaluation\*\* - Accuracy, Precision, Recall, F1-Score



---



\## 📈 Results



| Metric | Score |

|--------|-------|

| Accuracy | Update after training |

| Precision | Update after training |

| Recall | Update after training |

| F1-Score | Update after training |



---



\## 🚀 Future Improvements



\- Add Deep Learning models (LSTM, Autoencoder)

\- Real-time network traffic monitoring

\- Deploy as web application using Flask or Streamlit

\- Add more datasets for cross-validation

\- Feature importance analysis



---



\## 👤 Author



\*\*Likitha Puttaraju\*\*

\- GitHub: https://github.com/Likitha04-coder

\- Email: likithap2404@gmail.com

\- LinkedIn: https://linkedin.com/in/likitha-putta-raju-904a551b0

s



\## 📄 License



This project is licensed under the MIT License.



---



\## ⭐ Show Support



If you found this project helpful, please give it a star on GitHub!



