---
tags: ece-402 dsp
---

# Frequency Decomposition

**Frequency decomposition** is the process of separating a signal into its individual [[frequency|frequencies]], usually to perform some [[spectral-analysis|spectral analysis]] on the signal.

There are many practical applications to frequency decomposition, including:

- deconstructing radio waves to choose which particular radio station to listen to
- deconstructing [[audio-signal|audio signals]] into different frequency bands like bass and treble, to remove unwanted frequencies or boost wanted ones
- deconstructing earthquake vibrations of different speeds and strengths to optimize architectural designs to withstand earthquakes
- deconstructing computer data for use in file compression, to ignore less important frequencies and keep important ones

To perform frequency decomposition, [[fourier-transform|Fourier transforms]] are used to deconstruct a continuous signal in the [[time-domain|time domain]] into a signal in the frequency domain.

In [[digital-signal-processing|digital signal processing]], a [[discrete-fourier-transform|Discrete Fourier Transform (DFT)]] is used to convert a digital representation of a signal (finite sequence of equally-spaced samples) into a function of frequency. In practical applications, the DFT is implemented using Fast Fourier Transform (FFT).

## Sources

- <https://download.ni.com/evaluation/pxi/Understanding%20FFTs%20and%20Windowing.pdf>
