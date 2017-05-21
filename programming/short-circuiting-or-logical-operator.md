#### Logical operator semantics

It’s best to think of `||` and `&&` as control-flow operators.
The expression on the left is always evaluated, and its value
determines whether the expression on the right is evaluated or not.

So, we can say that unlike function arguments not all expressions
are eagerly evaluated.

```
const even = (n) =>
  n === 0 || (n !== 1 && even(n - 2))

even(42)
  //=> true
```
