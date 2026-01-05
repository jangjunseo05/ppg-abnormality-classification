# Robust Arrhythmia Classification from PPG Signals

Further details regarding this project are available in the attached PPT file!


## 📌 Project Overview
This project focuses on building a robust 1D-CNN (VGG-based) model to classify arrhythmia using PPG biosignals. 
The core objective was to overcome the inherent noise and variability in human-generated data through a high-fidelity preprocessing pipeline.

## 🛠️ Key Research Points & Decisions
* **Decision 1: Morphological Normalization via Stretching** 
  - Instead of simple padding, I applied **Cubic Spline Interpolation** to normalize segment lengths to 2,000 samples.
    This preserved the vital morphological features of the PPG wave, which are critical for arrhythmia detection.
* **Decision 2: Stability over Complexity** 
  - Implemented a modified VGG-1D architecture with **He Initialization** and **L2 Regularization** . 
  - Used **ReduceLROnPlateau** to achieve stable convergence despite the small dataset (20 patients).

## 📊 Results
* **Accuracy:** 0.9545 
* **AUC:** 0.9963 
* **Insight:** The experiment proved that in human-centric sensing, the quality of signal interpretation (preprocessing) often dictates model performance more than the model capacity itself.
