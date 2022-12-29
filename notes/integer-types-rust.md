---
title: Integer types (Rust)
tags: rust programming-languages computer-science
---

# Integer Types (Rust)

In [[Rust]], an integer is a [[data-types-rust|data type]] representing a number without a fractional component. Rust supports integer types of explicit sizes and signed/unsigned variants.

| Length  | Signed  | Unsigned |
| ------- | ------- | -------- |
| 8-bit   | `i8`    | `u8`     |
| 16-bit  | `i16`   | `u16`    |
| 32-bit  | `i32`   | `u32`    |
| 64-bit  | `i64`   | `u64`    |
| 128-bit | `i128`  | `u128`   |
| arch    | `isize` | `usize`  |

Signed numbers are stored using two's complement representation.

Each signed variant can store numbers from $-(2^{n-1})$ to $2^{n-1} - 1$ inclusive, where $n$ is the number of [[bit]]s that variant uses.

Unsigned variants can store numbers from 0 to $2^n-1$.

The `isize` and `usize` types depend on the computer architecture, either 64-bit or 32-bit architecture.

If unsure about which type to use, `i32` is a good place to start - although `isize` or `usize` are good when indexing some sort of collection.

## Integer Literals

Note that you can use `_` in numbers literals to make them easier to read.

| Number literals  | Example       |
| ---------------- | ------------- |
| Decimal          | `98_222`      |
| Hex              | `0xff`        |
| Octal            | `0o77`        |
| Binary           | `0b1111_0000` |
| Byte (`u8` only) | `b'A'`        |

## Sources

- <https://doc.rust-lang.org/book/ch03-02-data-types.html#integer-types>
