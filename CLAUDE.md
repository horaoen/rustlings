# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the **Rustlings Official Solutions** repository containing solutions for the Rustlings Rust learning exercises. Rustlings is a collection of small exercises to get you used to reading and writing Rust code.

### Structure

- **exercises/**: Directory containing incomplete exercise files that users need to fix
- **solutions/**: Directory containing complete solutions to all exercises
- Each exercise has two versions: the original (without `_sol` suffix) for users to complete, and a solved version (with `_sol` suffix)

### Exercise Categories

The exercises are organized by topic and map to corresponding chapters in "The Rust Programming Language" book:

1. **Introduction** (`00_intro/`) - Basic setup and greeting
2. **Variables** (`01_variables/`) - Variable declarations and mutability
3. **Functions** (`02_functions/`) - Function definitions and parameters
4. **Control Flow** (`03_if/`) - If expressions and conditionals
5. **Primitive Types** (`04_primitive_types/`) - Basic data types and type inference
6. **Vectors** (`05_vecs/`) - Dynamic arrays and vector operations
7. **Move Semantics** (`06_move_semantics/`) - Ownership and borrowing fundamentals
8. **Structs** (`07_structs/`) - Custom data structures
9. **Enums** (`08_enums/`) - Enumerated types and pattern matching
10. **Strings** (`09_strings/`) - String handling and slices
11. **Modules** (`10_modules/`) - Code organization and visibility
12. **HashMaps** (`11_hashmaps/`) - Key-value collections
13. **Options** (`12_options/`) - Optional values and null safety
14. **Error Handling** (`13_error_handling/`) - Result types and error propagation
15. **Generics** (`14_generics/`) - Generic types and traits
16. **Traits** (`15_traits/`) - Shared behavior and trait implementations
17. **Lifetimes** (`16_lifetimes/`) - Reference lifetimes and borrowing
18. **Tests** (`17_tests/`) - Unit testing and assertions
19. **Iterators** (`18_iterators/`) - Iterator patterns and functional programming
20. **Smart Pointers** (`19_smart_pointers/`) - Box, Rc, Arc, and other smart pointers
21. **Threads** (`20_threads/`) - Concurrent programming
22. **Macros** (`21_macros/`) - Metaprogramming with macros
23. **Clippy** (`22_clippy/`) - Code linting and best practices
24. **Conversions** (`23_conversions/`) - Type conversions and traits

## Common Development Commands

### Building and Running Exercises

```bash
# Build a specific exercise (example: variables1)
cargo build --bin variables1

# Run a specific exercise
cargo run --bin variables1

# Build and run in one command
cargo run --bin variables1

# Run the solution version
cargo run --bin variables1_sol
```

### Testing and Validation

```bash
# Check for compilation errors without building
cargo check --bin variables1

# Run with clippy for linting (configured in rust-analyzer.toml)
cargo clippy --bin variables1 --profile test

# Build all exercises (useful for validation)
cargo build
```

### Working with Solutions

```bash
# Compare exercise with solution
diff exercises/01_variables/variables1.rs solutions/01_variables/variables1.rs

# Run solution to see expected behavior
cargo run --bin variables1_sol
```

## Development Notes

### Configuration

- **rust-analyzer.toml**: Configures rust-analyzer to use `clippy` for checking with test profile
- **Cargo.toml**: Defines all exercises as separate binaries with both exercise and solution versions
- **Edition**: Uses Rust 2024 edition
- **Lint Configuration**: Strict linting rules forbidding unsafe code, todo!(), infinite loops, and memory leaks

### Exercise Structure

Each exercise typically follows this pattern:
1. **Problem**: Code with compilation errors or logic issues
2. **TODO Comments**: Indicate what needs to be fixed
3. **Incremental Learning**: Builds on concepts from previous exercises
4. **Self-Contained**: Each exercise focuses on specific concepts

### Working on Exercises

When helping with exercises:
1. Identify the specific concept being taught (ownership, borrowing, traits, etc.)
2. Provide minimal fixes that demonstrate the concept
3. Avoid introducing unnecessary complexity
4. Follow Rust best practices and idiomatic patterns
5. Ensure the solution compiles and runs correctly

### Common Issues to Address

- Missing type annotations
- Ownership and borrowing violations
- Incorrect use of `Option` and `Result` types
- Missing trait implementations
- Lifetime annotation errors
- String vs &str confusion
- Mutable vs immutable bindings

## Important Notes

- This is a **solutions repository**, not the main Rustlings project
- Solutions are provided for reference and learning
- Multiple valid solutions may exist for some exercises
- Focus on clear, idiomatic Rust code
- Prioritize correctness and readability over cleverness