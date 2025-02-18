# Julia Function Bug: Floating-Point Precision

This repository demonstrates a subtle bug in a simple Julia function involving floating-point arithmetic and negative numbers. The function aims to square the input, returning the positive value regardless of the input's sign. However, due to how floating-point numbers are represented, the result for negative numbers is not always perfectly accurate.

## Bug Description
The `myfunction` squares its input, producing a positive result.  However, due to the way the negative number is handled, there could be minor inaccuracies caused by floating-point precision differences in Julia between `x^2` and `-x^2` for negative x.

## Bug Solution
The solution involves using `abs()` to ensure the result is always positive, eliminating issues that can arise from directly negating a squared floating-point number.