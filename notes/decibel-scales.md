---
tags: mus-407 sound sound-properties amplitude decibel
---

# Decibel Scales

There are **two** distinct cases of the [[decibel]] scale for use of measurement:

## Sound pressure level

- `dB SPL` (decibel sound pressure level)
- used for measuring sound level of an acoustic environment
- 0 dB = threshold of hearing
  - below 0 dB, you cannot hear it
- 120-130 dB = threshold of pain
  - when representing [[dynamic-range|dynamic range]] through [[bit-depth|bit depth]] in a digital system, we don't need to exceed a bit depth that allows for more than the pain threshold

## Electrical signal level

Decibels are often used to describe [[audio-signal|audio signal]] levels.

- **analog**: `dBV` (voltage) , `dBu` (unloaded)
- **digital**: `dBFS` (relative to _full scale_)
- What does 0 dB mean?
  - _analog_: nominal operating level, optimal I/O linearity
  - _digital:_ highest representable level without introducing clipping/distortion
    - positive digital dBFS values are **_bad_**: clipping, nasty distortion
- signal levels below 0 dB have negative values
