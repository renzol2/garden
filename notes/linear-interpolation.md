---
tags: ece-402 dsp
---

# Linear Interpolation

**Linear interpolation** is the process of generating values between two neighboring [[sampling-signal-processing|samples]] in a signal.

- effectively draws a straight line between two neighboring samples and returns the appropriate point along that line.

## Definition

Let $a$ be a number between 0 and 1 which represents how far we want to interpolate a signal $y$ between time $n$ and $n + 1$. Then we can define the linearly interpolated value $\hat{y}(n+a)$ as follows:

$$
\hat{y}(n + a) = (1 - a) \cdot y(n) + a \cdot y(n+1)
$$

## Sources

- <https://ccrma.stanford.edu/~jos/pasp/Linear_Interpolation.html>
- <https://ccrma.stanford.edu/realsimple/Interpolation/>
