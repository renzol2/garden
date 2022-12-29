---
tags: ece-402 dsp
---

# Fast Fourier Transform

A **fast Fourier transform (FFT)** is an [[algorithm]] that computes the [[discrete-fourier-transform|discrete Fourier transform]] of a sequence, as well as its [[fourier-inversion-theorem|inverse]] (IDFT).

- rapidly computes transformations by factorizing the DFT matrix into a product of mostly zero factors
- reduces [[runtime]] complexity from $O(n^2)$ to $O(n\text{log}n)$

From MUS 409:

- The FFT is a version of the DFT/[[short-time-fourier-transform|STFT]] meant to be as efficient as possible
  - sample length of window must be a power of 2
  - removes redundant calculations; ~100 to 1000x faster
  - analysis/resynthesis can be done in real-time on a live signal

## Applications

FFTs are important in many applications since it makes working in the [[frequency-domain|frequency domain]] as easy as working in the [[time-domain|time domain]]. This has numerous applications in mathematics, science, music and other fields.

For music:

- digital recording and [[sampling-signal-processing|sampling]]
- [[additive-synthesis|additive synthesis]]
- [[spectral-analysis|spectral analysis]]
- pitch correction software

In detail (MUS 409):

- for each analyzed window, the FFT produces a **frame**, which contains two things:
  - magnitude array or magnitude spectrum - data corresponding to amplitude of each frequency component
  - phase array of phase spectrum - data corresponding to the inital phase of each frequency ycomponent
  - mag/phs arrays are made up of each individual, linearly spaced frequency bins, containing amplitude/phase information

![FFT in detail](../public/attachments/fft-in-detail.png)

- bin spacing determined by the following equation:

```text
frequency bin spacing interval = sample rate / window size
```

- e.g. a window size of 2048 samples and SR of 48000 samples/sec yields a bin spacing of 23.4375 Hz
  - bin 0: 0 Hz
  - bin 1: 23.44 Hz
  - bin 2: 46.88 Hz
- Time domain signals are band-limited below the [[nyquist-frequency|Nyquist frequency]], so only the lower half of the bins are usable
  - bin 1022: 23976.56 Hz
  - bin 1024: 24000 Hz (N)
  - bin 1024+: contains [[aliasing|aliased]] data; a mirror image of the first half, and is therefore useless

## Sources

- <https://en.wikipedia.org/wiki/Fast_Fourier_transform>
- <https://download.ni.com/evaluation/pxi/Understanding%20FFTs%20and%20Windowing.pdf>
