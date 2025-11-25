# 🎧 BanglaSER Fusion: Early Feature-Level Fusion for Robust Bangla Speech Emotion Recognition

This repository contains the implementation of **Early Feature-Level Fusion of Spectral and Temporal Descriptors** for **Bangla Speech Emotion Recognition (SER)** — a complete, reproducible framework that integrates *hybrid acoustic features*, *targeted augmentation*, and *deep neural architectures* for high-accuracy emotion classification.

The project builds a strong baseline for SER in low-resource languages and establishes a rigorous benchmark for the **BanglaSER dataset**.

---

## ⭐ Key Highlights

### 🔹 Early Feature-Level Fusion

Unified fusion of **MFCC**, **Log-Mel**, **ZCR**, **Chroma**, and **RMS** features into a single enriched acoustic tensor.

---

## 🗂️ Dataset

This project uses the BanglaSER dataset (Version 5), which contains:

* 1,467 Bangla audio utterances from 34 speakers (17 male, 17 female) covering five emotional states: angry, happy, sad, surprise, neutral. ([Mendeley Data][1])
* Recorded via smartphones and laptops in real-life conditions, supporting generalizable SER model training. ([Mendeley Data][1])

Dataset download links:

* [Zenodo version used in this project] — [https://zenodo.org/records/8265464](https://zenodo.org/records/8265464)
* **Additional official version** — [https://data.mendeley.com/datasets/t9h6p943xy/5](https://data.mendeley.com/datasets/t9h6p943xy/5)

---

### 🔹 Multiple Deep Architectures

The fused features are evaluated across:

* 1D-CNN
* LSTM
* GRU
* CNN-LSTM
* CNN-GRU
* LSTM-GRU
* Transfer models (YAMNet-BiLSTM, VGGish-BiLSTM)

### 🔹 Proposed High-Capacity CNN Model

A 2.77M-parameter **deep 1D-CNN** with progressively expanding filters and global average pooling achieves state-of-the-art performance.

### 🔹 State-of-the-Art Performance

On fused features + augmentation:

| Model            | Accuracy   | F1         |
| ---------------- | ---------- | ---------- |
| **Proposed CNN** | **96.80%** | **96.80%** |
| CNN-GRU          | 96.80%     | 96.79%     |
| CNN-LSTM         | 96.20%     | 96.19%     |
| Best Ensemble    | **97.20%** | **97.20%** |

---

## 📈 Results Summary

### 🔥 Individual Model Comparison

| Model              | Params | Accuracy   | F1         |
| ------------------ | ------ | ---------- | ---------- |
| **CNN (Proposed)** | 2.77M  | **96.80%** | **96.80%** |
| CNN-GRU            | 2.11M  | 96.80%     | 96.79%     |
| CNN-LSTM           | 2.50M  | 96.20%     | 96.19%     |
| GRU                | 1.26M  | 95.00%     | 95.00%     |
| LSTM               | 1.63M  | 93.80%     | 93.74%     |
| VGGish-BiLSTM      | 0.44M  | 77.00%     | 77.01%     |
| YAMNet-BiLSTM      | 1.36M  | 70.20%     | 70.23%     |

---

### 🤝 Ensemble Methods

Best performing ensemble:
**Mean Averaging (CNN + CNN_LSTM)** → **97.20% Accuracy & F1**

---

## 🧱 Repository Structure (Recommended)

```
Fusion-BanglaSER/
│── data/
│── features/
│── models/
│── notebooks/
│── src/
│   ├── preprocessing.py
│   ├── feature_extraction.py
│   ├── augmentation.py
│   ├── models_cnn.py
│   ├── models_rnn.py
│   └── ensemble.py
│── results/
│── README.md
```


## 🧑‍💻 Contributors

* **Tasnuba Islam**
* Rashik Iram Chowdhury
* Mohona Haque
* Sara Rahman
* Riasat Khan (Supervisor)

---
