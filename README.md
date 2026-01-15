# EEG Artifact Removal using RLS and IC-U-Net

This repository contains the implementation and results of a hybrid EEG artifact removal framework that combines **Recursive Least Squares (RLS) adaptive filtering** for temporal artifact suppression and an **IC-U-Net–based deep learning model** for spatial denoising of multichannel EEG signals.

The work is intended for **Brain–Computer Interface (BCI)** preprocessing and is validated using a publicly available EEG dataset.

---

## Overview

Electroencephalogram (EEG) signals are highly susceptible to physiological artifacts such as eye blinks and eye movements. This project proposes a two-stage denoising pipeline:

1. **RLS Adaptive Filtering**  
   Removes temporal artifacts caused by vertical and horizontal EOG signals.

2. **IC-U-Net Multi Architecture**  
   Learns spatial and temporal dependencies across 19 EEG channels to suppress remaining artifacts while preserving neural information.

---

##  Repository Structure

- `code.py` – Main implementation file  
- `results/` – Generated plots and evaluation results  
- `README.md` – Project documentation

---

## Methodology Summary

- EEG signals are band-pass filtered (0.5–40 Hz)
- Temporal artifacts are removed using RLS adaptive filtering with EOG reference signals
- The filtered output is processed using a multi-channel IC-U-Net for spatial artifact removal
- Performance is evaluated using Mean Squared Error (MSE) and qualitative signal analysis

Detailed mathematical formulations and architectural descriptions are available in the associated research paper.

---

## Results

The proposed framework effectively suppresses both temporal and spatial EEG artifacts.

- **Average MSE:** 0.0687  
- **Best-performing channel MSE:** 0.046  
- **Number of EEG channels:** 19 (10–20 system)  

All result figures and plots are available in the `results/` directory.

---

## Dataset

This project uses the **Mendeley EEG Artifact Dataset**.

The dataset is **not included** in this repository due to licensing restrictions.

Users must download the dataset separately and update the dataset paths in the code before execution.

---



