# F# Mutable Variable Swap Bug

This repository demonstrates a common misunderstanding regarding mutable variables and function scope in F#.  The `swap` function, intended to exchange the values of two mutable variables, fails to do so correctly.  The solution illustrates the proper way to handle mutable variables within functions to achieve the desired swap behavior. 

## Bug Description

The provided F# code attempts to create a function that swaps the values of two mutable integer variables. However, due to a misunderstanding of how F# handles mutable variables within function scopes, the swap function doesn't work correctly. The values of x and y remain unchanged after the call to the `swap` function.

## Solution

The solution demonstrates how to correctly swap the values by passing the mutable variables as ref arguments to the function and using the <- operator to modify their values. This ensures that the changes made within the swap function persist after the function call.

## How to reproduce the bug:
1. Compile and run the provided bug.fs. Note that the values of x and y do not change after the call to the swap function. 
2. Next, open and run bugSolution.fs. Note that the values of x and y are correctly swapped after the call to the swap function.