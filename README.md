# F# Mutable Variable Swap Bug

This repository demonstrates a common error when working with mutable variables in F#. The `swap` function attempts to swap the values of two mutable variables, but due to how F# handles variable scope, it fails to produce the expected result.

## Bug Description

The `bug.fs` file contains a function that tries to swap two mutable integer variables. The expected output is "20 10", but the actual output is "10 20".  This is because the `swap` function creates local copies of the variables, and modifying these copies does not affect the original variables.

## Solution

The `bugSolution.fs` file demonstrates the correct way to swap mutable variables.  It uses a helper function to explicitly pass the variables by reference using the `&` operator.