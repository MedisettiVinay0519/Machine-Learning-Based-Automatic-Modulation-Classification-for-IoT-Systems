# 📡 ML-Based Automatic Modulation Classification (AMC)

## 🚀 Overview
This project focuses on **Automatic Modulation Classification (AMC)** using Machine Learning and Deep Learning techniques to classify modulation schemes from raw IQ signal data without prior knowledge of transmitter parameters.

The system is trained on the **RadioML dataset** and evaluated under **noisy channel conditions (low SNR)** to ensure robustness for real-world wireless applications.

---

## 🏗️ System Architecture
![System Block Diagram](Model%20Design/AMC-SYSTEM-ARCH.png)

The overall pipeline includes:
- Signal generation / dataset input  
- Channel effects (AWGN noise, fading)  
- IQ sample extraction  
- Preprocessing  
- Classification using ML/DL models  

---

## 🧠 Deep Learning Architecture
![CNN Architecture](Model%20Design/AMC_MODEL-Arch1.jpeg)
![CNN Architecture](Model%20Design/AMC_MODEL-Arch2.jpeg)

The CNN model is designed to learn directly from raw IQ signals:
- Convolution + BatchNorm + ReLU layers  
- Residual (skip) connections for better gradient flow  
- Downsampling with increasing filters (64 → 128 → 256)  
- Global Average Pooling  
- Dense + Dropout layers for classification  

---

## 🎯 Objectives
- Classify modulation schemes using IQ signal data  
- Evaluate performance under **low SNR (-10 dB)**  
- Compare **ML vs Deep Learning approaches**  
- Improve robustness using preprocessing and tuning  

---

## ⚙️ Methodology
- Dataset: 32,000 samples (RadioML)  
- Modulations: 4ASK, BPSK, QPSK, 16PSK, 16QAM, FM, AM-DSB-WC, 32APSK  
- Train/Test Split: 80/20  

### Preprocessing
- Normalization  
- IQ data reshaping  
- Label encoding  

---

## 🧪 Models & Performance

### 🔹 Machine Learning
- KNN → ~56% accuracy  
- Random Forest → ~66% accuracy  

### 🔹 Deep Learning (CNN)
- ~85% accuracy (10 epochs)  
- **~98% accuracy (30 epochs)**  

---

## 📊 Results
- Significant improvement over traditional ML models  
- Reduced misclassification between similar modulation types  
- Strong performance even under noisy conditions  

---

## 🛠️ Tech Stack
- Python  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  

---

## 🌍 Applications
- Cognitive Radio  
- Wireless Communication Systems  
- Spectrum Monitoring  
- IoT Networks  

---

## 🔮 Future Work
- Multi-SNR training  
- Real-time deployment  
- Edge/IoT optimization  

---

## 📄 Report
👉 Add your project report PDF link here  

