---
tags: programming-languages functional-programming
---

# Currying

In [[functional-programming|functional programming]], **currying** is a way to define functions piecewise, one parameter section after the other.

Function application associates to the left:

```scala
sum(cube)(1,10) = (sum(cube))(1,10)
```

## Theory

A definition of a function with multiple parameter lists

$$
\text{def f($args_1$)...($args_n)$} = E
$$

where $n > 1$, is equivalent to

$$
\text{def f($args_1$)...($args_{n-1})$} = \text{\{ def g($args_n$) = $E$; g \}}
$$

where $g$ is a fresh identifier. Or, using an [[anonymous-function|anonymous function]]:

$$
\text{def f($args_1$)...($args_{n-1})$} = (args_n \Rightarrow E )
$$

By repeating the process $n$ times,

$$
\text{def f($args_1$)...($args_{n-1})(args_n)$} = E
$$

is shown to be equivalent to

$$
\text{def f = ($args_1 \Rightarrow$ ($args_2 \Rightarrow$ ...($args_n \Rightarrow E$)...))}
$$

**Currying** describes this style of definition and function application, names for 20th century logician Haskell Brooks Curry (1900-1982)

- the idea goes back even further to Schönfinkel and Frege, but the term "currying" has stuck

## Curried vs. uncurried

Examples are in [[ocaml]] from CS 421.

Recall:

```ocaml
# let add_three x y z = x + y + z;;
val add_three : int -> int -> int -> int = <fun>
```

How does this differ from...

```ocaml
# let add_triple (u,v,w) = u + v + w;;
val add_triple : int * int * int -> int = <fun>
```

- `add_three` is **curried**
- `add_triple` is **uncurried**

See example:

```ocaml
# add_triple (6,3,2);;
- : int = 11
# add_triple 5 4;;
Characters 0-10:
  add_triple 5 4;;
  ^^^^^^^^^^^^^^^^

(* This function is applied to too many arguments,
maybe you forgot a `;` *)
```

In OCaml, curried functions can use [[partial-application-functions|partial application]]. Uncurried functions cannot use partial application.

## Sources

- Functional Programming Principles in Scala (Coursera) (TODO: link)
