# JavaScript Loose Equality Bug

This repository demonstrates a common but subtle bug in JavaScript related to the loose equality (==) operator and handling of falsy values. The bug arises from the unexpected behavior of loose equality when comparing null and other falsy values (0, false, "", undefined).

## Bug Description
The provided JavaScript function `foo` aims to check if either `a` or `b` is null and return null in that case. However, due to loose equality, it may return incorrect results when `a` or `b` is another falsy value. For example, `foo(0, 5)` would unexpectedly return null, despite neither input being null.

## Solution
The solution is to use strict equality (===) to avoid type coercion and ensure that only null values are correctly handled.
