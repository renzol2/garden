---
title: Convolution reverb
tags: filters cs-448 dsp
---

# Convolution reverb

**Convolution reverb** is an implementation of [[reverb]] that uses [[convolution]] to simulate room reflections.

- Uses convolutions for [[delay-line|delays]]
- When spaced far apart, [[filter]] coefficients sound like echoes

The advantage of reverb via convolution is that it directly matches a room's impulse response.

## Implementation

### Cheating

We can make up a room response, usually wtih the following ideal parameters:

- first 100ms model the early reflections
- rest of response needs a very dense echo output

For early reflections:

- use sparse noise
- ex: cauchy noise (divide two Gaussian noise sequences)

For reverb tail:

- exponentially decaying noise
- for non-colored noise, use white noise
- for colored noise, use other types of noise!

### Using real room impulse responses

We can use real room responses for more accurate convolutions, by either

- downloading them online
- estimating the response of a room

The direct approach to measing room impulse responses is to make an impulsive sound in the room (clap, balloon pop, gun) and measure the resulting sound.

Problems

- extra noises will bias the measurement
  - what if someone drops a coin while recording...
- hard to get an exact impulse sound, since the excitation will most likely be "colored"

A more robust approach: deconvolution

- Excite the room with a more robust signal
- Knowing the excitation, estimate the [[room-impulse-response|RIR]]
- Repeat the experiment multiple times and average out the results for more robustness

By using [[maximum-length-sequences]], we can convolve with a fast and easy computation.

Alternative excitations:

- swept sine excitation (chirp)
- exponential swep sine
- white noise (poor man's MLS)

Some notes on excitations

- longer excitations have more accurate spectra
- noise robustness via repetition - average result out of many trials
- every loudspeaker and microphone has their own response

Or, we could create physical models of rooms and estimate the room response analytically. There are several approaches:

- Finite Element (FE) models
- Image-source methods
- Path/beam tracking

For path/beam tracking:

- explicitly compute the delays from all echoes and use them to construct the [[room-impulse-response|RIR]]
- this gets exponentially more expensive the more echoes you compute

Blending models

- image-source model is great for early reflecitons
- Blend image-source model with other methods

Compensating for physical rooms

- Playback of a simulated room recording inside another room colors the sound even more
- We often measure room responses so that we can undo them and present the desired signal
  - Requires [[equalization]] and removing echoes

## Sources

- CS 448
