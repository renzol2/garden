---
tags: cs-421 programming-languages functional-programming
---

# Partial application of functions

Partial application, also called _sectioning_, allows the partial calling of functions in [[OCaml]].

```ocaml
let add_three x y z = x + y + z;
# let h = add_three 5 4;;
val h : int -> int = <fun>
# h 3;;
- : int = 12
# h 7;;
- : int = 16
```

## Sources

- CS 421 Programming Languages and Compilers
