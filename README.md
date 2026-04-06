# PHASE-MODULATION-AND-DEMODULATION-USING-SCILAB
AIM

To write a program for Phase Modulation and Demodulation using SCILAB and to observe and measure the phase deviation and modulation index.

APPARATUS REQUIRED

Computer with i3 Processor or higher
SCILAB Software

THEORY

Phase Modulation (PM) is a modulation technique in which the phase of the carrier signal is varied in accordance with the instantaneous amplitude of the modulating signal, while the amplitude of the carrier remains constant.

Phase Deviation (Δφ)

Phase deviation represents the maximum change in phase of the carrier signal.

Δφ = kp * Am

Where:

kp = Phase sensitivity (rad/volt)
Am = Amplitude of modulating signal
Modulation Index (mp)
mp = Δφ

For sinusoidal signals:

mp = kp * Am
PM Signal Equation
s(t) = Ac cos(2πfc t + kp m(t))

For sinusoidal modulating signal:

s(t) = Ac cos(2πfc t + mp sin(2πfm t))

Where:

Ac = Carrier amplitude
fc = Carrier frequency
fm = Modulating frequency
kp = Phase sensitivity
mp = Modulation index

ALGORITHM

Define parameters:
Sampling frequency Fs
Time duration T
Carrier frequency fc
Modulating frequency fm
Phase sensitivity kp
Generate signals:
m(t) = sin(2πfm t)
c(t) = cos(2πfc t)
PM Modulation:
s(t) = cos(2πfc t + kp * m(t))
PM Demodulation:
Differentiate the PM signal
Apply envelope detection:
|s(t)|
Use low-pass filter to recover the original signal
Plot all signals:
Modulating signal
Carrier signal
PM signal
Demodulated signal

PROCEDURE

1.Refer to the algorithm and write the SCILAB code.

2.Open SCILAB software.

3.Create a new script file.

4.Enter the program and save it.

5.Execute the code.

6.Debug errors if any and re-run.

7.Observe the generated waveforms.

PROGRAM :
~~~
clc;
clear;
close;

Ac = 14.5;          
Am = 29;    
Fc = 5260;        
Fm = 526;         
Fs = 52600;      
kp = %pi/4;       

t = 0:1/Fs:2/Fm;  

E1 = Am * sin(2*%pi*Fm*t);
subplot(3,1,1);
plot(t, E1);
xlabel("Time (s)");
ylabel("Amplitude");
title("Message Signal");

E2 = Ac * sin(2*%pi*Fc*t);
subplot(3,1,2);
plot(t, E2);
xlabel("Time (s)");
ylabel("Amplitude");
title("Carrier Signal");


E3 = Ac * sin(2*%pi*Fc*t + kp*E1);
subplot(3,1,3);
plot(t, E3);
xlabel("Time (s)");
ylabel("Amplitude");
title("Phase Modulated Signal");

xgrid();
~~~

MODEL GRAPHS :

<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/2aaee069-8ee3-4bec-94e2-c6139d98f9e2" />


TABULATIONS :

<img width="756" height="1280" alt="image" src="https://github.com/user-attachments/assets/ae6c47ac-3be6-41e6-98d4-206f01f05473" />




RESULT :

<img width="866" height="1600" alt="image" src="https://github.com/user-attachments/assets/a76033a2-2115-4590-a11e-0c27d6a5bb4d" />

