# EEG Classification of Alpha-Band Oscillations

## Overview
This project implements a machine learning pipeline to classify EEG brain states (eyes-open vs eyes-closed) using alpha-band (≈8–12 Hz) neural activity. The workflow combines signal processing and interpretable machine learning to analyze frequency-domain EEG patterns.

---

## Key Result
- Achieved strong classification performance using a Logistic Regression model on EEG-derived features

---

## Signal Processing

### Alpha-Band Feature Extraction
- Extracted frequency-domain features from 64-channel EEG recordings using MNE-Python  
- Applied Power Spectral Density (PSD) analysis to identify alpha-band (8–12 Hz) activity  
- Observed stronger alpha power during eyes-closed conditions compared to eyes-open  

![Alpha Power Spectral Density](alpha_skyscraper.png)

---

## Machine Learning Pipeline
- StandardScaler normalization of EEG feature vectors  
- Logistic Regression classifier (Scikit-Learn)  
- Feature engineering based on frequency-domain EEG signals  

---

## Interpretability

- Mapped model coefficients back to EEG scalp regions  
- Identified strongest predictive signals in occipital region  
- Results align with known visual cortex activity patterns  

![EEG Feature Importance Map](ai_feature_map.png)

---

## Tech Stack
- Python  
- MNE-Python  
- Scikit-Learn  
- NumPy  
- Pandas  
- Jupyter Notebook  

---

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook EEG-Alpha-Classifier.ipynb
