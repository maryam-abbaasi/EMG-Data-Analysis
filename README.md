# EMG Hand Movement Analysis using Ninapro Dataset (DB1)

## Project Overview

This repository presents a complete signal processing and feature extraction pipeline for **surface Electromyography (sEMG)–based hand movement analysis** using the **Ninapro DB1 dataset**. The objective of this project is to preprocess raw EMG signals, extract meaningful features, and prepare a clean dataset suitable for **myoelectric control and machine learning–based hand gesture classification**.

The analysis focuses on the **S1-A1-E1.mat** file, which contains EMG recordings from **10 forearm electrodes** collected during **basic finger movement tasks**.

## Motivation

sEMG-based hand movement recognition is widely used in:

* Prosthetic hand control
* Rehabilitation engineering
* Human–computer interaction
* Assistive robotic systems

The Ninapro dataset is a benchmark dataset in this domain. This project aims to provide a **clear, reproducible, and well-documented workflow** for EMG signal analysis that can be easily extended for classification tasks.

## Dataset Description

**Dataset Name:** Ninapro (Non-Invasive Adaptive Prosthetics)
**Database:** DB1
**Subjects:** 27 healthy individuals
**Electrodes:** 10 Otto Bock MyoBock 13E200 sEMG electrodes
**Movements:** 52 hand gestures plus rest position

### Exercises

* **Exercise A:** Basic finger movements
* **Exercise B:** Isometric, isotonic, and wrist movements
* **Exercise C:** Functional grasping movements

### Dataset Variables

Each MATLAB file contains the following synchronized variables:

* **Subject:** Subject identifier
* **Exercise:** Exercise number
* **Emg (10 channels):** sEMG signals recorded from the forearm
* **Glove (22 channels):** Raw Cyberglove sensor data
* **Stimulus:** Movement label shown to the subject
* **Restimulus:** Refined movement label after relabeling
* **Repetition:** Repetition index of stimulus
* **Rerepetition:** Repetition index of restimulus

## Methods

### Data Loading

* MATLAB `.mat` files were loaded using Python.
* EMG signals and movement labels were extracted for analysis.

### Signal Preprocessing

* **Band-pass filtering (10–500 Hz):** Removes motion artifacts and high-frequency noise.
* **Notch filtering (50 Hz):** Eliminates power-line interference.

### Feature Extraction

#### Time-Domain Features

* Mean Absolute Value (MAV)
* Root Mean Square (RMS)
* Variance

#### Frequency-Domain Features

* Fast Fourier Transform (FFT) for spectral analysis

#### Time–Frequency Analysis

* Wavelet Transform for analyzing non-stationary EMG signals


## Visualization

* Raw and filtered EMG signal plots
* FFT magnitude plots
* Spectrograms and wavelet scalograms

## Results

* EMG signals were successfully filtered and denoised.
* Time-domain, frequency-domain, and time–frequency features were extracted.
* A structured dataset suitable for **machine learning–based hand gesture classification** was prepared.


## How to Run

* Open Google Colab
* Upload the notebook `EMG_Analysis.ipynb`
  or upload the notebook directly from your GitHub repository

Install Required Python Libraries:

Run the following command in a Colab cell to install all required dependencies:

```python
!pip install numpy scipy matplotlib pandas pywavelets scikit-learn

* Upload the `S1-A1-E1.mat` file to Colab
  **OR**
* Mount Google Drive and load the dataset from Drive
* Execute all cells sequentially
* The notebook will perform:

  * EMG signal loading
  * Preprocessing and filtering
  * Feature extraction
  * Visualization and analysis

The project was developed and executed entirely on Google Colab. No local Python installation is required. The workflow is fully reproducible on cloud-based environments

## Future Work

* Extend analysis to all subjects (S1–S27).
* Implement machine learning and deep learning classifiers.
* Perform EMG channel selection and feature optimization.
* Develop real-time EMG-based gesture recognition systems.

## References

1. Atzori et al., *Characterization of a Benchmark Database for Myoelectric Movement Classification*, IEEE Transactions on Neural Systems and Rehabilitation Engineering, 2014.
2. Gijsberts et al., *Electromyography data for non-invasive naturally-controlled robotic hand prostheses*, Scientific Data, 2014.

