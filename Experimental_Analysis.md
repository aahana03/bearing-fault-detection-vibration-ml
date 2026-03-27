# Experimental Vibration Analysis

## Overview
This section presents the development and evaluation of a machine learning-based bearing fault detection system using vibration data collected from a custom experimental setup.

Unlike benchmark datasets, this data captures **real-world variability across multiple sessions**.

---

## Experimental Setup

- Bearing mounted inside a housing placed on a rigid plate  
- Accelerometer mounted on the housing  
- Constant RPM operating conditions   
- Data collected across multiple sessions  
- ESP32 and MPU6050 used to acquire vibration data

### Setup Images
![Test Rig](graphs/test_rig.jpg)
![Sensor Placement](graphs/sensor.jpg)

---

## Objective
- To evaluate the performance of various ML models on **real experimental vibration data**.
- To study the effect of session variability and structural resonance on the quality of vibration signals.

---

## Methodology

### Feature Extraction
Raw acceleration data was recorded using accelerometer and micrcontroller and the following features were extracted along x, y and z- axes:

- RMS  
- Standard Deviation  
- Kurtosis  
- Crest Factor  
- Spectral Centroid  
- Spectral Entropy  

### Feature Engineering
- Resultant features computed from multi-axis data to ensure orientation independence  

---

## Feature Analysis

### RMS Variation Across Sessions
![RMS Plot](https://github.com/aahana03/bearing-fault-detection-vibration-ml/blob/e7351113712cded2788f0d7528cdd6f1d5f4f5c7/RMS%20Variation%20across%20sessions.png)

RMS values indicate higher vibration energy for faulty bearings, but also show variation across sessions.

---

### Spectral Entropy Variation
![Entropy Plot](https://github.com/aahana03/bearing-fault-detection-vibration-ml/blob/6dfb2415b38207816e73269709e7435995e2ed85/Spectral%20Entropy%20Variation%20across%20sessions.png)

Spectral features exhibit significant variation across sessions, highlighting sensitivity to experimental conditions.

---

### Heatmap
![Heatmap Plot](graphs/entropy_sessions.png)

Spectral features exhibit significant variation across sessions, highlighting sensitivity to experimental conditions.

---

## Model Development

Binary classification was performed:
- Healthy  
- Faulty  

---

### Model training and testing results
![ML model Comparison](graphs/entropy_sessions.png)

### Model Performance on Unseen Session Data
![Model Performance](graphs/entropy_sessions.png)
![confusion Matrix](graphs/entropy_sessions.png)

---

## Conclusion

Instance-based methods, K-Nearest Neighbours exhibit superior robustness in real-world scenarios with distribution variability. While machine learning models perform well on controlled datasets, real-world vibration data introduces variability that impacts performance. Incorporating multi-session data is essential for building robust fault detection systems. The contrasting performance of SVC and KNN highlights the impact of dataset characteristics on model selection.
