# PHP Object Reference Bug in Foreach Loop

This repository demonstrates a subtle bug in PHP related to object references and foreach loops.  The bug causes unexpected behavior when modifying object properties within a loop.

## Bug Description
The `bug.php` file contains code that attempts to modify the `value` property of multiple objects within a foreach loop.  Due to the way references are handled in PHP, all objects end up with the same final value, rather than each object maintaining its independently modified value.  The `bugSolution.php` file provides a corrected version of the code that avoids this problem.

## How to Reproduce
1. Clone this repository.
2. Run `bug.php` using a PHP interpreter. Observe the unexpected output.
3. Run `bugSolution.php` to see the corrected behavior.

## Solution
The solution involves creating a copy of the object or using a different loop technique that doesn't modify the original objects through reference.