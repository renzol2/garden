---
tags: ece-402
---

# Fourier Inversion Theorem

The **Fourier inversion theorem** states that it is possible to recover a function from its [[fourier-transform|Fourier transform]].

**Intuitively**: if we know all frequency and phase information about a wave, then we can reconstruct the original wave precisely.

## Application

The application of the Fourier inversion theorem is very common through this basic strategy:

- apply the Fourier transform on a signal
- perform some operation or simplification on the Fourier transform
- apply the inverse Fourier transform to obtain a modified version of the original signal

### Sound

Applying the Fourier inverse theorem in sound and audio relies on the above basic strategy. For ex:

- identifying unwanted [[frequency|frequencies]] in a [[dry-wet-signal|dry signal]] using Fourier transform, removing those unwanted frequencies with [[equalization|EQ]], and applying inverse Fourier transform to obtain the wet signal

## Sources

- <https://en.wikipedia.org/wiki/Fourier_inversion_theorem>
