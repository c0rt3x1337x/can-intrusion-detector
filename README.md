# can-intrusion-detector
This project demonstrates a machine learning pipeline for detecting cyberattacks on in-vehicle CAN (Controller Area Network) bus systems using a Random Forest classifier.

# CAN Intrusion Detector 🔐🚗

This project presents a machine learning pipeline for detecting malicious activity on in-vehicle CAN (Controller Area Network) bus systems using a Random Forest classifier. The model distinguishes between normal and anomalous messages in a binary classification setting.

---

## 🚀 Features

- Preprocesses raw CAN bus message logs into ML-ready format
- Trains a Random Forest classifier using 8 data bytes and CAN ID
- Supports detection of attack patterns such as flooding and spoofing
- Evaluates performance using standard metrics and visualizations
- Designed as a reproducible, extensible portfolio project

---

## 📁 Dataset

The dataset consists of CAN bus messages with timestamp, CAN ID, 8 data bytes, and labeled normal/attack flags.

Each message contains:
- Timestamp
- CAN_ID
- Data[0] through Data[7]
- Label indicating normal or attack (`R` = normal, `T` = attack)

---

## ⚙️ Model Pipeline

1. Load and clean the CAN bus dataset
2. Convert hexadecimal fields to integers
3. Use CAN ID and data bytes as input features
4. Encode labels as binary targets
5. Train/test split with stratification
6. Train a Random Forest model
7. Evaluate using confusion matrix, F1-score, precision, recall


## 🧰 Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

Install all dependencies:
```bash
pip install -r requirements.txt
