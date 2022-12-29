---
tags: wavetable-synthesis
---

# Phase increment

The **phase increment** in [[wavetable-synthesis|wavetable synthesis]] is the difference between the [[phase]] of a [[waveform]] for neighboring [[sampling-signal-processing|samples]].

$$
\theta_{inc}(f) = \frac{2\pi f (n + 1)}{f_s} - \frac{2\pi f (n)}{f_s} = \frac{2\pi f}{f_s}
$$

$\theta_{inc}(f)$ depends explicitly on the [[frequency]] $f$ and implicitly on the [[sample-rate|sample rate]] $f_s$, which usually stays constant.

In implementation, a `phase` variable is initialized to 0 and incremented by $\theta_{inc}(f)$ after generating each sample. This variable gets reset every time a new frequency needs to be generated (i.e. when a new key is pressed on a [[MIDI]] controller.

## Sources

- ["Wavetable Synthesis Algorithm Explained", Jan Wilczek (WolfSound)](https://www.thewolfsound.com/sound-synthesis/wavetable-synthesis-algorithm/)
