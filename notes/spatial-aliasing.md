---
title: Spatial aliasing
tags: cs-448
---

# Spatial aliasing

**Spatial aliasing** is a phenomenon where the frequency of spatialization is so high that the recording cannot accurately tell the difference between different locations.

To solve spatial aliasing:

- Mic distance needs to be less than half the wavelength of the input [[audio-signal|signal]]
    - Otherwise, we get spatial aliasing
    - We superimpose peaks that are more than one period apart
- This creates aliased locations that don't exist, in the same way that frequency [[aliasing]] creates new frequencies

## Sources

- CS 448 Microphone Arrays
