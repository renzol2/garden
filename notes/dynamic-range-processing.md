---
tags: music mus-407 electroacoustic dynamic-range dynamics audio-effects
---

# Dynamic Range Processing

Dynamic range processing transforms the amplitude of [[audio-signal|audio signals]]. A _dynamic range process_ (DRP) changes a signal's [[dynamic-range|dynamic range]] by altering its [[amplitude|amplitude]].

- measuring signal amplitude
- adjusts signal amplitude based on measured value

Measured & processed signals can be the same or different (i.e. there can be distinct _source_ & _target_ signals. see: [[side-chaining|Sidechaining]])

Applications include:

- maintaining a constant signal level
- increasing the overall level of a mix
- creative [[transient]] and [[envelope]] shaping
- [[noise]] reduction
- preventing clipping/overloading
- [[side-chaining|sidechaining]] (amplitude following, ducking)

## Key Concepts

All forms of DRP rely on an amplitude [[threshold-drp|threshold]].

- determines signal level above or below which DRP take effect, depending on the type of effect

DRPs utilize a **detection circuit** or **detection [[algorithm]]** for tracking signal amplitude, which can track either _peak_ or _average_ signal level

**Peak**: instantaneous measurement, captures true [[waveform]] peaks: "no sample left unchecked"

- more applicable for preventing overloading/clipping.

**Average**: signal values averaged over a time interval, also called _RMS_ ([[root-mean-square]]) tracking

- sculpting the [[dynamic-range|dynamic range]] of the sound without closely monitoring every single peak or [[transient]]
- provides a smoother response to a changing input signal

## Types

- [[noise-gate|Noise gate]]
- Compressor ([[compression|compression]])
- [[Limiter]]
- [[Expander]]
- [[envelope-shaper|Envelope shaper]]

## More Terms & Techniques

### DRP Considerations

DRPs, particularly compressors ([[compression|compression]]) and [[limiter]]s, can smear/distort transients

- like all effects, easy to overuse, generally should be applied in moderation
- can be used in extremes for creative effect

DRPs may involve a "look ahead" time to properly anticipate signal levels

- introduces a small delay into processed audio
- can create synchronization issues, but usually automatically or easily managed in DAW context

DRPs generally have more applications in recording/live sound.

In [[electroacoustic-music|electroacoustic]] [[music-composition|composition]], traditional application of DRP is less useful

- composer has complete control over levels during compositional process
- can usually go back and adjust levels as necessary

### Attack, Hold, Release

Many DRPs include [[envelope]] parameters: often _attack/release_, sometimes _hold_

**Attack** determines the amount of time for DRP effect to fully activate. The attack [[transient]] begins when signal crosses the threshold.

**Release** determines amount of time for DRP effect to deactivate completely. Release transient begins when level no longer crosses threshold.

**Hold** will force DRP effect to remain active for a time, regardless of threshold.

- can be exploited for creative transient shaping (used explicitly in envelope shapers)
- useful in noise gates to prevent intermittent signal near threshold

### Upward/Downward Compression & Expansion

Typical cases:

- compressors attenuate above a threshold ([[compression|compression]])
- [[expander]]s attenuate below a threshold
- both referred to as _"downward"_ compression/expansion

However, it is sometimes possible to set a threshold and amplify signal below it, considered a form of compression.

Likewise, it is possible to boost signal above a threshold - a form of expansion.

This technique is infrequently used:

- upward compression raises the [[noise-floor|noise floor]]
- upward expansion makes peaks even [[loudness|louder]]

### Side-Chaining

See: [[side-chaining|Sidechaining]]

## Transfer Function Examples

All DRP effects can be represented through a [[transfer-function|transfer function]], a function between an input signal (in [[decibel|dB]]) and an output signal with a processed [[amplitude]].
