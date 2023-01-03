---
title: Rc<T> in Rust
tags: rust computer-science
---

# `Rc<T>` Rust

**Reference counting**, or `Rc<T>` in [[rust|Rust]] is a [[smart-pointers|smart pointer]] that enables multiple ownership, where an address in memory has multiple owners. With `Rc<T>`, data cannot be cleaned up unless there are no more owners, in which case the data can be safely deallocated.

- Useful for allocating data on the heap for multiple parts of a program that cannot be determined at compile time
- Works only in single-threaded applications
- `Rc<T>` is like a TV in the living room - one person can't just turn it off when they're done if other people are watching! Only when everyone's done watching should the last person turn it off.

## Sources

- <https://doc.rust-lang.org/book/ch15-04-rc.html>
