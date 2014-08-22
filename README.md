# Simhash for Rust
[![Build Status](https://travis-ci.org/bartolsthoorn/rust-simhash.svg?branch=master)](https://travis-ci.org/bartolsthoorn/rust-simhash)

Simhash algorithm (developed by [Moses Charikar](http://www.cs.princeton.edu/courses/archive/spring04/cos598B/bib/CharikarEstim.pdf)) implemented in Rust. It generates 64 bit simhashes and can calculate similarities using the [Hamming distance](http://en.wikipedia.org/wiki/Hamming_distance).

To use simhash append the following lines to your `Cargo.toml` file.
~~~toml
[dependencies.simhash]

git = "https://github.com/bartolsthoorn/simhash-rs.git"
~~~

You can now use it in your project by adding simhash as an extern crate.
~~~rust
extern crate simhash;

fn main() {
  let h: u64 = simhash::hash("The cat sat on the mat");
  println!("{}", h);
}
~~~
