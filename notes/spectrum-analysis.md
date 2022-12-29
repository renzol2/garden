---
tags: mus-409
---

# Spectrum Analysis

## Spectrum Plots

2D plot of an instantaneous moment in time

- 3D time-varying plot - amplitude as a function of frequency and time
- 2D time-varying plot (sonogram): frequency and time axes, amplitude represented with color or line darkness

[[sound-waves|Sound]] can be described as a mixture of elementary vibrations with particular [[frequency|frequencies]], [[amplitude]], and [[phase]] offsets.

**Spectrum**: a measure of distribution of [[audio-signal|signal]] energy as a function of frequency

- i.e. how much of each frequency is present in a signal

**Spectrum analysis:** process of deconstructing a [[time-domain|time domain]] signal, and measuring/deriving its spectral components

- [[fourier-theorem|Fourier theorem]] is the most broadly applicable

An analogy:

- [[additive-synthesis|additive synthesis]] = following a recipe from a cookbook
- spectrum analysis = deriving a recipe from a complete meal

## Common Creative Applications

- resynthesis
  - time compression/expansion, pitch shifting, cross-synthesis
- analysis of electronic or other notation-less music by musicologists/theorists
- "intelligent" computer listening [[algorithm|algorithms]]
  - pitch/rhythm detection algorithms
  - rhythm detection is possible without an [[fast-fourier-transform|FFT]], using simple time domain tracking
  - FFT is more of a refined tool, where you can factor spectrum into the detection of rhythm
    - ex. someone bumping into the [[microphones|microphone]] causes a low frequency bump, which time domain analysis can't catch

### Sources

- MUS 409
