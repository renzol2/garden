---
tags: music granular-synthesis synthesis audio composition digital mus-305 ece-402 mus-409
---

# Granular Synthesis

Granular synthesis is a method of [[sound-synthesis|synthesizing sound]] that manipulates [[sound-waves|sound]] on the [[microsound]] level.

- like spray-painting; atomizing small portions or windows of a sound and rearranging them in new ways.
- a set of techniques for creating sound constructed from numerous individual sound grains (MUS 409)
  - extremely flexible and multi dimensional
  - no minimum and maximum to what we call a “grain”

## Grain

A **grain** is a short sound [[sampling-composition|sample]], typically 1-100 ms

- the smallest we could get is one [[sampling-signal-processing|sample]]
- lots of situations where we might have granular algorithms that stretch grains to 3-10 seconds - is it really a grain anymore?
- a gray-ish area between granular synthesis and just sampling
- often at or near the threshold of frequency/amplitude discrimination

Input signal segmented into grains, then recombined/resynthesized according to various parameters

## Brief History

- **Isaac Beekman,** “corpuscular” theory of sound, Scientific Revolution (mid 16th-17th)
  - splattering of sound on the ear?
- **Dennis Gabor**, _Acoustical Quanta and the Theory of Hearing_ (1964)
  - proposed that sound could be viewed and understood as quantum particles
  - you could make “any sound” using this particulate approach
  - Gabor constructed an optical/mechanical sound granulator (similar to [[light-tone-organ|Light Tone Organ]])
- Granular synthesis is a popular technique by virtue of its flexibility

## Windowing

**Windowing** in granular synthesis is process of creating grains by applying a short [[amplitude]] [[envelope]].

- shaping the grain - the attack transients
- might be a bell curve, a percussive window function (short attack, long release), any shape under the rainbow is possible

## Applications

It is a technique used in [[music-composition]] and production.

- invention of granular synthesis commonly attributed to **Iannis Xenakis** [(Wikipedia)](https://en.wikipedia.org/wiki/Granular_synthesis#History)

Granular synthesis can be used both functionally and compositionally. Functionally, it can be used for time-stretching audio without changing [[frequency|frequency]]. Compositionally, using granular synthesis on sounds with significant [[transient|transients]] (rather than sustained sounds) can create interesting gestures at the note level.

TODO: take more notes: <https://www.izotope.com/en/learn/the-basics-of-granular-synthesis.html>

## Granular Synthesis Parameters

- **waveform type** - [[sine-wave|sine wave]], sampled sound, etc.
  - earliest fixed granular synthesis only worked on sine waves - there’s quite a lot you can do
- grain **density/frequency** - how many grains per second?
  - synchronous/asynchronous
  - synchronous = exact grains per second (grain frequency)
  - asynchronous = stochastic, random (approximate frequency)
- **gap size/hop size** - time between consecutive grains
  - more specifically, time between the onsets of adjacent grains
  - also called Inter-Onset Time (IOT)
- density/frequency and gap size/hop size seem to be related
  - language depends on the specific granular device
- grain **duration**
- grain **pitch/transposition**
- grain **start position** - from where in the original sample does the grain originate?
- grain **pan** (L/R)
- grain **envelope**/window function
  - triangle, rectangle, tukey, sine, percussive, reverse percussive

## Duration/Spectrum Relationship

TODO: create separate note

- There is an inverse relationship between duration & spectrum bandwidth
- infinitely short sound (impulse) → infinitely wide spectrum
  - impulse response?
- likewise, longer TD events → narrower FD spectra:
  - distinct spectral peaks, esp. for sine waves and other simple waveforms
- unit impulse
- long vs. short grain window
  - granulated 500 Hz sine wave, 100 ms grain duration (pure frequency with a little spectrum widening)
  - granulated 500 Hz sine wave, 1 ms grain duration (wide, crackling broadband noise)
- consequences:
  - short grains → broader, noisier spectrum
  - sharp transients in grain window → similar effect
    - crackling, popping, glitchy texture
- longer grain duration → narrower spectrum, fewer frequency, “smoother” sound

## Sources

- MUS 305 Lecture
- <https://en.wikipedia.org/wiki/Granular_synthesis>
