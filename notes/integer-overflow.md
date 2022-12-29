---
tags: computer-science
---

# Integer Overflow

**Integer overflow** is a phenomenon that occurs when a variable's value is changed to a value outside its designated range.

- for ex. in [[Rust]], integer overflow occurs when the [[integer-types-rust|integer type]] `u8` variable's value goes outside its range of values between 0 and 255.

In most programming languages, integer overflow causes _two's complement wrapping_, where the value "wraps around" the minimum or maximum of the values the variable's type can hold.

## Sources

- <https://doc.rust-lang.org/book/ch03-02-data-types.html#integer-types>
