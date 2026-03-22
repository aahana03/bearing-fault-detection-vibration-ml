# CWRU Dataset Analysis

## Overview
This section presents the development of a machine learning model for bearing fault classification using the Case Western Reserve University (CWRU) Bearing Dataset. 
This dataset consists of vibration signals recorded under controlled laboratory conditions with known fault types.

---

## Objective
- To study how frequencies vary for faulty vs. healthy data 
- Whether a machine learning model performs as expected for benchmark datasets. 

---

## Methodology

### Feature Extraction

Two types of features were extracted from vibration signals:

#### Statistical & Spectral Features:
- RMS (Root Mean Square)  
- Standard Deviation  
- Kurtosis  
- Crest Factor  
- Spectral Centroid  
- Spectral Entropy  

#### Bearing Fault Frequency Features:
- Maximum amplitude at BPFO (Ball Pass Frequency Outer race)  
- Maximum amplitude at BPFI (Ball Pass Frequency Inner race)  
- Maximum amplitude at BSF (Ball Spin Frequency)  
- Maximum amplitude at FTF (Fundamental Train Frequency)  

## Model Development

Multi-class classification was performed to identify different fault types:
- Healthy  
- Inner race fault  
- Outer race fault  
- Ball/Cage fault  

Multiple machine learning models were evaluated.
