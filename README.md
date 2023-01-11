# Welcome to the Rust Tutorial for C++ Programmers

This tutorial is designed to help C++ programmers learn the Rust programming language. The tutorial is organized as a series of examples and exercises that build on each other.

## Prerequisites

To get the most out of this tutorial, you should have prior experience programming in C++ including the use of smart pointers and familiarity with templates, generic programming, and move semantics. Familiarity with basic concepts such as variables, functions, control flow is also assumed.

## Setup

This tutorial is based on Jupyter notebooks, you can read them on Github but to run the code examples and exercises, you will need to install `evcxr` Jupyter kernel. To install `evcxr`, you will need `cargo`, Rust's package manager, which should have been installed when you installed Rust. You can download the latest version of Rust at the official website: https://www.rust-lang.org/learn/get-started.

To install `evcxr`:
1. Install jupyter: `pip install jupyter`
2. Open the terminal and type: `cargo install evcxr_jupyter` 
3. Then to register the kernel: `evcxr_jupyter --install`

You can use your preferred text editor or IDE to work on the code examples and exercises and you can also use Jupyter Notebook that allows you to run code inside the browser.

Note: if you face any installation issues you can refer to the `evcxr` documentation at https://github.com/google/evcxr

## Tutorial Content

The tutorial is divided into several sections, each covering a different topic. The sections are as follows:

0. **Introduction**: An overview of the Rust syntax. Variable declaration, if, for, while, arrays, functions and closures are covered at the syntax level.

1. **Thread Safety**: It covers scoped threads, references and borrowing rules, Mutex, RwLock, Atomics and interior mutability.

2. **Memory Safety**: This one is the biggest chapter of the tutorial. It has several sections:
    - Move and copy types, ownership and lifetimes of references.
    - `Option`, how it fills the need for null pointers, begining of the pattern matching.
    - Bound checking, pointers of unsized types.
    - Heap, smart pointers `Box`, `Vec`, `Arc` and `Rc`.
    - Memory leaks, static variables and compile time evaluation.
    - Relation of mutabilty, borrow rules and thread safety to the memory safety. Single threaded interior mutability type `RefCell`.

3. **Object-Oriented Programming**: It starts with the syntax of defining method for data types, then it goes with traits and its using in `dyn Trait` and
  generic functions. It also covers auto traits, super traits, associated types, derive, and some of the traits with special meaning in language, like `Drop`, `Debug`, `Display`, `Add`, `Iterator`, `IntoIterator`, `Clone`, `Copy`, `Sync` and `Send`.

4. **Functional Programming**: This chapter concepts is new for most C++ developers. It includes:
    - Enums with data (Sum types), how to use them with pattern matching, and their binary representation.
    - Iterators, how they are memory safe in Rust unlike C++, iterator adapters like `.filter` and `.map` and how to write for-less code with them.
    - Closures (lambda functions in C++) and how they capture variables from environment, while tracking mutability, thread safety and memory safety.

5. **Error handling**: A look at how Rust supports error handling by return value, similar to C, which is better for system programming than stack unwinding
    exceptions, while vastly improving its ergonomics with `Result` type and the `?` operator. And it covers panic, `catch_unwind`, and when to use `Result` and
    when to use panic for errors.

6. **Unsafe Code and FFI**: This chapter covers the concept of safe abstractions, unsafe operations, raw pointers, `transmute`, `union`, how to implement a vector like thing, how to
    call C functions and use `bindgen` to generate Rust equivalent definitons for C header files, a look into the inline assembly in Rust and why `unsafe` Rust should be avoided as much as possible.

7. **Macros**: An introduction to Rust declarative macros and comparasion with C preprocessor macros, with a small look to procedural macros and `syn` and `quote` crates.

8. **Asynchronous Programming**: It starts with writing a simple sleep function in blocking and non blocking mode, then it introduces `Future` as an abstraction
    over a non blocking work. Then we will see a simple and stupid executor and reactor for polling our future, and `async` and `await` syntax for composing futures. Finally
    we will use `tokio` instead of our simple runtime, and we will see some shortcomings of `async` language features in Rust.

At the end of each part, there are some exercises.

## Additional Learning Materials

In addition to this tutorial, there are a variety of other resources available to help you learn Rust. Here are a few recommendations:
- **The Rust Programming Language Book**: This is the official book for the Rust programming language. It's well suited for general audience and beginners, but experienced C++ programmers may find it to be a bit slow-paced or redundant in some sections. It is available online at https://doc.rust-lang.org/book/
- **Rust by Example**: This is a collection of example programs that demonstrate different Rust features and idioms. It is available online at https://doc.rust-lang.org/rust-by-example/
- **Rustlings**: A small collection of exercises to help you learn the basics of Rust. It is available on GitHub at https://github.com/rust-lang/rustlings
- **Rust Communities**: Rust has a vibrant and welcoming community, and there are many places to get help and ask questions. Some popular options include the Rust programming subreddit (https://www.reddit.com/r/rust/), the Rust programming Discord server (https://discord.gg/rust-lang) and Rust users discourse (https://users.rust-lang.org).
- **Rust for C programmers**: A guide that helps C programmers to learn Rust, helpful for systems-level development. It is available online at https://docs.opentitan.org/doc/ug/rust_for_c/
- **Rustonomicon**: A guide for writing unsafe code in Rust, which is a must read before writing any unsafe code. It is available online at https://doc.rust-lang.org/nomicon/
- **Rust with entirely too many linked lists**: A book which teaches the concept of ownership and lifetime in Rust by implementing some examples of linked lists. The exercise in chapter 2 is
    inspired by this book. It is available online at https://rust-unofficial.github.io/too-many-lists/

These resources, along with practice and experimenting with the language, should give you a strong foundation in Rust and help you become a proficient Rust programmer.

## Getting Help

If you have any questions or run into any problems while working through the tutorial, feel free to open an issue on the GitHub repository.

## Contributing

This tutorial is open-source and contributions are welcome. If you find any errors or think of a way to improve the tutorial, please open a pull request with your changes.
