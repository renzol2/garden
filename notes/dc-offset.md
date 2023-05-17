---
title: DC Offset
tags: dsp digital-audio
---

# DC Offset

In [[digital-signal-processing|DSP]], a DC offset refers to the mean amplitude of a waveform deviating from 0.

- if the mean [[amplitude]] is 0, then there is no DC bias and the [[waveform]] is DC balanced

DC offset is often (but not always) the result of a fault condition.

## Audio application

[[audio|Audio]] related problems that arise from DC offset include:

- Loudspeakers and headphones can be damaged while playing waveforms with a large DC offset. (Source: <https://youtu.be/8EK9sq_9gFI>)
- Premature asymmetrical [[digital-clipping|digital clipping]], resulting in unwanted [[distortion-audio|distortion]]
- Confusing level metering systems

## Solution

Since the effective [[frequency]] of a DC offset "signal" is 0 Hz, a [[high-pass-filter|high pass filter]] anywhere below 20 Hz should remove DC offset.

## Sources

- <https://en.wikipedia.org/wiki/DC_bias>
- <https://www.soundonsound.com/glossary/dc-offset>
