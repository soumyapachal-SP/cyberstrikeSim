# 🚀 CyberStrike Sim  
### A Real‑Time Simulation Framework for ML‑Based Intrusion Detection Systems

---

## 📌 Overview
**CyberStrike Sim** is a deployment‑oriented benchmarking framework for evaluating **Machine Learning (ML)–based Intrusion Detection Systems (IDS)** under **real‑time cloud conditions**.  
Unlike traditional IDS studies that rely only on offline accuracy, this framework integrates **latency‑aware simulation** using MATLAB cloudlets to assess real‑world deployability.

The framework combines:
- Hybrid dataset generation
- Offline ML model training (Python)
- Real‑time inference and latency evaluation (MATLAB)


---

## 🧠 Key Features
- Hybrid dataset generation using **CloudSim, Wireshark, and synthetic attacks**
- Dataset structure aligned with **NF‑ToN IoT, NSL‑KDD, and UNSW‑NB15**
- Support for multiple ML models
- **Latency‑aware benchmarking** using MATLAB cloudlet simulation
- Real‑time performance analysis beyond offline metrics

---

## 🗂️ Dataset Description
A **merged hybrid dataset** created from:
- **NF‑ToN IoT**
- **NSL‑KDD**
- **UNSW‑NB15**
- CloudSim‑generated traffic
- Wireshark packet captures
- Synthetic attack injection

### 🔹 Key Flow Features
- Duration  
- Protocol  
- Source / Destination  
- Source packets (spkts)  
- Destination packets (dpkts)  
- Attack label  

### 🔹 Attack Classes (5‑Class IDS Mapping)
- **Normal**
- **DoS**
- **Probe**
- **R2L** (Remote‑to‑Local)
- **U2R** (User‑to‑Root)

---

## ⚙️ Preprocessing Pipeline
- Protocol encoding (TCP→6, UDP→17, ICMP→1)
- Feature scaling
- Label encoding
- Data randomization
- **80:20 stratified train‑test split**

---

## 🧪 Methodology Workflow
1. Data acquisition and dataset merging  
2. Feature selection (flow‑level attributes)  
3. Preprocessing and normalization  
4. ML model training (Python)  
5. Offline evaluation (Accuracy, ROC‑AUC, MCC, Kappa)  
6. Latency profiling per model  
7. MATLAB cloudlet‑based real‑time simulation  
8. Deployment‑oriented performance analysis  

---

## 🤖 Machine Learning Models
- LightGBM  
- Random Forest  
- XGBoost  
- Ensemble Model  

---

## ⏱️ Real‑Time MATLAB Simulation
- ~**290,000 cloudlets** simulated
- Each cloudlet represents a **live inference request**
- Python‑derived latency profiles imported into MATLAB
- Metrics evaluated:
  - Average inference latency
  - Total execution time
  - Throughput
  - Real‑time accuracy

---

## 📊 Key Findings
- **XGBoost** achieves the best accuracy–latency balance
- **Ensemble model** provides the highest ROC‑AUC
- **Random Forest** offers lowest latency with moderate accuracy
- Offline metrics alone are insufficient for deployment decisions

---

## 🛠️ Tools & Technologies
- Python (Scikit‑learn, XGBoost, LightGBM)
- MATLAB (Cloudlet simulation)
- CloudSim
- Wireshark

