# EMG-Hand-Movement-Analysis  
This repository contains the analysis of sEMG (Surface Electromyography) data from the Ninapro Dataset. The focus is on processing and analyzing the S1-1-E1.mat file, which contains EMG signals recorded from 10 electrodes while performing various hand movements.  

## Dataset Overview  
- Dataset Name: Ninapro (Non-Invasive Adaptive Prosthetics)  
- Subjects: 27 healthy individuals  
- Data Collected:  
  - sEMG signals (10 electrodes)  
  - Kinematic data from a Cyberglove  
- Movements: 52 different hand gestures  

## Files in This Repository  
- S1-A1-E1.mat → MATLAB file containing raw EMG signals for Subject 1.  
- EMG_Analysis.ipynb → Jupyter Notebook for preprocessing, filtering, feature extraction, and visualization.  
- README.md → Documentation of this project.    

## Methods Used  
### Data Preprocessing  
- Loaded .mat file and extracted EMG signals.  
- Applied band-pass filtering (10Hz - 500Hz) to remove noise.  
- Applied notch filtering (50Hz) to remove power line interference.  

### Feature Extraction  
- Time-domain features: Mean Absolute Value (MAV), Root Mean Square (RMS), Variance.  
- Frequency-domain features: Fast Fourier Transform (FFT) for spectral analysis.  
- Time-Frequency analysis: Wavelet Transform for better insight into muscle activity.  

### Visualization  
- Plotted raw and filtered EMG signals.  
- Created spectrograms and wavelet transforms for better movement analysis.  

## Results  
- Successfully processed and extracted features from the S1-A1-E1.mat file.  
- Generated filtered EMG plots, FFT graphs, and spectrograms.  
- Prepared a dataset for machine learning-based classification (future scope).
  
##  References  
- Atzori et al., "Characterization of a Benchmark Database for Myoelectric Movement Classification", IEEE Transactions on Neural Systems and Rehabilitation Engineering, 2014.  
- Gijsberts et al.,"Electromyography data for non-invasive naturally-controlled robotic hand prostheses", Scientific Data, 2014.  

