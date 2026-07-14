# Dataset Analysis

---


# 1. Introduction

Developing and testing Brain-Computer Interface (BCI) algorithms requires large amounts of EEG data. Since collecting EEG recordings manually requires specialized hardware and participants, publicly available datasets are commonly used in research.

For this project, publicly available SSVEP datasets are being explored to:

- Understand the structure of EEG recordings.
- Learn how SSVEP data is organized.
- Develop and test signal processing algorithms.
- Validate the proposed frequency-to-color encoding framework.

At the current stage, two datasets have been explored or considered for this project:

1. Official MNE SSVEP Example Dataset
2. Wang et al. (2016) SSVEP Benchmark Dataset

---

# 2. Official MNE SSVEP Example Dataset

The official MNE SSVEP dataset was used during the initial phase of the project to understand EEG data and become familiar with the MNE-Python library.

The dataset is stored in the BrainVision format and consists of three files:

```text
.vhdr  → Header Information
.eeg   → EEG Signal Data
.vmrk  → Marker Information
```

The dataset was loaded using MNE and produced the following information:

```text
<RawBrainVision |
32 x 467580 (467.6 s),
~114.2 MiB,
data loaded>
```

This information indicates:

| Property | Value |
|-----------|--------|
| Number of Channels | 32 |
| Number of Samples | 467580 |
| Recording Duration | 467.6 seconds |
| Sampling Frequency | 1000 Hz |

---

# 3. Information Obtained from the Dataset

The MNE dataset helped us understand several important concepts:

- EEG recordings contain multiple channels.
- Each channel records voltage values over time.
- EEG data is accompanied by metadata such as sampling frequency and channel names.
- Brain signals can be organized and inspected using specialized libraries such as MNE.

The dataset served primarily as an educational and exploratory resource.

---

# 4. Wang et al. (2016) SSVEP Benchmark Dataset

The Wang et al. (2016) dataset is one of the most widely used benchmark datasets in SSVEP research.

This dataset is currently being considered as the primary dataset for this project because:

- It contains recordings from multiple participants.
- It provides multiple visual stimulation frequencies.
- It is widely used in SSVEP literature.
- It is suitable for evaluating frequency detection algorithms such as:
  - FFT
  - CCA
  - FBCCA
  - TRCA

This dataset is expected to become the main dataset for algorithm development and experimentation.

---

# 5. Dataset Structure

During dataset exploration, the following keys were observed:

```python
dict_keys([
'__header__',
'__version__',
'__globals__',
'X',
'Y'
])
```

The variables represent:

| Variable | Description |
|-----------|-------------|
| X | EEG recordings |
| Y | Labels corresponding to the recordings |

The dataset shapes obtained during exploration were:

```python
X.shape = (278, 64, 3000)
Y.shape = (278, 1)
```

This means:

- 278 EEG recordings (trials)
- 64 EEG channels
- 3000 samples per channel
- One label for each recording

---

# 6. Understanding the Dataset Dimensions

The shape:

```python
(278, 64, 3000)
```

can be interpreted as:

```text
(Number of Trials,
 Number of Channels,
 Number of Samples)
```

Therefore:

```text
278 trials
        ↓
64 channels per trial
        ↓
3000 voltage values per channel
```

This structure is ideal for implementing and testing signal processing algorithms.

---

# 7. Role of the Dataset in Our Project

The datasets explored in this project serve different purposes.

## MNE SSVEP Dataset

Purpose:

- Understanding EEG recordings.
- Learning MNE-Python.
- Exploring metadata and file formats.

## Wang Benchmark Dataset

Purpose:

- Implementing signal processing algorithms.
- Detecting SSVEP frequencies.
- Comparing different algorithms.
- Developing the frequency-to-color encoding framework.

---

# 8. Project Workflow Using Datasets

```text
Dataset
      ↓
Understand EEG Structure
      ↓
Load EEG Signals
      ↓
Preprocess Signals
      ↓
Detect Frequencies
      ↓
Frequency-to-Color Encoding
```

The datasets therefore act as the foundation for the development and evaluation of the proposed system.

---

# 9. Key Takeaways

- Public SSVEP datasets are essential for developing and testing BCI algorithms.
- The official MNE SSVEP dataset was used for learning and exploration.
- The Wang et al. (2016) dataset is being considered as the primary experimental dataset.
- EEG recordings are organized as trials, channels, and samples.
- Understanding the dataset structure is necessary before implementing signal processing algorithms.

---

# Summary

The exploration of publicly available SSVEP datasets has provided an understanding of how EEG recordings are stored and organized.

The MNE dataset was used to learn the structure of EEG data and understand metadata, while the Wang et al. (2016) benchmark dataset is expected to serve as the primary dataset for algorithm development and validation of the proposed frequency-to-color encoding framework.