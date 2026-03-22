# Bearing Fault Detection using Vibration Analysis and Machine Learning

## Overview
This project focuses on developing a supervised machine learning model to detect faults in rolling-element bearing using vibration signal analysis under both benchmark and real experimental conditions.

The study is carried out in two stages:
1. Benchmark analysis using the Case Western Reserve University Bearing Dataset.  
2. Real-world experimentation using a custom-built test rig.

---

## Key Contributions
- Developed a multi-class classifier on benchmark CWRU data achieving ~93% accuracy.  
- Designed and assembled a custom bearing test rig.
- Collected multi-session vibration data under under constant RPM conditions (=500 RPM).  
- Extracted statistical and spectral features:
  1. RMS, Standard Deviation  
  2. Kurtosis, Crest Factor  
  3. Spectral Centroid, Spectral Entropy  
- Engineered resultant features to handle multi-axis data.  
- Achieved ~95.5% accuracy (binary classification) on unseen experimental session data.
- Performed FFT analysis on vibration signals to identify frequencies of structural resonance and
  excess noise overlapping the actual signal.

---

## Machine Learning Pipeline
Raw Signal → Multi-Axis Feature Extraction → Resultant Features → Scaling → ML Model → Classification

---

## Tech Stack
- Python  
- NumPy, Pandas  
- Scikit-learn  
- Matplotlib
- C/C++

---

## Future Work
- Improved sensor mounting and vibration isolation.  
- Exploration of composite materials with reduced transmissibility.

---

## Summary
This project highlights the challenges of applying ML to real-world vibration data and demonstrates how multi-session training improves robustness.
