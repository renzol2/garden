---
title: Box<T> in Rust
tags: rust computer-science
---

# `Box<T>` (Rust)

A _box_ (typed `Box<T>`) in [[rust|Rust]] is a straightforward [[smart-pointers|smart-pointer]] that allocates data on the heap instead of the stack.

- No performance overhead, but also no additional functionality
- Useful for "recursive" data types

## Sources

- <https://doc.rust-lang.org/book/ch15-00-smart-pointers.html>
