---
tags: synthesis wavetable-synthesis
---

# Wave table lookup

**Wave table lookup** is the process of computing a waveform value from a wavetable.

## Computing a waveform value from a wavetable

The following section comes from ["Wavetable Synthesis Algorithm Explained" by Jan Wilczek](https://www.thewolfsound.com/sound-synthesis/wavetable-synthesis-algorithm/), using a [[sine-wave|sine]] wave table as an example.

The period of a wave table is given by its length $L$. For each [[sampling-signal-processing|sample]] index $k \in \{0, ..., L-1\}$ in the wave table, there exists a corresponding value $\theta = [0, 2 \pi)$ of the [[sine-generator#Analog|analog sine function]]:

$$
\frac{k}{L} = \frac{\theta}{2\pi}
$$

i.e. there exists a mapping between the values in the wave table and the values of the original waveform.

However, the above equation only holds for $\theta \in [0, 2 \pi)$. To calculate wavetable values for any arbitrary number $x \in \R$, we have to take that number and bring it back to the $[0, 2 \pi)$ range.

In software, this is done by using a function `fmod()`, which finds the remainder of a floating-point division.

Therefore, we can calculate a sample index _approximation_ of the wave table like so:

$$
k = \frac{\phi_x L}{2 \pi}
$$

### Obtaining sample index

The above resulting $k$ is usually a floating-point number between two integers, both of which denote wave table indices.

To make $k$ an integer and obtain a value from the wavetable, there are 3 options:

1. `floor(k)`
2. `round(k)`
3. [[linear-interpolation|linear interpolation]] between wave table values at `floor(k)` and `ceil(k)`

The resulting value `waveTable[k]`, where `k` is the resulting integer, is called a _wave table lookup_.

## Sources

- ["Wavetable Synthesis Algorithm Explained", Jan Wilczek (WolfSound)](https://www.thewolfsound.com/sound-synthesis/wavetable-synthesis-algorithm/)
