---
title: Allpass filter
tags: mus-407 ece-402
---

# Allpass Filter

An **allpass filter** is a [[sampling-signal-processing|signal processing]] [[filter]] that passes all [[frequency|frequencies]] equally in gain but changes the [[phase]] relationship among various frequencies.

- useful for [[delay-line|delay]] effects

## Allpass systems

There are several systems that have the "allpass" property, i.e. they do not affect the magnitude of any frequencies.

[[delay-line|Delays]] are the simplest allpass filter, since they affect the phase of the entire signal.

### First-order IIR allpass

A first [[filter-order|order]] [[infinite-impulse-response|IIR]] allpass system has the following difference equation:

$$
\begin{align}
y[n] &= a_1 x[n] + x[n-1] - a_1 y[n-1] \\
&= a_1 x[n] + d[n-1]
\end{align}
$$

where $x[n]$ is the input signal and $y[n]$ is the output signal.

In implementation, $d[n-1]$ can be stored as an intermediate value in a buffer.

This is actually a combination of a [[feedback-comb-filter|feedback comb filter]] and a [[feedforward-comb-filter|feedforward comb filter]].

The _allpass coefficient_, $a_1$, determines the _break frequency_ of the allpass filter. This break frequency determines where the phase shift of the filter is exactly $-\frac{\pi}{2}$ radians:

$$
a_1 = \frac{tan(\pi f_b / f_s) - 1}{tan(\pi f_b / f_s) + 1}
$$

Some properties of this first order IIR allpass:

- Phase shift at DC ($f=0$) is 0
- Phase shift at nyquist frequency is always the maximum phase delay
- Phase shift at break frequency $f_b$ is $-\frac{\pi}{2}$

Arranging multiple allpass filters in a series results in a summation of phase delays. This is the basis for the [[phaser]] effect.

### Second-order IIR allpass

A second-order IIR allpass filter is more flexible than the first-order, and is used to implement [[parametric-eq|parametric EQs]] and other [[equalization]] effects.

## Within reverb

In digital [[reverb]] [[algorithm]]s, all-pass filters reduce [[resonance]] by introducing [[frequency]]-specific [[phase]] shifts to diffuse the sound.

- Used in [[freeverb]]

## Sources

- MUS 407
- CS 448
- <https://thewolfsound.com/allpass-filter>
