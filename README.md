# DeCLFPNet 
This is first version of my code for DeCLFPNet.
After submit and accept our paper,ALL details of DeCLFPNet model will be released in this repo 
author : mehdi habibi 


## 1. Problem Statement
Brain-computer interfaces (BCIs) hold transformative potential for empowering individuals with motor impairments, offering them greater independence in daily life. However, decoding neural signals related to movement parameters remains a significant challenge for real-world applications. To address this, we propose a novel deep neural network that combines a convolutional block for feature extraction and a recurrent block for decoding continuous movement and applied force from LFP signals. By streamlining the feature extraction process and generalizing across diverse datasets, our approach not only advances decoding accuracy but also enhances our understanding of the neural dynamics underlying motor control.

## 2. Related Works
### LFPs Decoding
| Date | Paper | Description | Name| Dataset|
|------|-------|-------------|--------|-----------|
| 2016 | [Continuous Force Decoding from Local Field Potentials of the Primary Motor Cortex in Freely Moving Rats](https://www.nature.com/articles/srep35238) | This paper presents a method for decoding continuous force from local field potentials (LFPs) recorded in the primary motor cortex of freely moving rats. It demonstrates the feasibility of decoding motor signals in a naturalistic setting. | Khorasani|Rats' LFP Dataset.
| 2021 | [A stack LSTM structure for decoding continuous force from local field potential signal of primary motor cortex (M1)](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03953-0#:~:text=The%20proposed%20stack%20LSTM%20structure,accurate%20and%20faster%20BCI%20systems.) | This study introduces a stacked LSTM structure for decoding continuous force signals from LFPs in the primary motor cortex (M1), enabling accurate and faster BCI systems. | kashefi|Rats' LFP Dataset.
| 2012 | [Accurate decoding of reaching movements from field potentials in the absence of spikes](https://iopscience.iop.org/article/10.1088/1741-2560/9/4/046006) | Flint used a multi-input and multi-output Wiener cascade filter| Flint | Monkey's LFP.

### Baseline models for comparison
To validate the performance of the DeCLFPNet model, we compared it with several baseline studies, including Deep Xie [15], Khorasani [2], Kashefi [21], Ridge Regression, and Lasso Regression [22]. Below is a brief description of each baseline:

- **[Deep Xie](https://iopscience.iop.org/article/10.1088/1741-2552/aa9dbe)**: Utilizes a custom CNN architecture followed by an LSTM and a fully connected layer with ReLU activation to decode finger trajectory from ECoG signals.

- **[Khorasani](https://www.nature.com/articles/srep35238)**: Employs a BCI pipeline where LFP signals are band-pass filtered into six frequency bands (δ, θ, α, β, low-γ, high-γ), rectified, and smoothed with Savitzky-Golay to extract temporal envelopes, which are then decoded using PLS regression for continuous force values.

- **[Kashefi](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03953-0)**: Proposes a stacked LSTM with two layers (30 and 15 units) connected to a fully connected neuron with ReLU activation for decoding continuous force from Rat’s LFP signals.

- **[Ridge Regression](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)**: Uses the same feature extraction pipeline as Khorasani (band-pass filtering and smoothing) but applies L2 regularization for continuous force decoding from LFP signals.

- **[Lasso Regression](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)**: Follows the same feature extraction process as Khorasani and Ridge, but uses L1 regularization for continuous force decoding from LFP signals.
## 3. The Proposed Method (DeCLFPNet)
   
## 4. Implementation
   
### 4.1. Dataset
---

### Datasets

This project utilizes two key datasets:  

#### 1. Rats' LFP Dataset  
This dataset was gathered in our neuroscience laboratory in 2016 by Khorasani et al. for the purpose of decoding the applied force of rats from 16 channels of local field potential signals.
- **Subjects**: Three Wistar rats (200–300 g).  
- **Task**: Lever pressing to receive water rewards (force range: 0–0.15 N; lever movement: 0°–90°).  
- **Recording**:  
  - LFP signals from a 4 × 4 microwire array implanted in the left hemisphere (16 channels).  
  - Recorded at 10 kHz, filtered (0.1–500 Hz), and downsampled to 1 kHz.  
- **Trials**:  
  - Rat 1: 74 trials  
  - Rat 2: 79 trials  
  - Rat 3: 80 trials  
- **Data**:  
  - LFPs: (trials, 16, 3000)  
  - Force: (trials, 3000)
 
<p align="center">
  <img src="https://github.com/user-attachments/assets/f66eb7d4-2447-4148-9e35-c6ad0d66c812" alt="Force Movement">
</p>
<p align="center"><i>Rats' LFP-Force movement</i></p>

#### 2. Monkey's LFP Dataset  
This dataset is the publicly available LFP dataset for decoding hand position
trajectories
- **Subjects**: Rhesus Monkey C.  
- **Task**: Center-out task—reaching from a central target to one of eight targets arranged in a circular pattern.  
- **Recording**:  
  - LFP signals from M1 and PMd using a 96-channel silicon microelectrode array.  
  - Neural signals bandpass-filtered (1–500 Hz) and resampled to 1 kHz.  
- **Motion Data**: Two positional dimensions aligned with LFP signals.
<p align="center">
  <img src="https://github.com/user-attachments/assets/541fd9ba-100a-41e0-9933-a7e4dfb08a1c" alt="Center-Out movement">
</p>
<p align="center"><i>Monkey's LFP-Center-Out movement</i></p>


---

### Dataset Summary Table  

| **Dataset**   | **Subject**         | **Recording**        | **Task**                |  
|---------------|---------------------|----------------------|-------------------------|  
| [Rats' LFP](https://www.nature.com/articles/srep35238)     | Three Wistar rats   | 16 LFP Channels      | Force movement          |  
| [Monkey's LFP](https://portal.nersc.gov/project/crcns/download/dream/data_sets/Flint_2012)  | One rhesus monkey   | 96 LFP Channels      | Center-out movement     |  

---


### 4.2. Model
### 4.3. Configurations
### 4.4. Training DeCLFPNet
### 4.5  Results
### 4.5. Contact
   

