# til
Lets learn something everyday.

# Core

The comma operator in JavaScript is interesting.
It takes two arguments, evaluates them both, and itself evaluates to the value of the right-hand argument.

```js
(1, 2)
  //=> 2

(1 + 1, 2 + 2)
  //=> 4
```

#### Scheduling Microtasks

[SO](http://stackoverflow.com/q/36870467)

#### JS is stringly typed language

`[1, true] == '1,true' === true`

# ES6

#### Map

```
 var m = {};
 var a = {id: 1},
     b = {id: 2};
 m[x] = 'foo';
 m[x] = 'bar';
 
 m[x]?
 m[y]?
```

#### WeakMap

1. WeakMap take only object as keys.
2. They don't have `size` or `clear` method.
3. They don't have iterartor over `keys`, `values` or `entries`.

#### Array

Initialize an array of given length with default values:

```
Array(3).fill(null); // [null, null, null]
```

#### Classes

Unlike function declarations, class declarations are not hoisted.

```js

// A class only exists after execution reached its definition and it was evaluated.
// Accessing it beforehand leads to a ReferenceError

new Foo();

class Foo {}

```

#### A class body can only contain methods, but not data properties.


Prototypes having data properties is generally considered an anti-pattern, so this just enforces a best practice.

`constructor, static methods, prototype methods`

#### Rest vs Spread

spread elements 'expands' an array into its elements, and rest elements collects
multiple elements and 'condenses' into a single element.

[source (mdn)](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Spread_operator)

#### Symbols

`Symbol() !=== Symbol()`

#### async, await

https://developers.google.com/web/fundamentals/getting-started/primers/async-functions

# React

[HOC is better than mixins](https://facebook.github.io/react/docs/higher-order-components.html)

`e` is synthectic event for cross browser compatibility.

[Reducer Composition (Array)](www.example.com)
