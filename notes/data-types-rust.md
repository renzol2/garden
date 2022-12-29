---
tags: rust
---

# Data Types (Rust)

Rust is _statically typed_, meaning the compiler must know the data type of all [[variables-rust|variables]] at compile time. However, the compiler can infer the type of most variables through _type inference_.

In [[Rust]], there are two kinds of data types: _scalar_ types and _compound_ types.

## Scalar Types

A scalar type represents a single value. Rust has four primary scalar types:

1. [[integer-types-rust|Integer Types]]
2. floating-point numbers
3. Booleans
4. characters

### Integer Types

See: [[integer-types-rust|Integer Types (Rust)]]

### Floating-Point Types

Rust has two primitive types for floating point numbers (numbers with decimal points).

1. `f32` (32 bits in size)
1. `f64` (64 bits in size)

The default type is `f64` because modern CPUs handle 64-bit floating point numbers at roughly the same speed as `f32`, but with the bonus of having more precision in `f64`.

### Numeric Operations

Rust supports basic numeric operations, including integer division:

```rust
fn main() {
    // addition
    let sum = 5 + 10;

    // subtraction
    let difference = 95.5 - 4.3;

    // multiplication
    let product = 4 * 30;

    // division
    let quotient = 56.7 / 32.2;
    let floored = 2 / 3; // Results in 0

    // remainder
    let remainder = 43 % 5;
}
```

### Boolean Type

The Boolean type in Rust, specified as `bool`, has two possible values: `true` and `false`.

```rust
fn main() {
    let t = true;

    let f: bool = false;  // with explicit type annotation
}
```

### Character Type

Rust's `char` type is the most primitive alphabetic type.

- `char` type is four [[byte]]s in size and represents a Unicode Scalar Value, allowing for many types of characters past ASCII:
  - accented letters, Chinese, Japanese, Korean, emojis, zero-width spaces

## Compound Types

_Compound types_ group multiple values into one type. Rust has two primitive compound types: _tuples_ and _arrays_.

### Tuples

A tuple is a general way of grouping together a _fixed number_ of values _of a variety of types_ into one compound type.

Accessing values from a tuple can be done in two ways:

- destructuring
- period (`.`) followed by index of value to access

Example:

```rust
fn main() {
    let tup: (i32, f64, u8) = (500, 6.4, 1);

    // Destructuring
    let (x, y, z) = tup;

    // Period access
    let five_hundred = tup.0;
    let six_point_four = tup.1;
}
```

A tuple without any values, `()`, s a special type that has only one value, also written `()`.

- the type is called the _unit type_
- the value is called the _unit value_
- Rust expressions implicitly return the unit value if they don't return anything else

### Arrays

Arrays are _fixed length_ collections of multiple values _of the same type_. They are single chunks of memory allocated on the stack.

```rust
fn main() {
    let a = [1, 2, 3, 4, 5];
}
```

Benefits of arrays:

- useful for allocating data on the stack, rather than the heap
- useful to ensure you always have a fixed number of identical-type elements

Declaring an array's type and length explicitly:

```rust
let a: [i32; 5] = [1, 2, 3, 4, 5];
```

Declaring an array of type and identical elements:

```rust
// These are equivalent statements
let a = [3; 5];
let a = [3, 3, 3, 3, 3];
```

Array elements can be accessed by indexing using `[]` notation. If an out-of-bounds index is attempted to be accessed, the program terminates in a _runtime_ error, rather than accessing unsafe memory (i.e. unlike C or C++).

## Sources

- <https://doc.rust-lang.org/book/ch03-02-data-types.html#integer-types>
