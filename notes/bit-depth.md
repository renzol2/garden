---
tags: music mus-407 electroacoustic computer digital audio sampling  bit-depth dynamic-range quantization
---

# Bit Depth

**Bit depth** (or _sample width_) in a [[digital-audio|digital audio]] encoding system determines the number of [[bit]]s used to represent each [[sampling-signal-processing|sample]].

- i.e. the number of available resolution points to which a measured analog value can be approximated
- 1 [[byte]] = 8 bits

Number of resolution points = $2^{\text{bit depth}}$

- `1`-bit system; 2 resolution points
- `2`-bit system; 4 resolution points
- `8`-bit system; 256 resolution points
- `16`-bit system; 65536 resolution points (1 byte per sample)
- `32`-bit system; a lot of resolution points (4 bytes per sample)

Consider the analog-to-digital conversion process in a 3-bit system:

![Analog-to-digital conversion process in a 3-bit system](../assets/analog-to-digital-conversion-3-bit.png)

The [[amplitude]] of each sample is quantized to a particular bit and encoded into binary. Through [[pulse-code-modulation|PCM]], we then encode the binary into a modulated pulse wave.

Bit depth determines the maximum [[dynamic-range|dynamic range]] of a digital audio signal, resulting in the relative amount of [[decibel|dB]]s available.

- `16`-bits gives us 96 dB to work
- `24`-bits gives us 120-something dB
- Our pain threshold goes up to 120-something dB, so we don't need to raise the bit depth past something like `16`-bits.

`dynamic range (dB) ~= 6 x bit depth`, e.g. an 8-bit system provides 48 dB of dynamic range

- signals at or below -48 dBFS will be unresolvable from the [[noise-floor|noise floor]]

Reducing the bit depth, and therefore dynamic range, does _not_ reduce the number of samples taken (the sample rate). We can still represent high [[frequency|frequency]] content, but reducing the bit depth reduces the dynamic range at which we can represent the audio content.

## Tradeoffs between dynamic range and memory

A large dynamic range lets us represent sound at extremely varied loudness. However, the memory requirements for increasing the dynamic range get very expensive past 16-bits.

## Sources

- MUS 407
- CS 448
