- Open Source systems programming language.
- Advantages:
	- Type Safe - compiler ensures that no operation will be applied to a variable of the wrong type.
	- memory Safe - Rust pointers always refer to valid memory
	- Data Race Safe
	- Zero-cost abstractions
	- Minimal Runtime
	- Targets bare metal

## Installation

- Rust can be installed on your linux using the below commands, for other operating systems visit [rustus.rs](https://rustup.rs/).
``` zsh
$ curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
$ #check rust and cargo versions
$ rust --version
$ cargo --version
```

- The IDE we will be using is **Rustrover** from jetbrains which can be downloaded [Here](https://www.jetbrains.com/rust/download/#section=linux)
## Rust Features
- Offers a collection of features to help manage and organize code referred to as **modules system** which comprises of :
	- **Crates** - This is a compilation unit, the smallest piece of code the rust compiler can run it contains a hierarchy of Rust modules with an implicit, unnamed top module. Code in a crate is compiled together to create a binary executable and are reusable.
	- **Modules** - Help organize your program by letting you manage the scope of the individual code items inside a crate, related code items or items used together can be grouped into the same module.
	- **Paths** - Used to name items in code i.e a vector, code function or module. **Module** feature helps you control privacy of your paths.

## Create Projects with Cargo
- We use a rust build tool and dependency manager called **Cargo** :
	- _cargo new_ - Create new project template
	- _cargo build_ - Build project
	- _cargo run_ - Build and run project
	- _cargo test_ - Test project
	- _cargo check_ - Check project types
	- _cargo doc_ - Build Documentation for project
	- _cargo publish_ - publish crate to [crates.io](https://crates.io/)
- Dependency crates for a project can be added by adding the crate name to the **Cargo.toml** file.
