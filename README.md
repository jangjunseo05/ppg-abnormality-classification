# Robust Arrhythmia Classification from PPG Signals

## 📌 Project Overview
[cite_start]This project focuses on building a robust 1D-CNN (VGG-based) model to classify arrhythmia using PPG biosignals[cite: 53, 294]. [cite_start]The core objective was to overcome the inherent noise and variability in human-generated data through a high-fidelity preprocessing pipeline[cite: 56].

## 🛠️ Key Research Points & Decisions
* [cite_start]**Decision 1: Morphological Normalization via Stretching [cite: 56]**
  - [cite_start]Instead of simple padding, I applied **Cubic Spline Interpolation** to normalize segment lengths to 2,000 samples[cite: 56]. This preserved the vital morphological features of the PPG wave, which are critical for arrhythmia detection.
* [cite_start]**Decision 2: Stability over Complexity  [cite: 352-363, 1066]**
  - [cite_start]Implemented a modified VGG-1D architecture with **He Initialization** and **L2 Regularization**  [cite: 356-361, 1066]. 
  - [cite_start]Used **ReduceLROnPlateau** to achieve stable convergence despite the small dataset (20 patients)[cite: 58, 352].

## 📊 Results
* [cite_start]**Accuracy:** 0.9848 [cite: 346, 721]
* [cite_start]**AUC:** 1.0000 [cite: 346, 721]
* [cite_start]**Insight:** The experiment proved that in human-centric sensing, the quality of signal interpretation (preprocessing) often dictates model performance more than the model capacity itself[cite: 13, 58].
