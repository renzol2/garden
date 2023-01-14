---
title: Overdrive
tags: dsp audio-effects
---

# Overdrive

**Overdrive** is a [[distortion-audio|distortion]] effect that acts linearly on low-level [[audio-signal|audio signals]], but increasingly nonlinearly on higher level signals.

## Implementation

The characteristic curves for overdrive effects remain linear at low input levels, and get increasingly non linear at high input levels.

Example curve:

$$
\begin{align}
2x &\text{ for } 0 \leq x \le 1/3 \\
f(x) = 1-(2-3x)^2 / 3 &\text{ for } 1/3 \leq x \le 2/3 \\
1 &\text{ for } 2/3 \leq x \leq 1
\end{align}
$$

This particular curve is **memoryless**, i.e. any output [[sampling-signal-processing|sample]] only depends on the current input sample, and not on any previous inputs or outputs.

This type of curve results in a fairly close approximation to analog distortion circuits, though it is not perfect.

## Sources

- <https://www.oreilly.com/library/view/audio-effects/9781466560284/>
