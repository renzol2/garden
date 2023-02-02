---
title: Biquad filter
tags: filters audio-effects dsp
---

# Biquad filter

A **biquad filter** is a second-[[filter-order|order]] [[infinite-impulse-response|IIR]] [[filter]] that uses the two most recent input [[sampling-signal-processing|samples]] and the two most recent output samples.

The different equation of a biquad filter is:

$$
y_n = a_0x_n + a_1x_{n-1} + a_2x_{n-2} - b_1y_{n-1} - b_2y_{n-2}
$$

## Use case

A biquad filter's coefficients can be tuned to represent most classic filter types, such as:

- [[low-pass-filter|LPF]] and [[high-pass-filter|HPF]]
- [[low-shelf|low shelf]] and [[high-shelf|high shelf]] filters
- [[parametric-eq|parametric EQ]] setups

## Sources

- <https://dobrian.github.io/cmp/topics/filters/filterequation.html>
