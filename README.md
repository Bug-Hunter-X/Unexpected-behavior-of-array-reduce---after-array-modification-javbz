# Unexpected Behavior of `reduce()` after Array Modification in Swift

This example demonstrates a common misconception regarding the immutability of `reduce()` operations on arrays in Swift.  Modifying an array after a `reduce()` operation does not affect the result of the `reduce()` call, as it operates on a copy of the array.

## The Problem:

The `reduce()` function creates a copy of the array at the time of its execution.  Therefore, subsequent changes to the original array do not impact the results already calculated by the `reduce()` function. This often leads to unexpected behavior.

## The Solution:

To achieve the desired outcome (dynamically updating the sum after array modification), use a variable to store the sum, and then update this variable whenever the array is updated.