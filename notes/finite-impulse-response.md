---
tags: mus-407 filters
---

# Finite impulse response (FIR)

**Finite impulse response** (FIR) filters are [[filter|filters]] whose [[impulse-response|impulse response]] decays to zero after some time.

- Referred to as "passive", "well-behaved"
- inherently stable design but fewer possibilities for [[spectrum]] changes
- less creatively flexible

Since FIR filters can be described as time series, applying an FIR filter involves using [[convolution]].

- They can be sounds themselves (a filter response is just an instantaneous, full frequency signal), but we usually listen to them by using source signals

## Views of a filter

We can represent a filter in both the [[time-domain]] and [[frequency-domain]].

We can get the [[filter-response-curve]] by taking the DFT of the filter's time domain representation. 

## General equation

The general equation for a digital FIR filter is:

$$
y_n = a_0x_n + a_1x_{n-1} + a_2x_{n-2} + ... + a_Nx_{n-N}
$$

or, the output [[sampling-signal-processing|sample]] $y_n$ is a summation of the past $N$ input samples $x_n$, $x_{n-1}$, $x_{n-2}$, to $x_{n-N}$. Each input sample has a coefficient $a_n$, which is typically in the range $[-1, 1]$ and determines the weight of each past sample.

An even more general equation for _all_ filters can be seen with the implementation of a digital [[infinite-impulse-response|IIR]] filter.

## Sources

- MUS 407 Filters
- CS 448 Filters
- <https://dobrian.github.io/cmp/topics/filters/filterequation.html>
