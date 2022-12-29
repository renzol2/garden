---
tags: rust computer-science programming-languages
---

# Cargo

Cargo is [[Rust]]'s build system and package manager.

- helps manage Rust projects by building code, downloading library dependencies, and building external libraries in packages called _crates_

## Crates

Crates can be classified into a few types:

- _binary crate_, an executable
- _library crates_, which contain code intended to be used in other programs

Crates are specified under the `[dependencies]` line in `Cargo.toml`, where versions are specified with [[semantic-versioning|Semantic Versioning]].

## Usage

- `cargo build` - build a project
- `cargo run` - build and run a project
- `cargo check` - build a project without producing a binary to check for errors
- `cargo build --release` - compile project with optimizations
- `cargo update` - update packages
- `cargo doc --open` - generate documentation for current Cargo project

## Sources

- <https://doc.rust-lang.org/book/ch01-03-hello-cargo.html>
