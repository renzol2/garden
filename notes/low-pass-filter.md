---
tags: mus-407 filters
---

# Low pass filter

A **low pass filter** (LPF) is a [[filter]] that progressively attenuates a [[audio-signal|signal]] **above** a [[frequency]] threshold

- allows low frequencies to pass through the filter
- has one main parameter: [[cutoff-frequency|cutoff frequency]]
- can also have parameters to affect the steepness of the curve (Q)

Low pass filters are used to remove high frequency elements (hiss, [[noise]], etc.). Generally, they "muffle" a sound.

## Design

The ideal response of a LPF is a *step function*, i.e. everything above a certain frequency $\omega$ is set to an [[amplitude]] of 0.

The inverse [[discrete-fourier-transform|DFT]] of this step function is the *sinc* function. If we look at the frequency response of the sinc function, it looks like a LPF!

The longer the filter (in the time domain), the better the frequency response. However, this causes more bunched up [[filter-ripple|ripples]]. 

[[windowing|Windowing]] the filter decreases the rippling and results in a more "palatable" response. However, windowing also decreases the steepness of the filter. This is an established tradeoff.

To make a low pass filter

- Pick a cutoff frequency $0 < \omega < 1$, where $\omega = 1$ will filter nothing and $\omega = 0$ will filter everything
- Generate a sinc to get the filter coefficients
    - $x[n] = \omega sinc(n \omega)$
- Apply [[windowing]] to smooth [[filter-ripple|rippling]]
- [[convolution|Convolve]] with a desired sound

## Sources

- MUS 407 Filters
- CS 448
