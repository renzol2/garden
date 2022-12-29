---
tags: cs-421 programming-languages functional-programming
---

# Continuation passing style

In [[functional-programming|functional programming]], **continuation-passing style** (CPS) is a style of programming in which control is passed explicitly in the form of a [[continuation]].

- A compilation technique to implement non-local control flow, especially useful in interpreters
- A formalization of non-lcoal control flow in denotational semantics
- Possible intermediate state in compiling functional code

CPS is used for the following reasons:

- Makes [[order-of-evaluation|order of evaluation]] explicitly clear
- Allocates variables (to become registers) for each step of computation
- Essentially converts functional programs into imperative ones
  - Major step for compiling to assembly or byte code
- [[tail-recursion|Tail recursion]] is easily identified
- Strict forward recursion converted to tail recursion
  - At the expense of building large closures in heap
- Preserves order of evaluation through continuations
- Use of continuations can also change order of evaluation
- Also implements:
  - Exceptions and exception handling
  - Co-routines
  - (pseudo, aka green) threads

## Sources

- CS 421 Programming Languages and Compilers
