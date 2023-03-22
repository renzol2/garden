---
title: Audio fingerprinting
tags: cs-448 dsp
---

# Audio fingerprinting

**Audio fingerprinting** is the taks of finding exact matches from recordings to a database of music.

- Widely available commercially, e.g. Shazam
- Works even with potentially [[noise|noisy]] recordings

## Implementation

The query can be noisy or incomplete due to environmental noise, subset of sample being queried, etc.

Solution: find salient peaks

- find local peaks in the [[spectrogram]] and note their positions
- spectrogram array is now represented by a set of points

Forming constellations

- connect neighboring peaks to form pairs
  - information we keep: `time1` and `[time2 - time1, freq1, freq2]`
- advantage: constellations are rather robust and do not change as drastically under noise, filtering, etc.
- particularly good at identifying transients, e.g. drums

### Fast searching

**Hashes** are used for fast searches

- for each recording, make a table of constellations
- take all constellation features and hash them, i.e. pack in to a 12 [[bit]] number
- find database entries with common hashes to query
  - common hashes imply similar spectral features
  - lots of these imply a very similar spectrogram
- very efficient since we can precompute database hashes
- not all matches will be correct, but those that have the same time offset between files will suggest that the two files are likely the same

## Results

Robust to noise-contaminated sources: 90% for 3dB SNR, 79% for 0dB SNR

Rapid searching in database

## Sources

- CS 448: Classification and Music Information Retrieval
