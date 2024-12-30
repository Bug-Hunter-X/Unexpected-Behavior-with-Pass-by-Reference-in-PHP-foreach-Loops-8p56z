# PHP Foreach Loop Pass-by-Reference Bug

This repository demonstrates a common, yet subtle, error in PHP involving the use of pass-by-reference in `foreach` loops.  The example highlights how modifications to array elements within the loop using pass-by-reference directly affect the original array, potentially leading to unintended consequences.

The `bug.php` file contains the buggy code, while `bugSolution.php` provides a corrected version.

## How to Reproduce

1. Clone this repository.
2. Run `bug.php` using a PHP interpreter.
3. Observe the unexpected output.
4. Compare the output to the corrected version in `bugSolution.php`.

## Explanation

PHP's `foreach` loop, by default, uses pass-by-reference when iterating over arrays.  This means that changes made to `$value` inside the loop directly affect the original array element. While often convenient, this can lead to bugs if the programmer doesn't anticipate this behavior.

The solution demonstrates how to avoid this pitfall by creating a copy of the array element before making any modifications.