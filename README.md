# Haskell Sort Function Bug
This repository demonstrates a common misconception about Haskell's `sort` function from the `Data.List` module.  Many programmers new to Haskell assume `sort` behaves like functions in imperative languages, modifying the input list in place.  This is incorrect.  Haskell's `sort` is pure; it returns a *new* sorted list, leaving the original list untouched. This example illustrates the correct behavior and shows how to properly handle sorted lists in Haskell.

## How to Reproduce
1. Clone this repository.
2. Compile and run `bug.hs` using a Haskell compiler (like GHC).
3. Observe that `xs` and `ys` are not equal despite `ys` containing the sorted elements of `xs`.

## Solution
The solution involves understanding Haskell's immutability and using the returned sorted list (`ys`) instead of expecting `xs` to change.