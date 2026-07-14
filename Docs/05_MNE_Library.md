# MNE-Python Library

---


# 1. Introduction

MNE-Python is an open-source Python library designed for processing and analyzing neurophysiological data such as:

- Electroencephalography (EEG)
- Magnetoencephalography (MEG)
- Electrocorticography (ECoG)
- Functional Near-Infrared Spectroscopy (fNIRS)

The name **MNE** originally stands for:

> **Magnetoencephalography and Electroencephalography**

The library provides tools for reading, organizing, visualizing, and processing brain signal data.

---

# 2. Why Was MNE Developed?

EEG data can be stored in many different formats and often contains large amounts of metadata.

Without specialized libraries, researchers would need to:

- Read EEG files manually.
- Parse different file formats.
- Extract channel information.
- Organize metadata.
- Implement preprocessing tools from scratch.

MNE simplifies these tasks by providing ready-to-use functions for handling neurophysiological data.

---

# 3. Why Did We Explore MNE?

The primary purpose of using MNE in this project was educational and exploratory.

MNE helped us:

- Understand how EEG data is stored.
- Learn the structure of EEG recordings.
- Inspect channel information.
- Understand sampling frequency and metadata.
- Explore publicly available SSVEP datasets.

At the current stage of the project, MNE is being used as a learning and exploration tool rather than as a mandatory component of the final system.

---

# 4. Supported File Formats

MNE supports multiple neurophysiological file formats, including:

- BrainVision (.vhdr, .eeg, .vmrk)
- EDF (.edf)
- FIF (.fif)
- BDF (.bdf)
- EEGLAB (.set)

The official MNE SSVEP example dataset uses the:

```text
BrainVision Format
```

which consists of three files:

- .vhdr → Header information
- .eeg → EEG signal data
- .vmrk → Marker information

---

# 5. The Raw Object

The most important concept in MNE is the **Raw Object**.

When an EEG dataset is loaded, MNE creates an object called:

```python
raw
```

Example:

```python
raw = mne.io.read_raw_brainvision(...)
```

The Raw object acts as a container that stores:

- EEG signals
- Channel information
- Sampling frequency
- Recording duration
- Measurement metadata

---

# 6. Information Stored in the Raw Object

The Raw object contains two main components.

## EEG Signals

The recorded voltage values from all channels.

## Metadata

Information describing the recording.

Examples:

- Channel names
- Number of channels
- Sampling frequency
- Recording duration
- Measurement date

---

# 7. Exploring an SSVEP Dataset Using MNE

During the initial phase of this project, MNE was used to load and inspect the official SSVEP example dataset.

The following output was obtained:

```text
<RawBrainVision |
sub-02_ses-01_task-ssvep_eeg.eeg,
32 x 467580 (467.6 s),
~114.2 MiB,
data loaded>
```

This information means:

| Item | Meaning |
|------|---------|
| 32 | Number of EEG channels |
| 467580 | Total recorded samples |
| 467.6 s | Recording duration |
| Data Loaded | EEG recording has been loaded into memory |

This exploration helped us understand how EEG recordings are organized before beginning signal processing.

---

# 8. The raw.info Object

The metadata of an EEG recording is stored inside:

```python
raw.info
```

Important information includes:

| Field | Description |
|--------|-------------|
| ch_names | Names of EEG channels |
| nchan | Number of channels |
| sfreq | Sampling frequency |
| meas_date | Recording date |
| bads | Bad channels |

Example output:

```text
nchan: 32
sfreq: 1000.0 Hz
chs: 32 EEG
```

This information provides a summary of the EEG recording.

---

# 9. Accessing EEG Data

The actual EEG signals can be obtained using:

```python
data = raw.get_data()
```

The returned data is typically organized as:

```text
Channels × Samples
```

For example:

```text
32 × 467580
```

This means:

- 32 EEG channels
- 467580 recorded samples

---

# 10. Why Is MNE Useful?

MNE allows researchers to focus on signal processing and analysis rather than spending time handling low-level file operations.

Without MNE:

```text
Read files manually
↓
Parse metadata manually
↓
Extract channels manually
↓
Write utility functions
```

With MNE:

```text
Load dataset
↓
Access EEG signals
↓
Inspect metadata
↓
Begin analysis
```

This significantly reduces development time.

---

# 11. MNE in Our Learning Journey

The role of MNE in this project is currently:

```text
Dataset
     ↓
MNE
     ↓
Understand EEG Structure
     ↓
Explore SSVEP Data
     ↓
Prepare for Signal Processing
```

MNE has helped us understand:

- What an EEG recording looks like.
- How EEG data is organized.
- How channels and sampling frequencies are stored.
- How SSVEP datasets can be explored.

---

# 12. Key Takeaways

- MNE-Python is an open-source library for neurophysiological data analysis.
- It supports many EEG file formats.
- The Raw object is the foundation of MNE.
- raw.info stores metadata about the recording.
- raw.get_data() returns EEG signals.
- MNE was used in this project primarily for learning and dataset exploration.

---

# Summary

MNE-Python provides a convenient way to load and inspect EEG datasets.

Although MNE is not currently a mandatory component of the final project pipeline, it has played an important role in helping us understand EEG recordings and explore publicly available SSVEP datasets.

The knowledge gained through MNE will help us implement our own signal-processing pipeline in the later stages of this project.