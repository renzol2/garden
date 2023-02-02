---
tags: ece-402 dsp cs-448
---

# Discrete Fourier Transform

A **Discrete fourier transform (DFT)** is a conversion between a discrete [[time-domain|time domain]] representation and a discrete [[frequency-domain|frequency domain]] representation of a signal.

It converts a sequence of equally-spaced discrete samples into a [[complex-number|complex]] valued function of [[frequency]].

- the resulting complex-valued function is called the **Discrete-Time Fourier Transform (DTFT)**

A signal, first represented as a real value in terms of some sample number $n$, becomes a [[complex-number|complex number]] at frequency bin $k$.

From MUS 409: a version of the [[fourier-transform|Fourier Transform]] for discrete (i.e. [[digital-audio|digital]], [[sampling-signal-processing|sampled]]) [[audio-signal|signals]]
  - can be applied to a signal of any length
  - often too slow for real-time applications
  - good for accurate, offline analysis of pre-precorded sounds

## Application

DFTs are almost always implemented using Fast Fourier Transform (FFT) algorithms, and are utilized in [[digital-signal-processing|digital signal]] and image processing applications.

## Sources

- <https://en.wikipedia.org/wiki/Discrete_Fourier_transform>
- <https://download.ni.com/evaluation/pxi/Understanding%20FFTs%20and%20Windowing.pdf>
- CS 448
