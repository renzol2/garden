---
title: Audio plugin anatomy
tags: dsp audio audio-programming
---

# Audio plugin anatomy

The anatomy of an audio plugin can be broken down into several main parts:

1. DSP
2. Parameters
3. Preparing DSP before processing audio samples
4. Processing audio at a regularly occurring intervals
5. GUI

## DSP Code

Audio plugins utilize [[digital-signal-processing|DSP]] implementations in code to process audio, since audio software works with [[digital-audio|digital audio]].

## Parameters

The DSP of a plugin can be controlled by users through parameters that are specified by the plugin. These parameters can control any number of facets of the plugin, and can also be automated by a plugin host.

## Preparing DSP

Hosts allow plugins to prepare DSP before processing audio. This stage is important for some plugins to initialize the DSP, like allocating memory for [[delay-line|delay lines]] or performing expensive computations.

## Processing audio in blocks

To prevent sending large amounts of [[sampling-signal-processing|samples]], audio plugins break up incoming audio signals into _blocks_ or _buffers_. The size of incoming/outgoing buffers can be set in audio plugin hosts, like DAWs.

The **buffers per second** processed by an audio plugin is determined by `sample rate / buffer size`.

The DSP of a plugin must be fast enough to process all these blocks at the specified rate, since the host of a plugin will not wait. Otherwise, the plugin will cause unwanted artifacts (clicks, pops, noise, etc).

## GUI

Users often interact with plugins through their GUI. The GUI needs to be intuitive and easy to understand for the user, and the GUI needs to reflect the state of the plugin at all times.

## Sources

- <https://www.youtube.com/watch?v=Mo0Oco3Vimo>
