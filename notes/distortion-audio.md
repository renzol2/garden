---
title: Distortion (audio)
tags: dsp audio-effects
---

# Distortion (audio)

**Distortion** is an [[audio-signal|audio signal]] processing effect that alters the original shape of a signal. It is generally considered an artifact that is unwanted in many cases, but also wanted and even intentional in other cases, especially in music.

Musically, distortion can induce tones ranging from "fuzzy", "growling",  and "gritty" to "smooth and singing" or "harsh and grungy". Distortion can be induced by running signals through an amplifier (ex. guitar amps, vacuum tube amps) or through dedicated, self-contained distortion effects.

Distortion effects affect signals in various ways:

- clipping the signal
- adds sustain
- adds [[harmonic|harmonics]] and [[inharmonicity|inharmonic]] overtones
- [[compression|compresses the dynamic range]], in a way that sounds "warm" and "dirty"

There are often three terms used for 'distortion' effects:

- [[overdrive|Overdrive]]: a nearly linear effect for low level signals, but increasingly nonlinear at high levels
- Distortion: nonlinear effect on most all signal levels
- Fuzz: complete nonlinear effect that creates drastic changes to input [[waveform]]; often hard or harsh sounding

## Implementation

Distortion effects can be described by a **characteristic curve**, i.e. a function that maps input [[sampling-signal-processing|samples]] to output samples. 

This results in a **non-linear** system, whereas most audio effects operate under a linear system.

When implemented with a characteristic curve, distortion is **time-invariant**, since output samples depend only on input samples and not the time at which they are processed.

Distortion by characteristic curve is also **memoryless**, since the implementation does not require any previous or future samples - it just needs the current input sample to make the output sample.

## Hard clipping & soft clipping

Distortion effects are often categorized by whether they produce [[hard-clipping]] or soft-clipping.

## Sources

- <https://en.wikipedia.org/wiki/Distortion_(music)>
- <https://en.wikipedia.org/wiki/Distortion>
