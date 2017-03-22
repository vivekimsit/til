The comma operator in JavaScript is interesting.
It takes two arguments, evaluates them both, and itself evaluates to the value of the right-hand argument.

```js
(1, 2)
  //=> 2

(1 + 1, 2 + 2)
  //=> 4
```
