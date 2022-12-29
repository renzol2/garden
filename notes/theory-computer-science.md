---
tags: computer-science programming-languages
---

# Theory (mathematics, programming)

In mathematics & programming, a **theory** consists of

- one or more data types
- operations on these types
- laws that describe the relationships between values and operations

Normally, a theory does not describe mutations!

- i.e. theories define operations without [[side-effect-programming|side effects]]
- e.g. theory of polynomials, theory of [[string|strings]] and [[string-concatenation|string concatenation]]
  - there are no operators to change an element while keeping the sequence the same

## Consequences for programming

Implementing high level concepts in [[programming-language|programming languages]] and [[programming-paradigm|paradigms]] following mathematical theories calls for _no mutation_

- theories do not admit mutation
- mutationc an destroy useful laws in the theories

Therefore, we

- concentrate on defining theories for operators expressed as functions
- avoid mutations altogether
- have powerful ways to abstract and compose functions

## Sources

- Functional Programming Principles in Scala (Coursera) (TODO: link)
