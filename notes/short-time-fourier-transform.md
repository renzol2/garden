---
tags: ece-402 dsp
---

# Short-time Fourier Transform

The **Short-time Fourier transform (STFT)** is a [[fourier-transform|Fourier transform]] used to determine the [[sine-wave|sinusoidal]] [[frequency|frequencies]] and [[phase]] content of local sections of a signal as it changes over time.

- procedure for computing STFTs is to divide a longer signal into shorter segments and individually compute Fourier transforms on each segment
- each Fourier transform is then plotted onto a [[spectrogram]] or other visualization

From MUS 409:

- The **STFT** is an adaptation of the DFT meant to fit real-world, finite-duration sounds
- in preparation for analysis, the STFT breaks the input signal into short segments ([[windowing]]) and applying a particular [[amplitude]] [[envelope]]
  - usually 1 ms to 1 sec
  - amplitude windows usually overlap ("hop size" = 1, 0.5, 0.25)
  - similar windowing concept to that of grains in [[granular-synthesis|granular synthesis]]
  - Fourier analysis is then performed on each window, in sequence, treating each segment as one period of an infinite-length periodic function

## Sources

- <https://en.wikipedia.org/wiki/Short-time_Fourier_transform>
