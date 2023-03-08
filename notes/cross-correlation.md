---
title: Cross correlation
tags: cs-448
---

# Cross correlation

Cross correlation allows us to [[localization|localize]] a [[sound-waves|sound]] using inputs from a [[microphone-array|microphone array]]. We measure signal correlation using

$$
c[d] = \Sigma_{t} y_1[t] y_2[t + d]
$$

i.e. multiply multiple output signals, with one signal being delayed by $d$ samples.

This is very similar to the [[convolution]] formula.

## In the frequency domain

This is accomplishable and more efficient in the [[frequency-domain|frequency domain]] using [[fast-fourier-transform|FFTs]].

- Get inputs, chop to frames, and take the FFT of both signals' frames
- Compute cross correlation in the frequency domain
- Go back to time domain and get the peak

However, correlation output is dependent on input [[loudness]]. This can be solved with the [[gcc-phat|GCC-PHAT algorithm]], although this doesn't work with multiple sources.

To track multiple sources, we can use a [[beamformer]] to measure the amount of acoustic energy around a [[microphone-array|microphone array]].

## Sources

- CS 448 Microphone Arrays
