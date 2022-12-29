---
tags: ece-402 dsp spectral-analysis
---

# Long Window Time-Varying Spectral Analysis

**Long Window Time-Varying Spectral Analysis** is a form of [[time-varying-spectral-analysis|time-varying spectral analysis]] that analyzes an entire [[audio-signal|audio signal]] or longer windows (>100ms) of an original signal.

- useful for a wide class of inputs, including polyphonic and [[inharmonicity|inharmonic]] sounds
  - higher [[partial]]s are easier to analyze compared to lower [[partial]]s due to larger window of samples
- results in poor time resolution, temporal smearing, and long-window artifacts
  - time-domain shape of attacks and [[transient]]s becomes smeared
  - artifacting results from miscalculations due to large window size

Long window analysis facilitates some forms of manipulation:

- pitch manipulation
- time stretching

## Sources

- [ECE 402 UIUC: Electronic Music Synthesis](https://courses.grainger.illinois.edu/ece402/)
