---
tags: mus-407 filters
---

# Band pass filter

A **band pass filter** (BPF) is a [[filter]] that preserves [[audio-signal|signal]] energy at a **center** [[frequency]]; progressively attenuates above and below

- allows a band of frequencies to **pass** through the filter

Usually has two main parameters:

- _center frequency_ and _bandwidth_
- or, the _two bounding frequencies_ (but the former is more common)

## Designing a band pass filter

To get a bandpass filter, combine a [[high-pass-filter]] and [[low-pass-filter]] with cutoff frequencies depending on the band pass filter's parameters.

Coefficients are:

$$
x[n] = 2 cos (\pi n \omega_c) \omega_b sinc( \omega_b n)
$$

## Sources

- MUS 407 Filters
