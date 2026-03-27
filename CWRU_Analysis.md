# CWRU Dataset Analysis

## Overview
This section presents the development of a machine learning model for bearing fault classification using the Case Western Reserve University (CWRU) Bearing Dataset. 
This dataset consists of vibration signals recorded under controlled laboratory conditions with known fault types.

---

## Objective
- To study how frequencies vary for faulty vs. healthy data 
- Whether a machine learning model can clearly differentiate between healthy and faulty data. 

---

## Methodology

### Feature Extraction
The vibration signals were segmented into fixed-length windows of 2048 samples. Two types of features were extracted from vibration signals:

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

## Feature Analysis

### RMS Feature Distribution
![RMS Feature Plot](https://github.com/aahana03/bearing-fault-detection-vibration-ml/blob/edb1f7ce6f11f564908c07b62931ac5ce992be52/time_rms.png)

The feature distributions show clear separation between healthy and faulty bearing conditions, indicating that the dataset is well-suited for classification tasks.

## Results

**Test Accuracy: ~93.35%**

### Table comparing accuracies for different ML models
![Accuracy Comparison](https://github.com/aahana03/bearing-fault-detection-vibration-ml/blob/ee300bafb5557829b331cb7fb93246cd9ce8d870/image.png)

### Confusion Matrix and other metrics of the best performing model
![Tuned SVC](https://github.com/aahana03/bearing-fault-detection-vibration-ml/blob/cd7fa53fb35d85a1d090ec03a80d89be07e732bd/SVC_Train.png)
![Tuned SVC](https://github.com/aahana03/bearing-fault-detection-vibration-ml/blob/4ffb210a362ef938e672876f23ff03525b90a0cf/SVC_Test.png)

## Conclusion

Margin-based classifiers like Support Vector Classification perform well on structured benchmark datasets. However, such experiments are conducted under controlled conditions and they do not fully represent real-world operating conditions. Model performance on real industrial data with distributed damage and excess noise may be lower.
It can be observed from the confusion matrix that the model was able to perfectly separate healthy vibration data from faulty ones. However, there were some misclassifications within the faulty vibration signals, 

## Reference
https://www.kaggle.com/datasets/brjapon/cwru-bearing-datasets
