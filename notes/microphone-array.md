---
title: Microphone array
tags: cs-448
---

# Microphone array

A **microphone array** is a group of [[microphones]] working in tandem.

The most common microphone array is a linear microphone array, placed in a line and all facing the same direction.

Microphone arrays are commonly used with [[omnidirectional]] microphones to get a uniform response from all directions.

## Hardware concept

Similar to how a parabolic dish focuses [[sound-waves|sound]], we can simply use an array of microphones placed in a parabola to focus on sound coming in front.

## Software concept

Instead of actually placing more microphones to create this array, we can virtually move microphones using time delays on the recorded [[audio-signal|signal]].

- we can implement this using [[convolution]]

### Formal process

To actually implement this, we'll do the following:

- using filter instead of delays, since they're more flexible
- we work in the [[frequency-domain|frequency domain]]

When sound hits the microphone straight on, we can simply sum the signal across microphones.

When sound hits the microphone at an angle, we have to delay the signal hitting the further microphone by a certain amount.

This delay is essentially a [[phase]] shift, which can be achieved by moving the signals to the frequency domain via [[discrete-fourier-transform|DFT]] and multiplying the appropriate frequency bins by a complex number $v_i$, which achieves the phase shift.

- $v_i$ can also tell us how much to scale the phase-shifted signal, to simulate the signal losing energy over some distance

Each direction is associated with a **steering vector**, which models sound propagation effects.

- for every angle (microphone), we make a steering vector that tells us how to phase shift the frequencies at each microphone

## Far field model

We assume that the incoming sound wave is planar because the sound is so far that the spherical wave curvature is gone.

$$
dt = \frac{r \cos \theta}{C}
$$

If we don't know the angle of localization, we can measure the delay between channels to infer that angle.

### From angle to time-delay

Known as _TDOA_ estimation (time difference of arrival). The basic idea is to find how much to delay one of the recordings so that it aligns with the other recording best. There will be no exact match due to [[noise]] and other finnicky problems. We can accomplish this with [[cross-correlation|cross correlation]].

$$
\theta = cos^{-1}\frac{dt * C}{R}
$$

### In the digital world

We consider the angle of incidence, resulting in a sample delay, which corresponds to a phase shift.

$$
\theta \rightarrow dn = \frac{r \cos \theta}{C} R
$$

where $R$ is the [[sample-rate|sample rate]].

This lets us compute the steering vector for frequency $k$:

$$
v_2 = e^{-jdn \frac{2 \pi}{N} k}
$$

We need a unique steering vector for each microphone for each frequency that we compute.

## Directional response

Directional response describes the array response at any angle, which we can measure using a delta function (i.e. just measuring the steering vectors).

TODO: insert linear arrays with $M$ mics equation

To visualize these directional responses, we usually use a polar plot to map its [[polar-pattern|polar pattern]], like what we'd do with single microphones

For low frequency signals, their wavelength is so long that microphones that are very close together often receive the same signal.

- i.e. it's harder to [[localization|localize]] lower frequencies

For high frequency signals, the smaller wavelength means that microphone arrays have a stronger directional response towards focused areas.

## Generalizing to wideband inputs

Most sounds are not single sinuosoids - they have complex [[spectrum|spectra]]. This means we have more steering vectors per microphone.

TODO: insert linear arrays with $M$ mics equation

## Focusing towards one direction

- Undo the effects of the steering vector by "steering" the array towards a location
- Take mic inputs and modulate by certain phase shift
  - invert propagation delays so that all microphone inputs superimpose exactly


## Sources

- CS 448: Microphone Arrays
