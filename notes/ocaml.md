---
tags: cs-421 programming-languages functional-programming
---

# OCaml

OCaml is a general-purpose, multi-paradigm [[programming-language|programming language]] that extends Caml with object-oriented features.

- has much basis in programming language research
- has many features not clearly in most conventional languages
- particularly efficient for programming tasks involving languages (e.g. parsing, compilers, [[user-interface|user interfaces]])

OCaml is industrially relevant, particularly in finance:

- Jane Street trades billions of dollars per day using OCaml
- Major language supported at Bloomberg

Similar languages:

- Microsoft F#
- SML
- Haskell
- [[scala|Scala]]

## OCaml as a Functional Language

Below are some examples of [[functional-programming|functional programming]] concepts in OCaml.

### `'a`

The type `'a` is a _type variable_, standing for any given type.

### Functions with more than one argument

```ocaml
let add_three x y z = x + y + z;;

let add_three =
  fun x -> (fun y -> (fun z -> x + y + z));;
```

In this example, the first definition of `add_three` is syntactic sugar for the second.

### Partial application of functions

See: [[partial-application-functions|Partial application of functions]]

### Functions as arguments

In functional programming, functions can be passed in as arguments to other functions.

```ocaml
# let thrice f x = f(f(f x));;
val thrice : ('a -> 'a) -> 'a -> 'a = <fun>
# let g = thrice plus_two;;
val g : int -> int = <fun>
# g 4;;
- : int = 10
# thrice (fun s -> "Hi! " ^ s) " Good-bye!";;
- : string = "Hi! Hi! Hi! Good-bye!"
```

### Tuple as Values

```ocaml
# let s = (5, "hi", 3.2);;
val s : int * string * float = (5, "hi", 3.2)
```

### Pattern Matching with Tuples

```ocaml
# let s = (5, "hi", 3.2);;
val s : int * string * float = (5, "hi", 3.2)

# let (a, b,c) = s;;  (* (a,b,c) is a pattern *)
val a : int = 5
val b : string = "hi"
val c : float = 3.2

# let x = 2, 9.3;;  (* tuples don't require parentheses in OCaml *)
val x : int * float = (2, 9.3)
```

### Nested Tuples

Tuples can be nested:

```ocaml
let d = ((1,4,62),("bye",15),73.95);;
val d : (int * int * int) * (string * int) * float =
  ((1, 4, 62), ("bye", 15), 73.95)
```

Patterns can be nested:

```ocaml
let (p,(st,_),_) = d;;  (* _ matches all, binds nothing *)
val p : int * int * int = (1, 4, 62)
val st : string = "bye"
```

### Functions on Tuples

```ocaml
let plus_pair (n,m) = n + m;;
val plus_pair : int * int -> int = <fun>
# plus_pair (3,4);;
- : int = 7
# let double x = (x,x);;
val double : 'a -> 'a * 'a = <fun>
# double 3;;
- : int * int = (3, 3)
# double "hi";;
- : string * string = ("hi", "hi")
```

### Match Expressions

OCaml has [[pattern-matching-programming|pattern matching]] capabilities.

The following example takes a triple and figures out how to make a pair out of it.

```ocaml
let triple_to_pair triple =
  match triple
  with (0, x, y) -> (x, y)
  | (x, 0, y) -> (x, y)
  | (x, y, _) -> (x, y);;

val triple_to_pair : int * int * int -> int * int = <fun>
```

Explanation:

- Each clause: pattern on left, expression on right
- Each x, y has scope of only its clause
- Compiler uses first matching clause

## Evaluating declarations

- Evaluation uses an environment $\rho$
- To evaluate a simple declaration `let x = e`
  - Evaluate expression `e` in $\rho$ to value `v`
  - Update $\rho$ with $x v : \{x \rightarrow v \} + \rho$
- Update: $\rho_1 + \rho_2$ has all the bindings in $\rho_1$ and all those in $\rho_2$ that are not rebound in $\rho_1$

```text
{ x -> 2, y -> 3, a -> "hi"} + {y -> 100, b -> 6} =
{ x -> 2, y -> 3, a -> "hi", b -> 6}
```

## Evaluating expressions in OCaml

- Evaluation uses an environment $\rho$
- A constant evaluates to itself, including primitive operators like + and =
- To evaluate a variable, look it up in $\rho: \rho(V)$
- To evaluate a tuple $e_1, ..., e_n$
  - Evaluate each $e_i$ to $v_i$ right to left for OCaml
  - Then make value $(v_1, ... v_n)$
- To evaluate uses of +, \_, etc, eval args, then do operation
- Function expression evaluates to its closure
- To evaluate a local dec: `let x = e1 in e2`
  - Eval `e1` to `v`, then eval `e2` using $\{x \rightarrow v\} + \rho$
- To evaluate a conditional expression: `if b then e1 else e2`
  - Evaluate `b` to a value `v`
  - If `v` is `True`, evaluate `e`
  - If `v` is `False`, evaluate `e2`

## Evaluation of Application with Closures

- Given application expression $f e$
- In Ocaml, evaluate $e$ to value $v$
- In environment $\rho$, evaluate left term to closure, $c = <(x_1,...,x_n) \rightarrow b, \rho'>$
  - $x_1,...,x_n)$ variables in (first) argument
  - $v$ must have form $v+1,...,v_n$
- Update the environment $\rho'$ to

$$
\rho'' = \{x_1 \rightarrow v_1,...,x_n \rightarrow v_n\} + \rho'
$$

## Sources

- CS 421 Programming Languages and Compilers
