# EX NO: 2 DSB-SC-AM MODULATOR AND DEMODULATOR

### Aim:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

### Equiptments Required:

• Computer 

• SCI LAB

Note: Keep all the switch faults in off position

### Algorithm:

#### Define Parameters: 
  • Fs: Sampling frequency.
  
  • T: Duration of the signal.
  
  • Fc: Carrier frequency. 
  
  • Fm: Frequency of the message signal.
  
  • Amplitude: Maximum amplitude of the message signal.
  
#### Generate Signals: 
  • Message Signal: A sinusoidal signal that will be modulated. 
  
  • Carrier Signal: A high-frequency sinusoidal signal used for modulation.
#### DSBSC Modulation: 

  • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
  
#### DSBSC Demodulation: 
  • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). 
  
  • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
  
#### Visualization: 

  Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation. 
  
### Procedure:
  • Refer Algorithms and write code for the experiment. 
  
  • Open SCILAB in System.
  
  • Type your code in New Editor.
  
  • Save the file.

  • Execute the code 
  • If any Error, correct it in code and execute again 
  • Verify the generated waveform using Tabulation and Model Waveform

### Model Waveform:

<img width="563" height="543" alt="image" src="https://github.com/user-attachments/assets/3d89769e-6e86-4464-a88b-8fd3f360fed5" />

### Program:
~~~
Am=8.22;
Ac=16.44;
fm=857;
fc=8570;
fs=85700;
t=0:1/fs:2/fm;
em=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,em);
ec=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,ec);
eAM1=(Ac+em).*cos(2*3.14*fc*t);
eAM2=(Ac-em).*cos(2*3.14*fc*t);
edsbsc=eAM1-eAM2;
subplot(3,1,3);
plot(t,edsbsc);
~~~

### Output Graph:

<img width="761" height="721" alt="image" src="https://github.com/user-attachments/assets/e45ecd6b-ec68-490a-91d6-c30b24d82df6" />

### Tabular Column:

<img width="857" height="1600" alt="image" src="https://github.com/user-attachments/assets/c5ab4878-819e-44a3-bfa8-8c137d20a866" />

### Result:
Thus the DSB-SC-AM Modulation and Demodulation is generated.
#
