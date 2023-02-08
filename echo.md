---
title: Echo
tags: cs-448
---

# Echo

An **echo** is a type of [[fixed-delay-effects]]. This is a feedforward circuit.

FIR filter:

$$
y[t] = x[t] + gx[t-N]
$$

where $y[t]$ is output, $x[t]$ is input, $g$ is some attenuation, and $N$ is the amount of delay in the filter.

## Sources

-
