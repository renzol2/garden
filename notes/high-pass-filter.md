---
tags: mus-407 filters
---

# High pass filter

A **high pass filter** (HPF) is a [[filter]] that progressively attenuates a [[audio-signal|signal]] **below** a [[frequency]] threshold

- allows high frequencies to pass through the filter
- one main parameter: [[cutoff-frequency|cutoff frequency]]

High pass filters are useful for removing low frequency content (rumbling, hum, etc.).

## Designing a high pass filter

Subtract a [[low-pass-filter|LPF]] from the input:

- `Highpassed = input - lowpass(input)`

Or in pseudocode:

```
highpass():
    if n = 0:
        1 - omega * sinc(n * w)
    else if n != 0:
        -omega * sinc (n * w)
```

## Sources

- MUS 407 Filters
