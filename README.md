# EEG Motor Imagery Classification using SPWVD and CNN

In this project, I've used Deep learning for 4-class motor imagery EEG classification using Smoothed Pseudo Wigner–Ville Distribution (SPWVD) time-frequency representations and Convolutional Neural Network (CNN) on the BCI Competition IV-2a dataset. 

I used SPWVD to transform EEG signals into TFR images. EEG data from 3 motor cortex channels (C3,C4,Cz) with 1-D data were converted into TFR images (2-D data) having the size of 256 × 256 pixels. Unlike my previous project, CSP+LDA, this approach leverages time-frequency representations + CNNs to automatically learn discriminative patterns from EEG signals.

### Main Contributions:

✅ High-resolution Time-Frequency Analysis using SPWVD

✅ CNN-based Motor Imagery Classification

✅ Comparison with my previous project (Classical CSP + LDA/SVM)

---
##  Dataset:  BCI Competition IV – 2a

| **Aspect** | **Details** |
|------------|-------------|
| Dataset | BCI Competition IV-2a (Subjects A01-A09) |
| Classes | Left hand, Right hand, Foot, Tongue (4 classes) |
| EEG Channels | 3 (C3, Cz, C4) |
| Time window | 2-6 seconds post-cue |
| Frequency band | 8-30 Hz (bandpass filtered) |

### Motor Imagery Classes

| Label | Task |
|---------|---------|
| 1 | Left Hand |
| 2 | Right Hand |
| 3 | Foot |
| 4 | Tongue |

---

## Methodology

```text
Raw EEG
    │
    ▼
Preprocessing
    │
    ▼
Epoch Extraction (2–6 s)
    │
    ▼
Channel Selection
 (C3, Cz, C4)
    │
    ▼
 SPWVD
    │
    ▼
Time-Frequency Images
    │
    ▼
   CNN
    │
    ▼
4-Class Classification

```

## Time-Frequency Representation (TFR)

The EEG signals are transformed into **Time-Frequency Representations (TFRs)** using the **Smoothed Pseudo Wigner–Ville Distribution (SPWVD)**.

### Why SPWVD?

| Method | Time Resolution | Frequency Resolution |
|----------|----------|----------|
| STFT | Medium | Medium |
| Wavelet Transform | High | Medium |
| SPWVD | Very High | Very High |

### Advantages

- Better energy concentration
- Captures ERD/ERS patterns
- Suitable for non-stationary EEG signals
- High time-frequency resolution

---

# Results

### Classical Machine Learning

| Method | Accuracy |
|----------|----------|
| CSP + LDA | ? |
| CSP + SVM | ? |
| SPWVD + CNN | ? |

---


## Author

**Hesam Moradkhani**

Research Interests:

- Brain-Computer Interfaces (BCI)
- EEG Signal Processing
- Machine Learning
- Deep Learning
- NeuroAI

## ⭐ If you find this project useful

Consider giving the repository a star.
