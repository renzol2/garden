---
tags: mus-407 midi
---

# MIDI Message Format

A [[MIDI]] message consists of one or more _[[byte]]s_ in the following format:

- a _status_ byte followed by zero, one, or two _data_ bytes
- status bytes begin with a `1`, data bytes begin with a `0`

- 1 byte = 8 bits
- 1 [[bit]] = smallest digital unit, corresponding to zero or one ("off" or "on")
- a UART chip (Universal Asynchronous Receiver/Transmitter) receives and processes binary signal into usable data
- MIDI messages sent at 31,250 bits/sec
  - exact division of 1 mHz to facilitate synchronization with early CPUs

## Example

Scenario: **pressing** and **releasing** a key on a MIDI keyboard controller

**How many MIDI messages are generated?** _Two_.

- A _note-on_ message when we press the key
- A _note-off_ message when we release the key

**How many bytes are generated?** _Six_. Each message contains three bytes:

- A _status byte_ specifying message type and channel
- A _data byte_ specifying note number
- A _data byte_ specifying note velocity

### Binary vs. Decimal Data

Every MIDI message starts with exactly one status byte followed by an arbitrary amount of data bytes.

Example:

- A MIDI Note On message starts with a status byte indicating that it is a 'Note On' message, followed by additional metadata such as key number, velocity, etc.

### Note-On Message, Deconstructed

```text
10010010

Breaking up into sections, starting from left:
1 -> indicates status byte
001 -> message type, 8 possibilities (001 = note on)
0010 -> message channel, 16 possibilities: 0010: channel 3 (0-indexed)
```

```text
00111100
Note number: 60 (decimal)
```

```text
01100101
Note velocity: 101 (decimal)
```

## Sources

- MUS 407 MIDI
