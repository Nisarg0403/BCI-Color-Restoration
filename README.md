# 🧠 BCI-Color-Restoration

> **A Brain-Computer Interface (BCI) research project investigating EEG-based SSVEP decoding, frequency-to-color encoding, source localization using sLORETA, and targeted cortical stimulation using tACS toward future cortical color restoration systems.**

---

# 📖 Project Overview

The human visual system processes light through the eyes and converts it into electrical signals that are interpreted by the visual cortex located in the occipital lobe of the brain. Brain-Computer Interfaces (BCIs) provide an opportunity to directly measure these neural responses using Electroencephalography (EEG) and potentially communicate information back to the brain using non-invasive stimulation techniques.

This project explores an end-to-end computational framework for:

- Acquiring brain activity using EEG
- Detecting Steady-State Visual Evoked Potentials (SSVEP)
- Decoding visual stimulus frequencies
- Designing a novel frequency-to-color encoding framework
- Localizing cortical activity using sLORETA
- Investigating targeted stimulation using tACS

Rather than claiming to restore color perception, this project focuses on building the computational and signal-processing framework that could support future cortical color restoration research.

---

# 🎯 Project Objectives

The primary objectives of this project are:

- Understand Brain-Computer Interface (BCI) systems.
- Study EEG signal acquisition and processing.
- Learn SSVEP-based visual BCIs.
- Develop an EEG preprocessing pipeline.
- Implement frequency detection algorithms.
- Design a frequency-to-color encoding framework.
- Explore source localization using sLORETA.
- Investigate targeted cortical stimulation using tACS.
- Build a research foundation for future color restoration systems.

---

# 🔬 Research Motivation

Current visual prosthetic systems primarily focus on restoring basic visual perception such as brightness, shapes, or object detection.

Very little research exists on computational frameworks capable of representing color information through cortical stimulation.

This project aims to investigate one possible approach by combining EEG-based signal decoding with a novel frequency-to-color encoding strategy and targeted brain stimulation techniques.

---

# 💡 Proposed Research Workflow

```text
Visual Stimulus
        │
        ▼
     Human Eye
        │
        ▼
Visual Cortex (Occipital Lobe)
        │
        ▼
        EEG
        │
        ▼
Signal Acquisition
        │
        ▼
Preprocessing
        │
        ▼
Feature Extraction
        │
        ▼
Frequency Detection
(FFT / CCA / FBCCA / TRCA)
        │
        ▼
Frequency-to-Color Encoding
        │
        ▼
Source Localization (sLORETA)
        │
        ▼
Targeted Brain Stimulation (tACS)
        │
        ▼
Future Cortical Color Restoration
```

---

# 🧠 Core Concepts

This project combines multiple interdisciplinary domains:

- Brain-Computer Interface (BCI)
- Electroencephalography (EEG)
- Steady-State Visual Evoked Potentials (SSVEP)
- Digital Signal Processing
- Machine Learning
- Computational Neuroscience
- Source Localization
- Brain Stimulation

---

# 🛠 Technology Stack

| Category | Technology |
|----------|------------|
| Programming Language | Python |
| EEG Processing | MNE-Python |
| Numerical Computing | NumPy |
| Signal Processing | SciPy |
| Data Analysis | Pandas |
| Visualization | Matplotlib |
| Machine Learning | Scikit-learn |
| Deep Learning (Future) | PyTorch |
| Source Localization | sLORETA |
| Brain Stimulation | tACS |

---

# 📂 Repository Structure

```
BCI-Color-Restoration/

├── README.md
├── docs/
├── datasets/
├── notebooks/
├── src/
├── papers/
├── results/
├── presentations/
├── requirements.txt
└── .gitignore
```

---

# 📚 Documentation

The `docs/` directory contains detailed documentation for every topic studied during the project.

Topics include:

- Project Overview
- Brain Computer Interface
- EEG Fundamentals
- EEG Signal Processing
- SSVEP
- MNE-Python
- Dataset Analysis
- Frequency Detection Algorithms
- Source Localization
- tACS
- Weekly Learning Notes

---

# 📈 Algorithms Planned

Signal Processing

- Butterworth Filter
- FFT
- Peak Detection

Feature Extraction

- ICA
- CCA

Advanced Methods

- FBCCA
- TRCA

Future Research

- Deep Learning Models
- Source Localization
- Cortical Stimulation

---

# 📊 Dataset

The project currently explores publicly available SSVEP datasets including:

- Official MNE SSVEP Example Dataset
- Wang et al. (2016) SSVEP Benchmark Dataset (planned)

These datasets are used for understanding EEG signal processing and validating frequency detection algorithms.

---

# 🚧 Current Progress

## Completed

- Brain Computer Interface Fundamentals
- EEG Fundamentals
- SSVEP Fundamentals
- MNE-Python Introduction
- Raw Object Understanding
- Official MNE SSVEP Dataset Exploration

## In Progress

- Dataset Selection
- Signal Preprocessing

## Planned

- Butterworth Filtering
- FFT Implementation
- CCA
- FBCCA
- TRCA
- Frequency-to-Color Encoding
- sLORETA
- tACS Integration

---

# ⚠ Research Disclaimer

This repository represents an ongoing academic research project.

The current work focuses on developing an EEG decoding and frequency-to-color encoding framework.

The project **does not claim to restore human color vision**. Instead, it investigates computational methods that may contribute to future research on cortical color restoration using non-invasive brain stimulation.

---

# 📄 License

This repository is intended for academic and research purposes.