# LFPRegNet 
This is first version of my code for LFPRegNet that paper will be publish in ieee transaction on industrial informatics 
author : mehdi habibi 
 3 december 2024 

## 1. Problem Statement
Brain-computer interfaces (BCIs) hold transformative potential for empowering individuals with motor impairments, offering them greater independence in daily life. However, decoding neural signals related to movement parameters remains a significant challenge for real-world applications. To address this, we propose a novel deep neural network that combines a convolutional block for feature extraction and a recurrent block for decoding continuous movement and applied force from LFP signals. By streamlining the feature extraction process and generalizing across diverse datasets, our approach not only advances decoding accuracy but also enhances our understanding of the neural dynamics underlying motor control.

## 2. Related Works

| Date | Paper | Description |
|------|-------|-------------|
| 2016 | [Continuous Force Decoding from Local Field Potentials of the Primary Motor Cortex in Freely Moving Rats](https://www.nature.com/articles/srep35238) | This paper presents a method for decoding continuous force from local field potentials (LFPs) recorded in the primary motor cortex of freely moving rats. It demonstrates the feasibility of decoding motor signals in a naturalistic setting. |
| 2019 | [Nonlinear sparse partial least squares: an investigation of the effect of nonlinearity and sparsity on the decoding of intracranial data](https://iopscience.iop.org/article/10.1088/1741-2552/ab5d47) | This work explores how nonlinearity and sparsity in sparse partial least squares models influence the decoding accuracy of intracranial neural data. |
| 2020 | [State-based decoding of force signals from multi-channel local field potentials](https://ieeexplore.ieee.org/abstract/document/9177005) | This paper proposes a state-based approach for decoding force signals using multi-channel local field potentials, achieving robust decoding accuracy. |
| 2021 | [A stack LSTM structure for decoding continuous force from local field potential signal of primary motor cortex (M1)](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-020-03953-0#:~:text=The%20proposed%20stack%20LSTM%20structure,accurate%20and%20faster%20BCI%20systems.) | This study introduces a stacked LSTM structure for decoding continuous force signals from LFPs in the primary motor cortex (M1), enabling accurate and faster BCI systems. |


## 3. The Proposed Method
   
## 4. Implementation
   
### 4.1. Dataset
This datasets contain three rats , this data was recorded by khorasani ,2016
Here's the final text tailored for a GitHub repository. It's concise, informative, and formatted for easy readability in Markdown:

---

### Datasets

This project utilizes two key datasets:  

#### 1. Rats' LFP Dataset  
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

#### 2. Monkey's LFP Dataset  
- **Subjects**: Rhesus Monkey C.  
- **Task**: Center-out task—reaching from a central target to one of eight targets arranged in a circular pattern.  
- **Recording**:  
  - LFP signals from M1 and PMd using a 96-channel silicon microelectrode array.  
  - Neural signals bandpass-filtered (1–500 Hz) and resampled to 1 kHz.  
- **Motion Data**: Two positional and two velocity dimensions aligned with neural signals.
- **Center-Out Task Example**
<p align="center"> <img src="https://www.researchgate.net/publication/267930377/figure/fig1/AS:359753692794888@1462783373018/Center-out-task-kinematics-The-trajectories-show-the-position-of-the-tip-of-the-index.png" alt="Center-out task example" width="500"> </p> <p align="center"><i>Center-out task</i></p>

![Center-out-task-kinematics-The-trajectories-show-the-position-of-the-tip-of-the-index](https://github.com/user-attachments/assets/aa2155d2-bca5-4555-b3ef-e712579fc668)
---

### Dataset Summary Table  

| **Dataset**   | **Subject**         | **Recording**        | **Task**                |  
|---------------|---------------------|----------------------|-------------------------|  
| Rats' LFP     | Three Wistar rats   | 16 LFP Channels      | Force movement          |  
| Monkey's LFP  | One rhesus monkey   | 96 LFP Channels      | Center-out movement     |  

---


### 4.2. Model
### 4.3. Configurations
### 4.4. Training LFPRegNet
### 4.5  Results
### 4.5. Contact
   

