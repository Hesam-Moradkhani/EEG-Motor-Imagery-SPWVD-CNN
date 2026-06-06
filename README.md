# EEG Motor Imagery Classification using SPWVD and CNNs

In this project, I've used Deep learning for 4-class motor imagery EEG classification using Smoothed Pseudo Wigner–Ville Distribution (SPWVD) time-frequency representations and Convolutional Neural Networks (CNNs) on the BCI Competition IV-2a dataset. 

### Main Contributions:

✅ High-resolution Time-Frequency Analysis using SPWVD

✅ CNN-based Motor Imagery Classification

✅ Comparison with my previous project (Classical CSP + LDA/SVM)

---
##  Dataset:  BCI Competition IV – 2a

| **Aspect** | **Details** |
|------------|-------------|
| Dataset | BCI Competition IV-2a (Subject A01 & A02) |
| Classes | Left hand, Right hand, Foot, Tongue (4 classes) |
| EEG Channels | 22 channels |
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

## ⚙️ Methodology

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
CNN / ResNet18
    │
    ▼
4-Class Classification
```

---

## 🖼️ Time-Frequency Representation

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

## 🧪 Experiments

| Experiment | Input | Model |
|------------|---------|---------|
| Exp-1 | SPWVD Images | Custom CNN |
| Exp-2 | SPWVD Images | ResNet18 |
| Exp-3 | RGB-SPWVD (C3,Cz,C4) | ResNet18 |
| Exp-4 | CSP Features | LDA |
| Exp-5 | CSP Features | SVM |

---

## 📈 Results

### Classical Machine Learning

| Method | Accuracy |
|----------|----------|
| CSP + LDA | TBD |
| CSP + SVM | TBD |

### Deep Learning

| Method | Accuracy |
|----------|----------|
| SPWVD + CNN | TBD |
| SPWVD + ResNet18 | TBD |
| RGB-SPWVD + ResNet18 | TBD |

---

## 📂 Repository Structure

```text
EEG-Motor-Imagery-SPWVD-CNN/

├── data/
├── notebooks/
├── src/
├── models/
├── figures/
├── results/
├── README.md
├── requirements.txt
└── LICENSE
```

---

## 🚀 Future Work

- Subject-independent decoding
- EEGNet implementation
- ATCNet implementation
- Transfer learning
- Explainable AI (Grad-CAM)
- Vision Transformers (ViT)
- Cross-subject evaluation

---

## 🛠️ Installation

```bash
git clone https://github.com/yourusername/EEG-Motor-Imagery-SPWVD-CNN.git

cd EEG-Motor-Imagery-SPWVD-CNN

pip install -r requirements.txt
```

---

## 👨‍💻 Author

**Hesam Moradkhani**

Research Interests:

- Brain-Computer Interfaces (BCI)
- EEG Signal Processing
- Machine Learning
- Deep Learning
- Neurotechnology

---

## ⭐ If you find this project useful

Consider giving the repository a star.
