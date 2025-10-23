# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program
```
clc;
clear;
close;
Ac=16.6;
Am=8.3;
Fc=4000;
Fm=400;
Fs=50000;
t=0:1/Fs:2/Fm;
wm=2*3.14*Fm;
wc=2*3.14*Fc;
E1=Am*sin(2*3.14*Fm*t);
subplot(3,1,1);
plot(t,E1);
xlabel("Time(s)");
ylabel("Amplitude");
title("Message Signal m(t)");
E2=Ac*sin(2*3.14*Fc*t);
subplot(3,1,2);
plot(t,E2);
xlabel("Time(s)");
ylabel("Amplitude");
title("Carrier Signal c(t)");
E3=((Am/2)*cos((wc-wm)*t))-((Am/2)*cos((wc+wm)*t));
subplot(3,1,3)
plot(t,E3);
xlabel("Time(s)");
ylabel("Amplitude");
title("DSB-SC Modulated Signal s(t)");
xgrid();
```
Output Graph
<img width="1612" height="835" alt="image" src="https://github.com/user-attachments/assets/8cae6ddf-0b6b-41e0-ba61-daab2cfdd0e0" />

Tablular Column
<img width="1048" height="953" alt="image" src="https://github.com/user-attachments/assets/e7ba619a-3f56-4123-b7e5-57294441c340" />






<img width="661" height="916" alt="image" src="https://github.com/user-attachments/assets/e308b838-6a91-435d-96b0-90f89c1fc16d" />

Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

