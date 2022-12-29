---
tags: dsp synthesis
---

# Sine Generator

A **sine generator** is an [[oscillator]] that creates a [[sine-wave|sine wave]].

## Analog

Given a frequency and amplitude, the general (analog, continuous) formula for a sine wave is

$$
s(t) = A sin (2 \pi ft + \phi)
$$

- $f$: frequency in Hz
- $A$: amplitude in range [0, 1]
- $t$: time in seconds
- $\phi$: initial phase (for most cases, assume $\phi$ is 0)

## Digital

A digital sine wave is given by the following formula:

$$
s[n] = A sin (2 \pi f n / f_s)
$$

- $n$: the [[sampling-signal-processing|sample]] number
- $f_s$: [[sample-rate|sample rate]]

In most digital scenarios, such as calculators and computers, any `sin()` function is computed using the _Taylor expansion_ of the sine function:

$$
sin(x) = x - \frac{x^3}{3!} + \frac{x^5}{5!} + \frac{x^7}{7!}
$$

However, this computation is generally expensive, especially in the context of [[digital-audio|digital audio]] where thousands of samples are computed a second.

- digital implementations usually resort to [[wave-table|wave tables]], storing pre-computed values in memory

## Sources

- ["Wavetable Synthesis Algorithm Explained", Jan Wilczek (WolfSound)](https://www.thewolfsound.com/sound-synthesis/wavetable-synthesis-algorithm/)
