---
title: GCC-PHAT algorithm
tags: cs-448
---

# GCC-PHAT algorithm

- Perform FFT on frames of both input channels
- _Whiten_ the [[spectrum|spectra]], i.e. make the amplitude response uniform throughout
  - this maintains [[phase]] information, but removes [[amplitude]] information (which is good for [[localization]])
- Compute [[cross-correlation|cross correlation]]
- Get peak in the [[time-domain|time domain]]

## Sources

- CS 448 Microphone Arrays
