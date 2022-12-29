---
tags: cs-421 programming-languages functional-programming
---

# Environment (programming)

An **environment** records what value is associated with a given identifier

- Environments are central to the semantics and implementation of a [[programming-language|programming language]]
- Specifically important in [[functional-programming|functional programming]]
- Think of environments as a _cloud of bindings_
- In [[ocaml|OCaml]], variables are reassigned values and old values are discarded completely

Notation:

$\rho = \{\text{name}_1 \rightarrow \text{value}_1, \text{name}_2 \rightarrow \text{value}_2, ...\}$

Environments are often stored as a list or a stack.

- To find value start from left and take first match
- Implementation can involve: association lists, hash tables, pre-defined mapping functions, etc.

## Sources

- CS 421 Programming Languages and Compilers
