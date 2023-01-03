---
title: Smart pointers
tags: computer-science rust
---

# Smart pointers

A **smart pointer** is a data structure that acts as a [[pointer]] with additional metadata and functionality.

- Holds an address in memory like a pointer
- Additional information includes reference counting, length or capacity, etc.
- Exists in C++ and [[rust|Rust]]

## In Rust

Rust's smart pointers implement the `Deref` and `Drop` traits, allowing pointers to be dereferenced and deallocate memory, respectively.

The most common smart pointers in Rust are:

- [[box-t|box]] (typed `Box<T>`)
- `Rc<T>`
- `Ref<T>` and `RefMut<T>`, accessed through `RefCell<T>`

Examples of smart pointers "under the hood" in Rust include:

- `String` (see: [[strings-rust|Strings (Rust)]])
- `Vec<T>`

## Sources

- <https://doc.rust-lang.org/book/ch15-00-smart-pointers.html>
