---
tags: computer-science api
---

# Application Binary Interface

An **application binary interface (ABI)** is a connection between two binary program modules. Usually, one of these modules is a library or operating system facility, and the other is a program being run by a user.

The main difference between [[application-programming-interface|API]]s and ABIs lie in their domain within a computer:

- an ABI defines how data structures and computational routines are accessed in _machine code_: a low-level, hardware-dependent format
- an API defines these accesses are implemented in _source code_: a higher-level, hardware-independent, human-readable format

A common convention in ABIs is the _calling convention_, which determines how data is provided as input to, or read as output from, computational routines.

![API vs. ABI diagram](../public/attachments/api-abi-diagram.png)

## Sources

- <https://en.wikipedia.org/wiki/Application_binary_interface>
