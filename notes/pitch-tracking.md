---
title: Pitch tracking
tags: mus-407 sound sound-perception pitch cs-448
---

# Pitch tracking

## Zero crossing rate

Find where the waveform crosses the zero mark

- usually twice per period: $f = 0.5 / dz$

Very fast to compute, just find $x[t]x[t+1] < 0$

## Peak picking method

Find where the waveform peaks over time

Hard to compute; effectively zero crossings of derivative on positive side

More intuitive, but slightly more complex code

If there are multiple peaks per period, this method will fail (which is most of the time)

## Low pass filter

Apply a [[low-pass-filter|LPF]] to the signal to leave only the fundamental frequency

- Filter cutoff needs to be greater than fundamental; otherwise, it removes the fundamental too if it's too aggressive

## Measuring waveform similarity using autocorrelation

Use [[cross-correlation|cross correlation]] (cross-correlate the [[waveform]] with itself) to measure waveform similarity at offset $k$

This is called **auto-correlation**:

<!-- TODO: finish this equation -->

$$
c_{x,x}[k] = \Sigma_t 
$$

Autocorrelation basically tells you "Your waveform is very similar to itself shifted by $x$ samples". The distance between peaks of the autocorrelation relate to the pitch (periodicity) of the signal.

We can use the [[fast-fourier-transform|FFT]] to make the autocorrelation operation faster.

- Convolution: $x * y = \text{DFT}^{-1}(X[w]Y[w])$
- Flipping: $x[-t] = \text{DFT}^{-1}(X[w]*)$
- Cross-correlation: $c_{x,y} = \text{DFT}^{-1}(X[w]*Y[w])$

You can perform the [[short-time-fourier-transform|STFT]]:

- for each time frame, compute autocorrelation
- take [[inverse-fourier-transform|inverse FFT]] to obtain time version
- get first *significant* peak to find current period
  - *significant* in this case = above ~80% of main peak

### Practical word of caution

```python
c = irfft( rfft(x) * conj(rfft(x)))
```

The negative side values will be appended at the end (refer to slide).

### Tricks for autocorrelation pitch tracking

- Smoothing out occasional jumps (often octave jumps); use median filtering to correct
- Imposing limits on period size
  - Shouldn't be too small (high pitch)
  - Shouldn't be too low
- Periodicity should be strong
  - Height of autocorrelation peak should be high; otherwise, it means there might not actually b e periodicity

## Cepstrum

We can use the [[cepstrum]]: $X_{\tau} = DFT^{-1}(log|X_{\tau}[w]|)$

The [[spectrum]] usually has a spectrum of its own; we can use the cepstrum to highlight periodicity in a sound.

See: [[cepstral-pitch-detection|Ceptral pitch detection]]

## Frequency domain approaches

Use peak-picking on spectra (i.e. discover harmonic series over frequency), but this can be tricky.

## Applications

- Page turner
- Query by humming (search a song by singing it); pitch track user input and match to song database

## Sources

- CS 448: Pitch tracking and modifications
