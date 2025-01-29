# TypeScript Type Error with String and Number Addition

This example demonstrates a scenario where TypeScript's type system fails to catch a type error at compile time, leading to a runtime error. The `add` function is designed to add two numbers, but it accepts a string as the second argument. Although TypeScript does not throw an error during compilation, unexpected behavior occurs at runtime.

## Bug

The bug lies in the loose type checking of the `add` function when a string is passed as an argument. Instead of throwing a compilation error, the string is implicitly concatenated to the number. This unexpected behavior can be difficult to detect and debug.

## Solution

The solution involves improving the type checking mechanism to handle string and number addition explicitly. A stricter check can be implemented to enforce that only numeric values are passed as arguments. This can prevent unexpected results caused by implicit type coercion.