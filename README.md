# TIL

> Lets learn something everyday.

## ES6

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

#### Nodejs compatibility

`node --v8-options | grep "in progress"`

[More here](https://nodejs.org/en/docs/es6/)


## Web performance

[Faster Font Loading with Font Events](https://jonsuh.com/blog/font-loading-with-font-events/)

## Git

### Merge

#### Undo Merge

`git merge --abort`

[SO](http://stackoverflow.com/a/18693059)

## Node

#### Passing ENV variabels to node

`USER_ID=239482 USER_KEY=foobar node app.js`
