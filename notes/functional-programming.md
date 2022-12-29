---
tags: programming-languages
---

# Functional programming

**Functional programming** is a [[programming-paradigm|programming paradigm]] that calls for

- in a restricted sense, programming without mutable variables, assignments, loops, and other imperative control structures, dealing only with [[theory-computer-science|theories]] on data
- in a wider sense, focusing on pure functions
- in particular, functions can be values that are produced, consumed, and composed

Functional programming can be used like a calculator, within an interactive shell (or REPL, for Read-Eval-Print-Loop)

It's good functional programming style to split up a task into many small functions.

- modularity, ease-of-use

## Functions as first-class

Functional languages treat functions as _first-class values_ - functions are essential building blocks to programs built using functional programming

- a function can be passed as a parameter and returned as a reuslt
  - any function that has this behavior is called a _higher-order function_
- provides a flexible way to compose programs
- makes use of [[anonymous-function|anonymous functions]] for passing functions as parameters

Functions are essential abstractions because they let us introduce general methods to perform computations as explicit and named elements in programming.

- abstractions can be combined with higher-order functions to create new abstractions
- in programming, one must look for opportunities to abstract and reuse
- the highest level of abstraction is not always the best, but it's good to know the techniques of abstraction to use them when appropriate

## Languages

An ideal functional [[programming-language|programming language]] exhibits the following characteristics across different contexts:

- in a restricted sense, the language has no mutable variables, assignments, or imperative control structures
- in a wider sense, the language enables the construction of elegant programs that focus on functions
- in particular, functions in a FP language are first-class citizens, i.e.
  - they can be defined anywhere, including inside other functions
  - like any other value, they can be passed as parameters to functions and returned as results
  - there exists a set of operators to compose functions

### Examples

FP languages in the restricted sense:

- Pure Lisp, XSLT, XPath, XQuery, FP (experimental)
- Haskell (without I/O Monad or UnsafePerformIO)

FP languages in the wider sense:

- Lisp, Scheme, Racket, Clojure
- SML, [[OCaml]], F#
- Haskell (full language)
- [[Scala]]
- Smalltalk, Ruby
- [[JavaScript]]

### History

- 1959: Lisp
- 1975-77: ML, FP, Scheme
- 1978: Smalltalk
- 1986: Standard ML
- 1990: Haskell, Erlang
- 1999: XSLT
- 2000: [[OCaml]]
- 2003: [[Scala]], XQuery
- 2005: F#
- 2007: Clojure

## Sources

- Functional Programming Principles in Scala (Coursera) (TODO: link)
