---
title: Infinite impulse response (IIR)
tags: mus-407 filters
---

# Infinite impulse response (IIR)

**Infinite impulse response** (IIR) filters are [[filter|filters]] whose [[impulse-response|impulse response]] design involves feedback

- IR approaches but never reaches zero
- unstable, can self-oscillate (analog) or output explosive values ([[digital-audio|digital]])
- this feedback enables amplification of the [[spectrum]] (i.e. [[additive-eq|additive EQ]])

They are not applied with plain convolution - they use _feedback_ to produce infinitely long effects

## General equation

The general equation for a digital IIR filter is:

$$
\begin{align}
y_n &= \\ 
& a_0x_n + a_1x_{n-1} + a_2x_{n-2} + ... + a_Nx_{n-N} \\
&- b_1y_{n-1} + b_2y_{n-2} - ... - b_Ny_{n-N}
\end{align}
$$

or, the output [[sampling-signal-processing|sample]] $y_n$ is a summation of the past $N$ _input_ samples $x_n$, $x_{n-1}$, $x_{n-2}$, to $x_{n-N}$, as well as the past $N$ _output_ samples $y_n$, $y_{n-1}$, to $y_{n-N}$. 

Each past input sample has a coefficient $a_n$, and each output sample has a coefficient $b_n$, which are typically in the range $[-1, 1]$ and determines the weight of each past sample. In this way, digital FIR filters introduce [[feedback]] by including past output samples.

## Sources

- MUS 407 Filters
- CS 448
- <https://dobrian.github.io/cmp/topics/filters/filterequation.html>
