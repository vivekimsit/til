# til
Lets learn something everyday.

# Javascript

Map

```
 var m = {};
 var a = {id: 1},
     b = {id: 2};
 m[x] = 'foo';
 m[x] = 'bar';
 
 m[x]?
 m[y]?
```

WeakMap

1. WeakMap take only object as keys.
2. They don't have `size` or `clear` method.
3. They don't have iterartor over `keys`, `values` or `entries`.

Array

Initialize an array of given length with default values:

```
Array(3).fill(null); // [null, null, null]
```

Classes

Unlike function declarations, class declarations are not hoisted.

```js

// A class only exists after execution reached its definition and it was evaluated.
// Accessing it beforehand leads to a ReferenceError

new Foo();

class Foo {}

```

### A class body can only contain methods, but not data properties.


Prototypes having data properties is generally considered an anti-pattern, so this just enforces a best practice.

`constructor, static methods, prototype methods`

# React

[HOC is better than mixins](https://facebook.github.io/react/docs/higher-order-components.html)

`e` is synthectic event for cross browser compatibility.

[Reducer Composition (Array)](www.example.com)
