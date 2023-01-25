---
tags: music mus-407 signal-processing sampling cs-448
---

# Aliasing

**Aliasing** (or **foldover**) is the phenomenon where frequencies greater than the [[nyquist-frequency|Nyquist Frequency]] $N$ are still digitally represented within the range $[0, N]$.

- input [[frequency|frequency]] will "reflect" off of **zero** and $N$ if boundary is exceeded
- similar to "negative frequencies" in [[modulation-synthesis|modulation synthesis]]

Imagine a [[sampling-signal-processing|sampled]] analog input with [[spectrum|spectral]] content above $N$.

- Foldover occurs as the [[waveform]] is sampled
- Results in unnecessary and/or unwanted interference (either constructive or destructive)
- Alias frequencies interfere/sum with sub-$N$ frequencies, altering the spectrum

**Rule of thumb**: sample **at least twice** the highest frequency you record

## ADC/DAC Conversion Process

An ADC includes an [[anti-aliasing-filter|anti-alias filter]], which removes analog frequency components that would cause aliasing.

A DAC includes a **smoothing filter**.

- reconstruction of an analog signal from raw digital data results in [[waveform]] discontinuities ("staircase" shape)
- without smoothing, these artifacts produce audible high frequency content

Both classify as [[low-pass-filter|low-pass filter]] whose [[cutoff-frequency|cutoff frequency]] is at or near the [[nyquist-frequency|Nyquist Frequency]].

_Aliasing_ in general does not exist just in audio, but in _anything_ digital.

- think: pixels on a screen
- in this case, _resolution_ of a digital image is similar to _sample rate_ of digital audio


## Sources

- MUS 407
- CS 448
