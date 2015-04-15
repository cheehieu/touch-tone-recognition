touch-tone-recognition
======================

<img src="http://niftyhedgehog.com/touch-tone-recognition/images/dtmf_gui.png">

## Overview
Back when people actually dialed telephone numbers to make calls, operators utilized dual-tone multiple frequency (DTMF) touch tones to decipher which key was pressed. With DTMF, each button on the keypad was represented by a combination of two unique frequencies. The switching station could then decode the signal by running the generated tone through 8 bandpass filters. This technology was superior to pre-1960's pulse dialing techniques because DTMF could avoid harmonics and modulation problems. In today's digital VoIP world, however, these audible DTMF tones are played back for nostalgic reasons.

This Matlab-based project implements a DTMF generation and decoding algorithm using fast Fourier transforms, signal denoising, pitch extraction, and sound visualization. A graphical user interface was also developed to demonstrate the manipulation and visualization of signal data.

This project was developed in the spring of 2010 with my group (Norman Chung, Rocky Mark Juan, Alexander Nobles, and Bryce Toth) for USC's Introduction to Linear Systems (EE-301) course, taught by professor Michael Enright. 

## Software


### Matlab Algorithm
There were 5 main parts to the overall Matlab algorithm:

1. Generate DTMF touch tones
2. Parse DTMF signal
3. Filter signal
4. Scoring function
5. Decode and return result

* Input (impulse response in time domain), noise
* FFT to create frequency response in frequency domain
* Noise reduction
* Bandpass filters
* Scoring function based off frequency response amplitudes

### GUI
* User-generated touch tones
* Near real-time DTMF decoding
* Input -> output string
