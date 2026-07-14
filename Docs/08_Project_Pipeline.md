# Project Pipeline

---


# 1. Introduction

This document describes the complete workflow of the proposed Brain-Computer Interface (BCI) system.

The project aims to:

1. Record brain activity using EEG.
2. Detect SSVEP frequencies.
3. Convert detected frequencies into computational color representations.
4. Explore future integration with source localization and cortical stimulation techniques.

The current project focuses primarily on the computational framework and signal processing pipeline.

---

# 2. Overall Project Pipeline

```text
Flickering Visual Stimulus
            ↓
          Human Eye
            ↓
        Visual Cortex
            ↓
      SSVEP Generation
            ↓
      EEG Acquisition
            ↓
      Signal Processing
            ↓
     Frequency Detection
            ↓
 Frequency-to-Color Encoding
            ↓
     Future sLORETA
            ↓
       Future tACS
            ↓
 Future Cortical Color Restoration
```

---

# 3. Step 1 – Visual Stimulation

The process begins with a visual stimulus.

A light source or screen displays visual targets flickering at specific frequencies.

Example:

| Target | Frequency |
|---------|------------|
| A | 8 Hz |
| B | 10 Hz |
| C | 12 Hz |
| D | 15 Hz |

The user focuses on one of these targets.

---

# 4. Step 2 – SSVEP Generation

When the user observes a flickering target, neurons in the visual cortex begin responding at approximately the same frequency.

Example:

```text
Visual Stimulus = 10 Hz
        ↓
Brain Response ≈ 10 Hz
```

This electrical response is called the Steady-State Visual Evoked Potential (SSVEP).

---

# 5. Step 3 – EEG Acquisition

The SSVEP response is recorded using an EEG device.

The EEG machine records:

- Voltage signals
- Multiple channels
- Time-series data

Channels near the occipital lobe are especially important:

- O1
- O2
- Oz

---

# 6. Step 4 – Signal Preprocessing

Raw EEG signals contain noise and unwanted frequencies.

Therefore, preprocessing techniques are applied.

Planned techniques include:

- Butterworth Filter
- ICA (optional)

The objective is to improve the quality of the EEG signal before frequency analysis.

---

# 7. Step 5 – Frequency Detection

After preprocessing, signal processing algorithms are used to detect the SSVEP frequency.

Planned algorithms:

### Basic Methods

- FFT
- Peak Detection

### Intermediate Methods

- CCA

### Advanced Methods

- FBCCA
- TRCA

The output of this stage is:

```text
Detected Frequency
```

For example:

```text
10 Hz
```

---

# 8. Step 6 – Frequency-to-Color Encoding

The detected frequency becomes the input to the proposed encoding framework.

```text
Detected Frequency
        ↓
Encoding Algorithm
        ↓
Color Representation
```

This encoding process is a computational representation and does not imply that EEG frequencies are the physical frequencies of visible light.

The purpose of this stage is to investigate methods of representing color information computationally.

---

# 9. Future Phase – Source Localization

Once a computational color representation has been generated, future work may investigate source localization techniques.

Planned method:

```text
sLORETA
```

The objective is to identify brain regions associated with visual processing.

---

# 10. Future Phase – Brain Stimulation

Future research may investigate:

```text
Transcranial Alternating Current Stimulation (tACS)
```

The goal is to explore whether computationally encoded information can eventually contribute to future cortical color restoration systems.

This phase is exploratory and lies outside the scope of the current implementation.

---

# 11. Current Scope of the Project

The current implementation focuses on:

```text
EEG
↓
SSVEP
↓
Signal Processing
↓
Frequency Detection
↓
Encoding Framework
```

The following components are considered future work:

- sLORETA
- tACS
- Human stimulation experiments
- Clinical validation

---

# 12. Technologies Used

| Component | Technology |
|-----------|-------------|
| Programming Language | Python |
| EEG Exploration | MNE-Python |
| Numerical Computing | NumPy |
| Signal Processing | SciPy |
| Visualization | Matplotlib |
| Machine Learning | Scikit-Learn |

---

# 13. Expected Outputs

The project aims to produce:

- EEG preprocessing pipeline.
- SSVEP frequency detection system.
- Comparison of frequency detection algorithms.
- Frequency-to-color encoding framework.
- Research documentation for future cortical stimulation studies.

---

# 14. Project Workflow Summary

```text
Visual Stimulus
       ↓
SSVEP Response
       ↓
EEG Recording
       ↓
Signal Processing
       ↓
Frequency Detection
       ↓
Color Encoding
       ↓
Future Brain Stimulation Research
```

---

# Key Takeaways

- The project is divided into multiple stages.
- The current focus is EEG processing and SSVEP frequency detection.
- Frequency detection algorithms form the core of the system.
- The encoding framework is the primary research contribution.
- sLORETA and tACS are future research directions.

---

# Summary

This document presents the complete architecture of the proposed Brain-Computer Interface system.

The current work focuses on building an EEG-based SSVEP detection and frequency-to-color encoding framework, which may serve as a computational foundation for future research in cortical color restoration and targeted brain stimulation.