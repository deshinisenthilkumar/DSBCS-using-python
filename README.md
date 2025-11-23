# DSBCS-using-python

# Aim
To write a program to perform Double Sideband Suppressed Carrier (DSB-SC) modulation and demodulation using Python, and study its spectral characteristics.

# Apparatus Required
Software: Python with NumPy, SciPy, and Matplotlib libraries

Hardware: Personal Computer

# Theory
Double Sideband Suppressed Carrier (DSB-SC) modulation is a type of amplitude modulation where the carrier is suppressed, and only the two sidebands (upper and lower) carry information. The modulated signal is given by:

# Algorithm
Define Parameters:
Sampling frequency (Fs)
Time duration (T)
Carrier frequency (Fc)
Message frequency (Fm)
Amplitude (A)
Generate Signals:

Message signal → sinusoidal
Carrier signal → high-frequency sinusoidal
DSB-SC Modulation:

Multiply the message and carrier signals to obtain the modulated signal
DSB-SC Demodulation:

Multiply the modulated signal again by the carrier
Apply a Butterworth low-pass filter to recover the original message signal
Visualization:

Plot the message signal, carrier signal, DSB-SC modulated signal, and demodulated signal
# Python Code
```
import numpy as np
import matplotlib.pyplot as plt
Am = 4.2;
fm = 359;
Ac = 8.4;
fc = 3590;
fs = 35900;
t=np.arange(0,2/fm,1/fs)
m = np.cos(2 * np.pi * fm * t)
c=np.cos(2*np.pi*fc*t)
s1 = (Ac + m) * np.cos(2 * np.pi * fc * t)
s2 = (Ac - m) * np.cos(2 * np.pi * fc * t)
s = s1 - s2
s = m * c
plt.subplot(3,1,1)
plt.plot(t, m)

plt.subplot(3,1,2)
plt.plot(t,c)

plt.subplot(3,1,3)
plt.plot(t,s)
```

# Output
<img width="672" height="508" alt="Screenshot 2025-11-23 095402" src="https://github.com/user-attachments/assets/27235a01-3f6a-4bcd-a4a4-173604f98b6b" />

# Tabulation
![WhatsApp Image 2025-11-23 at 09 56 15_e82f977c](https://github.com/user-attachments/assets/a9cbb6f8-1728-460f-8d84-a1739b73df30)


# Result
Thus, the DSB-SC-AM modulation and demodulation were implemented using Python (NumPy, SciPy, and Matplotlib), and their spectral characteristics were successfully studied.
