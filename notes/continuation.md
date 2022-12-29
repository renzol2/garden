---
tags: cs-421 programming-languages
---

# Continuation

A **continuation** is a programming technique for all forms of "non-local" control flow:

- non-local jumps
- exceptions
- general conversion of non-tails to tail calls

Essentially, it's a higher order function of GOTO.

## Usage

The idea of continuations is to use functions to represent the control flow of a program.

The method of using continuations is to have each procedure take a function as an extra argument with which to pass its result. An outer procedure "returns" no result.

- The function receiving the result is called a _continuation_.
- The continuation acts as an "accumulator" for work to still be done.

Writing procedures in such a way is called [[continuation-passing-style|CPS]].

## Sources

- CS 421 Programming Languages and Compilers
