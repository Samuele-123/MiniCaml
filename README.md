# Repository README

## Simple Interpreter for a Functional Programming Language

This repository contains a simple interpreter for a functional programming language implemented in OCaml. The language supports basic arithmetic operations, boolean expressions, and function definitions.

### Language Features

- **Data Types:**
  - Integer (`Int`)
  - Boolean (`Bool`)
  - String (`String`)

- **Expressions:**
  - Arithmetic operations: `Sum`, `Diff`, `Prod`, `Div`
  - Comparison operations: `IsZero`, `Eq`, `LessThan`, `GreaterThan`
  - Logical operations: `And`, `Or`, `Not`
  - Conditional statements: `IfThenElse`
  - Variable binding: `Let`, `Letrec`
  - Function definition: `Fun`
  - Function application: `Apply`

### How to Use

To use the interpreter, you can define your program using the provided abstract syntax and then call the `eval` function with your expression and an optional environment.

Example:

```ocaml
let my_program = Sum(EInt 5, Prod(EInt 2, EInt 3)) in
let result = eval my_program emptyenv in
print_endline (match result with Int n -> string_of_int n | _ -> "Error");
```

### Type System

The language has a simple type system with the following types:
- `TInt`: Integer
- `TBool`: Boolean
- `TString`: String
- `TClosure`: Function
- `TRecClosure`: Recursive Function
- `TUnBound`: Unbound

### Type-checking

The interpreter includes a basic type-checking mechanism to ensure that operations are applied to the correct types.

### Primitives

The language includes primitive functions for arithmetic, comparison, and logical operations.

### Error Handling

Runtime errors are captured using the `RuntimeError` exception, providing informative error messages.

## Additional Documentation
You can find the operational semantics of the language in the included PDF file in this repository.
