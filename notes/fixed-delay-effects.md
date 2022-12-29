---
tags: mus-407 delay delay-line
---

# Fixed Delay Effects

**Fixed delay effects** are [[digital-delay-line|delay effects]] where the delay time does not change.

There are three general categories:

1. **short delay** (<10 ms)
   - [[filter|filtering]], [[spectrum|spectral]] coloration, [[comb-filter|comb filtering]]
   - can affect the higher [[harmonic]]s of a sound, depending on the delay time and the [[sample-rate|sample rate]]
2. **medium delay** (10 ms to 50 ms)
   - emphasis, bolstering, impression of increased [[loudness]]
   - still some spectral coloration from [[phase|phasing]]
   - used often in vocal pop production
3. **long delay** (>50 ms)
   - discrete, distinct echoes, simulation of large reflective spaces
   - basically an echo effect

**multi-tap delay**: one write pointer and more than one read pointer

- can create a specific pattern of multiple echoes
- may or may not include a [[feedback]] path

## Creative Usage

Use fixed delay effects on dynamic, complex waveforms.

- worst candidates are [[sine-wave|sine waves]], since the echo will just produce another sine wave
