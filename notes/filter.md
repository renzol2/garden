---
tags: mus-407 filters cs-448 audio-effects
---

# Filter

A **filter** is a device that alters a [[sound-waves|sound's]] [[spectrum]].

- in other words, they're used to alter [[frequency]] content
- broad definition applies to things not designed specifically to be filters (e.g. rooms, mouths, etc.)
- most effective when applied to a wide/rich spectrum

Multiple filters are used within [[equalization]] (EQ). In [[audio]], most filters are low-[[filter-order|order]] filters, which are simpler in design and less susceptible to error.

## Digital filter representations

There are several ways to represent a linear digital filter:

- Difference equation
- Block diagram
- Impulse response (this one is useful for musicians)
- Transfer function
- Poles, zeroes, and gain
- Magnitude and phase response

## Classic filters

Classic filter types are only capable of signal attenuation.

- [[band-reject-filter|Band reject filter]]
- [[band-pass-filter|Band pass filter]]
- [[high-pass-filter|High pass filter]]
- [[low-pass-filter|Low pass filter]]

## FIR vs. IIR

There is an important distinction between [[finite-impulse-response|FIR]] filters and [[infinite-impulse-response|IIR]] filters.

FIR filters are stable and do not involve [[feedback]], whereas IIR filters can be unstable and explosive due to their use of feedback in their design.

## Characteristics

- [[cutoff-frequency|Cutoff frequency]]
- [[q-factor|Q factor]]

## Arbitrary filter responses

Arbitrary filter responses tend to involve combinations of basic filters for specific purposes.

- ex: denoising, dehumming, etc.

## General filter design: window method

- Take desired [[filter-response-curve]]
- [[inverse-fourier-transform|IDFT]] it
- [[windowing|Window]] it

## Filter design considerations

- Frequency sampling method: define frequency points and their response
- Optimization methods
  - e.g. Parks-McClellan, linear programming, etc.
  - Specify constraints and get optimal filter via optimizer
- Look into `scipy.signal`

## Sources

- MUS 407 Filters
- CS 448
