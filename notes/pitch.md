---
tags: mus-407 sound sound-perception pitch cs-448
---

# Pitch

**Pitch** is the subjective human response to [[frequency]].

- characteristic by which tones are ordered from low to high
- generally, it relates to the rate of waveform repetition

## Perception

It is _culturally_ related to frequency, but

- frequency is quantifiable and observable - number of cycles per second
- pitch is simply our subjective perception of frequency
- pitch can be ambiguous
- the same frequencies can be different between different backgrounds and even situational contexts

We might "hear" some infrasonic frequencies, but we do not perceive their pitch

- instead, we perceive a regular rhythmic pattern
- phenomenon of [[psychoacoustics]]

## Description

In Western notation, pitch is often notated within the [[tet|twelve equal temperament system]].

- each individual pitch falls within one of 12 [[pitch-class|pitch classes]] and some octave
- also commonly used with [[midi|MIDI]], equating certain key number values to pitch

## Across fields

For speech, we use the term $F \varnothing$ (f-zero); the frequency of the lowest periodic element

- F1 is the first harmonic, F2 is the second harmonic, etc.

For music, we use notes (e.g. C#, Bb, etc.), as well as the [[fundamental]] frequency

## Formal definition

Periodicity: $s[t+P] = s[t]$

A function that repeats every $P$ samples, where $P$ defines pitch.

## Real-world version

Quasi-periodicity: $s[t + P] = f(s[t])$

where $f(x) = x + C$, or $f(x) = ax$ (i.e. almost periodic, but not quite)

## From the frequency perspective

An (approximately) [[harmonic]] sound is composed of several harmonics, where the fundamental frequency $f_0$ can change over time.

- the signal can also be [[noise|noisy]], or slightly aperiodic
- each harmonic can have its own [[amplitude]] and [[phase]] at any given point in time

Together, these factors create the perception of pitch.

## Why care about pitch

### Speech pitch analysis

- Measure intonation, prosody, emotion, etc.
  - e.g. identify a question from rising pitch in the end
  - identify [[depression]], [[autism-spectrum-disorders|autism]], speech impediments, etc.
- Used for tonal language analysis

### Music

Some musical applications of pitch analysis:

- Music pitch tracking
- Analyzing historical recordings
  - Music transcription and musicological analysis
  - Performance analysis
- Finding melodies
  - Query by humming; melody tracking

## Sources

- [MUS 407 Sound, Acoustics, & Psychoacoustics](https://prezi.com/view/ZcqvwosFJCFJQtQrbP75/)
- CS 448: Pitch tracking and modifications
