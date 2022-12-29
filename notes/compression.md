---
tags: music compression mus-407 production dynamics drp dynamic-range-compression dynamic-range
---

# Compression

**Compression** is a form of [[dynamic-range-processing|dynamic range control]] that (generally) reduces the [[dynamic-range|dynamic range]] of a signal. A _compressor_ is an amplifier whose gain is determined by an input [[audio-signal|signal]] level

- when signal level > [[amplitude]] threshold, compression effect becomes active and attenuates a signal

Frequently used to regulate a "peaky" signal during recording, i.e. to provide a more constant and predictable level

- e.g. rock drum set, swaying vocalist
- essentially, automates [[mixer]] input faders to avoid manual adjustment

Compression is also used during mixing/mastering to provide a higher overall mix level.

Compressor behavior is modeled using a graph of its [[transfer-function|transfer function]], which is generally comprised of these parameters:

- [[ratio-drp|ratio]]
- [[threshold-drp|threshold]]
- makeup gain
- attack/release

Compressors can also feature the following additional parameters:

- auto mode
- lookahead
- stereo linking

## Ratio

The severity of signal attenuation is determined by a _compression [[ratio-drp|ratio]]_.

Downward compression ratios of 8:1 and above are generally considered "extreme" compression

- Can result in a perceptual distortion of [[transient|transients]], noticeable changes in [[timbre]], often described as a "squashed" sound
- A compressors with ratios above 10:1 would generally be considered a [[limiter]]

## Makeup gain

After compression is applied, **makeup gain** is a normal amplification process used to compensate for the loss in overall level

- typically used to restore peaks to their original level after compression creates more [[headroom]]
- content below threshold, including the [[noise-floor|noise floor]], undergoes a net level increases

## Types of Compression

- [[limiter|Limiting]]
- [[upward-compression|Upward compression]]
- [[multiband-compression|Multiband compression]]
- [[parallel-compression|Parallel compression]]
- [[buss-compression|Buss compression]]
- [[side-chaining|Sidechain compression]]
- Serial compression

## Sources

- MUS 407 Dynamic Range Processing
- <https://www.blackghostaudio.com/blog/the-ultimate-guide-to-compression>
