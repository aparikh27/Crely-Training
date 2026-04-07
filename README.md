# Crely Training: ECG Signal Processing Pipeline

## Overview
This project demonstrates an end*to*end pipeline for physiological signal processing and ECG classification using open*source clinical datasets.  

The goal is to showcase readiness for real*world biomedical data (e.g., Crely’s multi*modal datasets) by building a reproducible workflow from raw signals to machine learning predictions.


## Tech Stack
* **Language:** Python  
* **Datasets:** PhysioNet (MIT*BIH, PTB*XL)  
* **Libraries:** `wfdb`, `neurokit2`, `numpy`, `pandas`, `matplotlib`, `scikit*learn`  


## Pipeline

### Week 1 — Data (WFDB)
* Loaded ECG signals + annotations from MIT*BIH  
* Visualized heartbeats with labeled peaks  

### Week 2 — Signal Processing (NeuroKit2)
* Cleaned ECG signals (noise + baseline removal)  
* Detected R-peaks  
* Extracted Heart Rate + HRV  

### Week 3 — Features & Labels
* Processed PTB-XL dataset  
* Extracted interval + HRV features  
* Mapped labels to Normal vs Abnormal  

### Week 4 — ML Pipeline
* Preprocessing (imputation + scaling)  
* Feature-based classification  
* Model: Random Forest (balanced)  


## Results
* Built dataset from raw ECG signals  
* Extracted clinically meaningful features  
* Trained and evaluated a classification model  
* Output: **Normal vs Arrhythmia prediction**


## Key Takeaways
* ECG signals require robust cleaning + feature extraction  
* Signal features map directly to clinical conditions  
* Reproducible pipelines are critical for real-world data  


## Reproducibility
* Data downloaded programmatically via PhysioNet  
* End-to-end pipeline runs via notebook