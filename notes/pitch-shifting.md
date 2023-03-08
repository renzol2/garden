---
tags: ece-402 dsp pitch-shifting
---

# Pitch Shifting

**Pitch shifting**, in this context, is the process of changing the [[pitch]] of some audio sample in playback.

- there are methods to [[pitch-shifting-realtime|pitch shift in realtime]], which utilizes [[variable-delay-effects|variable delay lines]], but the process in this note is different

## Naïve Method

The naïve method to pitch shift is to play back a sample at a different rate.

- a normal playback would be at rate 1.0
- a faster playback would be at rates > 1.0 (ex. octave up would be rate 2.0)
- a slower feedback would be at rates < 1.0 (ex. octave down would be rate 0.5)

In a digital context, this would essentially be changing the [[sample-rate|sample rate]].

This method raises several problems:

- any vibrato or tremolo changes speed
- the onset time and [[transient]] shape changes with the sustain, changing the overall [[envelope]]
- note length speeds up or slows down
- the [[spectrum]] has large changes, causing the spectral envelope to shift and moving the [[resonance]]s/formants
  - think "chipmunk" effect when going up or "inflated head" effect when going down
- playing at a lower rate results in high energy buildup near the Nyquist frequency, resulting in artifacts
- playing at a higher rate results in [[aliasing]]

![Pitch shifting issues](../assets/pitch-shifting-issues.png)

There are a few fixes to these problems:

- interpolating to fractional samples in sample file helps a little, but all problems persist
- insert zeros (for speech) - adding zero samples before glottal pulses reflects mouth shape (resonances, decay rates), even at different pitches
- use an entirely different algorithm, such as Lent's algorithm

## PSOLA

**Pitch synchronous overlap add** finds the periods of the input signal and spaces them farther apart, or closer, to alter pitch.

- the characteristic period shape should stay the same in the [[time-domain|time domain]]; they should _not_ stretch out

## Applications

## Pitch correction

- Identify pitched areas, since unpitched areas are useless
- Identify preselected frequencies that are "correct", i.e. notes of a [[music-scale|music scale]]
- Quantize (to some degree) the pitch

## Changing pitch intonation

"Emotion changing" of a speech signal

- Exaggerate pitch for more excitement
- Flatten pitch for less emotion

## Sources

- ECE 402
