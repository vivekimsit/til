# TIL

> Lets learn something everyday.

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

#### Null

```js
var a = null;

(!a && typeof a === "object"); // true
```

null is the only primitive value that is "falsy" but that also returns "object" from the typeof check.

#### A class body can only contain methods, but not data properties.


Prototypes having data properties is generally considered an anti-pattern, so this just enforces a best practice.

`constructor, static methods, prototype methods`

#### Rest vs Spread

spread elements 'expands' an array into its elements, and rest elements collects
multiple elements and 'condenses' into a single element.

[source (mdn)](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Spread_operator)

#### Instance methods and properties

```js

 class Bork {
    //Property initializer syntax
    instanceProperty = "bork";
    boundFunction = () => {
      return this.instanceProperty;
    }

    //Static class properties
    static staticProperty = "babelIsCool";
    static staticFunction = function() {
      return Bork.staticProperty;
    }
  }
```
[Babel plugin](https://babeljs.io/docs/plugins/transform-class-properties/)

### Function default values

```js
function foo(opts) {
  opts = Object.assign({
    pow: ''
  }, opts);
}
```

## Web performance

[Faster Font Loading with Font Events](https://jonsuh.com/blog/font-loading-with-font-events/)


### Reducers

Using combineReducers does "call all reducers", or at least all of the slice reducers it is wrapping.

[Link](https://github.com/markerikson/redux/blob/structuring-reducers-page/docs/recipes/reducers/04-UsingCombineReducers.md)

### VIM

#### Convert tabs to spaces in a file

Select visually the area to apply the changes then,

`:retab`

### Service workers

A service worker is run in a worker context: it therefore has *no DOM access*,
and *runs on a different thread* to the main JavaScript that powers your app,
so it is not blocking. It is designed to be *fully async*; as a consequence,
APIs such as synchronous XHR and localStorage can't be used inside a service worker.
