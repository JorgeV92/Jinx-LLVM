# Jinx Compiler

A compiler for the **Jinx** programming language, built using LLVM. This project follows the structure and concepts from the [LLVM Kaleidoscope Tutorial](https://www.llvm.org/docs/tutorial/).

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Introduction

The Jinx Compiler is an experimental language frontend for LLVM, aiming to explore compiler design and language implementation. It serves as a learning platform and a starting point for anyone interested in building programming languages.

## Features

- **Lexical Analysis**: Tokenizes Jinx source code.
- **Parsing**: Generates an Abstract Syntax Tree (AST) from tokens.
- **Semantic Analysis**: Performs type checking and scope resolution.
- **Code Generation**: Converts the AST into LLVM Intermediate Representation (IR).
- **JIT Compilation**: Just-In-Time compiles and executes code.
- **Extensible Design**: Easily add new language features.

## Prerequisites

- **LLVM** (version 10 or higher)
- **C++ Compiler** (supporting C++17 or higher)
- **CMake** (version 3.10 or higher)
- **Git** (for cloning the repository)

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/jinx-compiler.git
   cd jinx-compiler
   ```

2. **Set Up LLVM**

   Ensure that LLVM is installed and the `llvm-config` executable is in your PATH.

3. **Build the Compiler**

   ```bash
   mkdir build
   cd build
   cmake ..
   make
   ```

## Usage

- **REPL Mode**

  Start the interactive Read-Eval-Print Loop (REPL):

  ```bash
  ./jinx
  ```

- **Script Mode**

  Run a Jinx script file:

  ```bash
  ./jinx path/to/script.jx
  ```

## Examples

**Hello World**

```jinx
print("Hello, World!");
```

**Factorial Function**

```jinx
def factorial(n)
  if n <= 1 then
    1
  else
    n * factorial(n - 1);

print(factorial(5));  // Output: 120
```

## Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the Repository**

   Click the "Fork" button at the top right of the repository page.

2. **Create a Feature Branch**

   ```bash
   git checkout -b feature/YourFeature
   ```

3. **Commit Your Changes**

   ```bash
   git commit -am 'Add YourFeature'
   ```

4. **Push to Your Fork**

   ```bash
   git push origin feature/YourFeature
   ```

5. **Submit a Pull Request**

   Open a pull request against the `main` branch of this repository.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [LLVM Project](https://llvm.org/) for providing a robust compiler infrastructure.
- [LLVM Kaleidoscope Tutorial](https://www.llvm.org/docs/tutorial/) for inspiration and guidance.
- Contributors and open-source community for their support.
