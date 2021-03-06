# mdBook [![Travis-CI](https://travis-ci.org/azerupi/mdBook.svg?branch=master)](https://travis-ci.org/azerupi/mdBook) [![Crates.io version](https://img.shields.io/crates/v/mdbook.svg)](https://crates.io/crates/mdbook) [![License](https://img.shields.io/crates/l/mdbook.svg)](LICENSE)

mdBook is a utility to create modern online books from markdown files.

**This project is still in its early days.**
For more information about what is left on my to-do list, check the issue tracker


## What does it look like?

The [**Documentation**](http://azerupi.github.io/mdBook/) for mdBook has been written in markdown and is using mdBook to generate the online book-like website you can read. The documentation uses the latest version on github and showcases the available features.

## Installation

There are 2 ways to install mdBook but both require [Rust and Cargo](https://www.rust-lang.org/) to be installed.

##### Install from Crates.io

Once you have installed Rust, type the following in the terminal:
```
cargo install mdbook
```

This will download and compile mdBook for you, the only thing you that will be left to do is add the Cargo bin directory to your path.

##### Install from git

The version published to Crates.io will ever so slightly be behind the version hosted here on Github. If you need the latest version you can build the git version of mdBook yourself. Cargo makes this ***super easy***!

First, clone the repository on your computer:

```
git clone --depth 1 https://github.com/azerupi/mdBook.git
```

Then `cd` into the directory and run:

```
cargo build --release
```

The executable will be in `./target/release/mdbook`.



## Usage

mdBook will primaraly be used as a command line tool, even though it exposes all its functionality as a Rust crate for integration in other projects.

Here are the main commands you will want to run, for a more exhaustive explanation, check out the [documentation](http://azerupi.github.io/mdBook/).

- `mdbook init`

    The init command will create a directory with the minimal boilerplate to start with.

    ```
    book-test/
    ├── book
    └── src
        ├── chapter_1.md
        └── SUMMARY.md
    ```

    `book` and `src` are both directories. `src` contains the markdown files that will be used to render the ouput to the `book` directory.

    Please, take a look at the [**Documentation**](http://azerupi.github.io/mdBook/cli/init.html) for more information and some neat tricks.

- `mdbook build`

    This is the command you will run to render your book, it reads the `SUMMARY.md` file to understand the structure of your book, takes the markdown files in the source directory as input and outputs static html pages that you can upload to a server.

- `mdbook watch`

    When you run this command, mdbook will watch your markdown files to rebuild the book on every change. This avoids having to come back to the terminal to type `mdbook build` over and over again.

### As a library

Aside from the command line interface, this crate can also be used as a library. This means that you could integrate it in an existing project, like a web-app for example. Since the command line interface is just a wrapper around the library functionality, when you use this crate as a library you have full access to all the functionality of the command line interface with and easy to use API and more!

See the [Documentation](http://azerupi.github.io/mdBook/lib/lib.html) and the [API docs](http://azerupi.github.io/mdBook/mdbook/index.html) for more information.

## Contributions

Contributions are highly appreciated and encouraged! Don't hesitate to participate to discussions in the issues, propose new features and ask for help.

People who are not familiar with the code can look at [issues that are tagged **easy**](https://github.com/azerupi/mdBook/labels/Easy). A lot of issues are also related to web development, so people that are not comfortable with Rust can also participate! :wink:

You can pick any issue you want to work on. Usually it's a good idea to ask if someone is already working on it and if not to claim the issue.


## License

All the code is released under the ***Mozilla Public License v2.0***, for more information take a look at the [LICENSE](LICENSE) file
