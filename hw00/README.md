# Homework 00: Hello Rust & Hello Cargo!

**Due Thursday, 2019-01-18, 18:00.**

For questions, please use the matrix channel.
Links on homepage.

#### Classroom for GitHub

If there is no starter code, such as in this homework, you can use Cargo to
initialize the git repository for you. See below. But first, Rust!

## Installing Rust

For this homework, all you'll have to do is install the Rust compiler (rustc)
and the Rust package manager (Cargo). We'll be using Rust v1.31 for this class.
(This homework doesn't depend on the version of Rust, so it's fine to get
started early.)

We recommend using [rustup][https://www.rust-lang.org/tools/install], a tool to manage multiple
installations of Rust on your system. Rustup supports Linux, OS X, and
Windows.

Rustup maintains a user default toolchain version (stable, beta, or
nightly). Run `rustup default stable` to set your user preference to stable.
This will also download the stable toolchain.

**On Linux, OS X**
Install rustup by following the [instructions on the rust
website][https://www.rust-lang.org/tools/install].
You can also use your local friendly package manager and install cargo and
rustc directly.

To check that Rust and Cargo are installed properly, run the following commands
and make sure the output matches below:

```
$ rustc --version
rustc 1.31.1 (b6c32da9b 2018-12-18)
$ cargo --version
cargo 1.31.0 (339d9f9c8 2018-11-16)
```

When a new version is released, you should update your version of Rust,
using `rustup update`.

## Hello, Rust!

Now that Rust is ready to roll, let's write our first "hello world" program.
Create a file named `main.rs` and modify the code snippet below to print out
"Hello, \<your name\>!".

```rust
fn main() {
    let name = "Ferris"; // Ferris is the name of Rust's unofficial crustacean mascot
    println!("Hello, {}!", name);
}
```

Once you've created your program, compile it using `rustc main.rs` and run the
resulting `main` binary to test it. Boom! You did it! You're a Rust programmer
now! 🎊🎉👍

## Hello, Cargo!

Rust has a fantastic package and build manager, Cargo, which is modeled from
years of learning from other languages. Cargo handles all the gory build
automation and dependency management details for you, so that you don't have to
worry about it when creating (or building or updating) a project.

Using `rustc` directly is fine for small projects, but Cargo really helps to
remove a lot of the friction of manual project management. If you've ever used
`rake` or `pip` for dependency management, Cargo is like those, plus all of the
build power provided by a good `Makefile`.

To make a new project for homework 0, run the command
`cargo new --bin hw00` (which will *create* the folder `hw00`).

Why `--bin`? We want this project to create a standalone executable, rather than
a library that can be rolled into other projects.

If you are not already in a git repository when you create your project, Cargo
will create a git repository (and `.gitignore`) for you. Then, you can add this
your GitHub repository as a git remote as follows:


```
git remote add origin git@github.com:username/hw00-<username>.git
git push -u origin master
```

Cargo creates this directory structure for you:

```
hw00
├── Cargo.toml
└── src
    └── main.rs

1 directory, 2 files
```

You may notice that the `main.rs` file Cargo creates looks suspiciously
similar to the "Hello World" code above. Since you've already written your
"Hello World" program, move the file you created into `src`, and overwrite
the `main.rs` that Cargo generated.

To finish things off, let's build our project. Simply run `cargo build` from any
directory in the project tree! You can run your executable with `cargo run`.
Pretty magic, huh?

## Bonus: Configuration

Adding to your personal environment setup is one of the many joys of starting
a new programming language. Rust has a pretty decent amount of support for being
new to the game.

Take a look at [this list of editor configs][configs.md]. There are more
unofficial or less-supported ones out there, so it's worth looking around. If
you aren't sure what to use, all three of your instructors use vim :)

  [configs.md]: https://github.com/rust-lang/rust/blob/master/src/etc/CONFIGS.md

## Submission

Commit and push your work to the master branch of your Classroom for Github
repository for this HW. **Make sure it is visible on Github!** This is your
submission. (Work must be in the master branch at the due time.)

That's it! ok bye get outta here :point_right:
