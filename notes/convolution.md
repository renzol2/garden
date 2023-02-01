---
title: Convolution
tags: cs-448 dsp filters
---

# Convolution

A **convolution** is an operation between time series.

Intuitively explained: For each sample of `y`, shift `x` to that sample's position, scale it by `y`'s value, and add to output.

- Note that this results in a longer output than input.
- Output length is `length(x)` + `length(y)` - 1

In the below example, $*$ is convolution, _not_ multiplication:

$$
z = y * x = x * y
$$

Convolution is a tool used in [[filter]] design, especially for simulating room reflections.

## Fast convolution

Convolution is computationally slow due to the amount of multiplication.

It can be sped up significantly using [[fast-fourier-transform|FFT]], with an [[algorithm]] known as **fast convolution**.

- Perform convolution in the [[frequency-domain]]
- Complexixity drops to $2 N log_2 N$

### Overlap-add fast convolution

Similar to spectrograms:

1. Make frames
2. Convolve frames using [[fast-fourier-transform]]
3. Invert back to [[time-domain]]

## Sources

- CS 448
