# Unexpected Null Return in Addition Function

This repository demonstrates a subtle bug in a JavaScript function that performs addition. The function unexpectedly returns `null` when one of the inputs is 0, instead of performing the addition. This is because the function uses strict equality (`===`) to check for `null` values.  This is a classic type-coercion issue.

## Bug Description
The function `foo` takes two numeric arguments and returns their sum. However, it uses strict equality (`===`) to check for null values. Strict equality does not perform type coercion, resulting in an unexpected behavior when either `a` or `b` is 0. 0 is considered a falsy value, but it is not null.

## Bug Solution
The solution is to use loose equality (`==`) or to explicitly check for both null and 0. 