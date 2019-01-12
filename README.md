# arsert

## arsert - assertions that fail very sophisticatedly

This crate allows you to write assertions like you would with a
builtin [`assert`][assert], but when the assertion fails, it outputs
diagnostic information about the parameters to the assertion.

### Usage

Here's a failing assertion:

```rust should_panic
use arsert::arsert;
let x = 1;
let y = 2;
arsert!(x == y); // Fails and tells you the values of `x` and `y`
```rust

Here's a successful one:

```rust
use arsert::arsert;
let x = 20 as i64;
arsert!(x <= x.pow(3));
```

### The Name

Sorry for the toilet humor (everybody poops, y'all). Name improvement
suggestions gladly accepted, provided the resulting name is terse and
meaningful.

License: MIT
