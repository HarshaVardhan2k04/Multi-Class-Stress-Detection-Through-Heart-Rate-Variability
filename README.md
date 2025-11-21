# Multi-Class-Stress-Detection-Through-Heart-Rate-Variability
This project focuses on **multi-class stress detection** using **Heart Rate Variability (HRV)** analysis combined with **Machine Learning (ML)** and **Deep Learning (DL)** models. The goal is to classify stress levels based on HRV features extracted from ECG/PPG signals.

---

# 📘 Motivation
Stress affects mental health, productivity, and cardiovascular activity. Traditional evaluation methods rely on self-assessment, which is subjective.  
This project aims to create an automated, scientific approach:

**HRV Signal → Feature Extraction → ML/DL Models → Stress Classification**

---

# 🔍 Project Overview
The project includes:

- Data preprocessing  
- R-peak and RR interval detection  
- HRV feature extraction  
- ML & DL model training  
- Performance evaluation  
- Visualizations and reports  

---

# 📂 Folder Structure
Multi-Class Stress Detection Through Heart Rate Variability/
│
├── data/ # datasets (raw + processed)
│ ├── raw/ # raw recordings (ECG/PPG/ibi/edf/...); DO NOT commit large raw files
│ ├── interim/ # intermediate artifacts (cleaned signals, RR lists)
│ └── processed/ # feature CSVs and train/test splits
│
├── notebooks/ # exploratory notebooks and experiments
│ ├── 01-data-exploration.ipynb
│ ├── 02-feature-extraction.ipynb
│ └── 03-modeling-and-eval.ipynb
│
├── src/ # production-ready scripts & modules
│ ├── data/
│ │ └── loader.py # dataset loaders
│ ├── preprocess/
│ │ └── signal_processing.py
│ ├── features/
│ │ └── hrv_features.py
│ ├── models/
│ │ ├── train_ml.py
│ │ └── train_dl.py
│ ├── evaluate.py
│ └── utils.py
│
├── experiments/ # saved experiment configs, results, logs
│ └── exp_2025-11-21/
│
├── models/ # trained model binaries (.pkl, .h5, .pt)
│
├── scripts/ # small helper scripts (run_training.sh, prepare_data.ps1)
│
├── docs/ # extra docs, diagrams, paper drafts
│
├── tests/ # unit/integration tests
│
├── .gitignore
├── requirements.txt
├── setup.cfg / pyproject.toml # optional packaging config
└── README.md

yaml
Copy code

---

# 🧪 Dataset
Supports multiple formats:

- ECG / PPG  
- RR interval files (`.csv`, `.txt`, `.edf`, `.ibi`, `.json`)  
- Public datasets like WESAD, MIT-BIH  

---

# 🧬 HRV Features Extracted

### **Time-Domain**
- Mean RR  
- SDNN  
- RMSSD  
- pNN50 / pNN20  
- Heart Rate Mean  

### **Frequency-Domain**
- VLF, LF, HF  
- LF/HF ratio  
- Total power  

### **Non-Linear**
- SD1, SD2  
- Sample Entropy  
- Approximate Entropy  
- DFA α1 & α2  

---

# 🤖 Machine Learning Models Used
- Logistic Regression  
- Random Forest  
- SVM  
- KNN  
- Gradient Boosting  
- XGBoost  

Best-performing: **Random Forest & XGBoost**

---

# 🧠 Deep Learning Models Used
- LSTM  
- 1D-CNN  
- CNN + LSTM hybrid  
- Bi-LSTM  

Achieved accuracy: **90–96%** (varies by dataset)

---

# 📊 Evaluation Metrics
- Accuracy  
- Precision, Recall, F1-score  
- Confusion Matrix  
- ROC/AUC  
- Cross-validation  

---

# 🛠️ Installation

### Install dependencies:
```bash
pip install -r requirements.txt
## 👥 Contributors

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/HarshaVardhan2k04">
        <img src="https://github.com/HarshaVardhan2k04.png" width="100px;" alt="Harsha"/>
        <br /><sub><b>Harsha Vardhan</b></sub>
      </a>
    </td>

    <td align="center">
      <a href="https://github.com/MOhanNaidu04">
        <img src="https://github.com/MOhanNaidu04.png" width="100px;" alt="Mohan"/>
        <br /><sub><b>Mohan Naidu</b></sub>
      </a>
    </td>

    <td align="center">
      <a href="https://github.com/sreevamsee">
        <img src="https://github.com/sreevamsee.png" width="100px;" alt="Srivamshi"/>
        <br /><sub><b>Srivamshi Voggu</b></sub>
      </a>
    </td>
  </tr>
</table>
