# quantum-rul-surrogate
for Quantum_Driven_Partition_Based_Bayesian_Optimization_Using_Local_Surrogate
# Quantum-Classical Hybrid RUL Prediction using Bayesian Optimization

This project explores a hybrid approach for Remaining Useful Life (RUL) prediction using both classical (Ridge regression) and quantum machine learning (VQC - Variational Quantum Classifier). It uses Bayesian optimization to dynamically tune model parameters and training intervals for improved predictive performance.

---

## 🚀 Key Features

- ✅ Preprocessing and scaling of engine sensor datasets
- ⚙️ Interval-based surrogate modeling using Ridge Regression
- 🔍 Bayesian optimization of:
  - Number of intervals
  - Lambda fusion weight
  - Penalty weight
- 🧠 Quantum surrogate model using Qiskit’s `VQC`
- 📉 RMSE-based evaluation for classical vs quantum models

---

## 🧠 Methodology

1. **Data Normalization:** Sensor data from the FD001 dataset is standardized.
2. **Interval-Based Modeling:** RUL is divided into quantized intervals, and separate Ridge models are trained per interval.
3. **Fusion & Penalty Function:** Models are combined using a lambda-weighted loss function that incorporates a penalty for deviation.
4. **Bayesian Optimization:** The loss function is minimized using Gaussian Process-based `gp_minimize` from `scikit-optimize`.
5. **Quantum Model Training:** A Qiskit-based `VQC` model is trained on one of the larger intervals for comparison.

---

## 📂 Files

- `Quantum_RUL_Model.py` – Main training script
- `train_FD001.txt` – CMAPSS dataset (you must add this)
- `LICENSE` – MIT license
- `README.md` – This file

---

## 📦 Requirements

Install dependencies via pip:

```bash
pip install -r requirements.txt
