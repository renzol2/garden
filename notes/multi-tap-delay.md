---
tags: music audio mus-407 digital-audio delay
---

# Multi-Tap Delay

**Multi-tap delay** is a [[fixed-delay-effects|fixed delay effect]] where the original [[audio-signal|signal]] is read multiple times, creating a "multiple delay" effect.

- implemented in a [[circular-queue|circular queue]] with one write pointer and _more than one_ read pointer
- can create a specific pattern of multiple echoes
- may or may not include a [[feedback]] path

![Multi-tap delay signal flow](../public/attachments/multi-tap-delay-signal-flow.png)
