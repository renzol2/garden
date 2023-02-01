---
tags: mus-407 filters cs-448
---

# Filter

A **filter** is a device that alters a [[sound-waves|sound's]] [[spectrum]].

- in other words, they're used to alter [[frequency]] content
- broad definition applies to things not designed specifically to be filters (e.g. rooms, mouths, etc.)
- most effective when applied to a wide/rich spectrum

Multiple filters are used within [[equalization]] (EQ).

## Classic filters

Classic filter types are only capable of signal attenuation.

- [[band-reject-filter|Band reject filter]]
- [[band-pass-filter|Band pass filter]]
- [[high-pass-filter|High pass filter]]
- [[low-pass-filter|Low pass filter]]

## IIR vs. FIR

- See: [[finite-impulse-response]] vs. [[infinite-impulse-response]]

## Characteristics

- [[cutoff-frequency|Cutoff frequency]]

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
