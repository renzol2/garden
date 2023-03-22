---
title: Mel Frequency Cepstral Coefficients
tags: cs-448
---

# Mel Frequency Cepstral Coefficients

**MFCCs** are a coarse version of the [[spectrogram]] that shows perceptually meaningful representations of [[sound-waves|sound]] over time.

- blurs [[frequency|frequencies]], uses _Mel_ warping to reduce their number and better reflect our perception of frequency (i.e. better reflect [[pitch]])
- _Mel_ short for melody
- performs DCT (discrete cosine transform) and keep lowest frequencies


## Uses

Useful for [[music-classification|music classification]] when focusing on overall spectral qualities instead of small pitch or rhythm fluctuations.

- while magnitude spectra are normally exponentially distributed, taking their log makes them Gaussian distributed and therefore easier to use with Gaussian-based classifiers
- using the Mel scale warps the data to map our perceptual space
- DCT keeps only the low frequencies and smooths the data

## Sources

- CS 448: Classification and Music Information Retrieval
