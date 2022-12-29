---
tags: mus-407 delay delay-line
---

# Flanger

The **flanger** effect is a [[variable-delay-effects|variable delay effect]] that derives from a phenomenon called _repetition pitch_ in which a [[noise]] source gains a sense of [[pitch]] when combined with a delayed copy of itself.

- introduces a "spectral sweep" that colors the sound

First documentation by Christian Huygens, 1693; noise from water fountain reflected from evenly-spaced stone steps.

Early notable use in _Mammy's Boogie_, Les Paul (1945)

- two tape recorders with identical input
- pressure applied to flange (edge of tape reel) to vary speed slightly
- [[mixer]] combines two inputs

## Digital Implementation

Flanging can be implemented as follows:

- delay time modulated by low-[[frequency]] [[sine-wave|sine wave]] (0.1-20 Hz)
- delayed signal has subtle fluctuations in pitch
- combined input + output has sweeping peaks and nulls in [[spectrum]], resulting from [[wave-interference|constructive/destructive interference]]
- peaks occur at integer multiples of $1/D$ Hz, where $D$ is the delay time in seconds
- nulls occur linearly between peaks, at odd [[harmonic]]s of $1/(2D)$ Hz

Flanger effects have similar sound to [[phaser]] effects

- could be considered a "sweeping" [[comb-filter]] effect
- **flanging** → variable-delay [[comb-filter]]
- **phasing** → variable-delay [[all-pass-filter]]
