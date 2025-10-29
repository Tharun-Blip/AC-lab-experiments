# Amplitude Modulation using Python

## Aim:

To implement and analyze amplitude modulation (AM) using Python's NumPy and Matplotlib libraries. 

## Theory:

Amplitude Modulation (AM) is a technique used in electronic communication, primarily for transmitting information via a radio carrier wave. In AM, the amplitude of the carrier wave is varied in proportion to that of the message signal. The general form of an AM signal is:

   <img width="460" height="332" alt="image" src="https://github.com/user-attachments/assets/ec25ee8e-310c-48d9-8050-df6a273a1476" />

## Algorithm:

1.	Initialize Parameters: Set the values for carrier frequency, message frequency, and sampling frequency.
2.	Generate Time Axis: Create a time vector for the signal duration.
3.	Generate Message Signal: Define the message signal as a cosine wave.
4.	Generate Carrier Signal: Define the carrier signal as a cosine wave.
5.	Modulate Signal: Apply the AM formula to obtain the modulated signal.
6.	Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.


## Program:
```
import numpy as np
import matplotlib.pyplot as plt

am = 4.5
ac = 9.0
fm = 344
fc = 3440
t = np.arange(0, 0.01, 1e-6)
mt = am * np.sin(2 * np.pi * fm * t)
ct = ac * np.sin(2 * np.pi * fc * t)
st = ac * (1 + (am/ac) * np.sin(2 * np.pi * fm * t)) * np.sin(2 * np.pi * fc * t)
plt.figure()
plt.subplot(3,1,1)
plt.plot(t, mt)
plt.title('Message Signal')
plt.subplot(3,1,2)
plt.plot(t, ct)
plt.title('Carrier Signal')
plt.subplot(3,1,3)
plt.plot(t, st)
plt.title('AM Signal')
plt.tight_layout()
plt.show()
```


## Output Waveform:
<img width="787" height="583" alt="image" src="https://github.com/user-attachments/assets/d4679053-c787-40e7-907a-b9090fe634bb" />

## Tabulation:
![WhatsApp Image 2025-10-29 at 19 00 08_63eb8e66](https://github.com/user-attachments/assets/62f96a13-0305-4383-a160-5736d17b25bc)

## Result:

The message signal, carrier signal, and amplitude modulated (AM) signal will be displayed in separate plots. Thus AM is implemented using numPy and Matplotlib.




