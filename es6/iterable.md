* There are two protocols: The iterable protocol and the iterator protocol.
* These protocols can be implemented by any object respecting some conventions.

```js
var iterator = someString[Symbol.iterator]();// string is an iterable by default
iterator + '';                               // "[object String Iterator]"
 
iterator.next();                             // { value: "h", done: false }
iterator.next();                             // { value: "i", done: false }
iterator.next();                             // { value: undefined, done: true }
```

Some built-in constructs, such as the spread operator, use the same iteration protocol under the hood:

```js
[...someString]                              // ["h", "i"]
```

We can make our own iterables like this:

```js
var myIterable = {};
myIterable[Symbol.iterator] = function* () {
    yield 1;
    yield 2;
    yield 3;
};
[...myIterable]; // [1, 2, 3]
```

Some statements and expressions expect iterables, for example the for-of loops, spread operator, yield*, and destructuring assignment:

```js
for(let value of ['a', 'b', 'c']){
    console.log(value);
}
// "a"
// "b"
// "c"

[...'abc']; // ["a", "b", "c"]

function* gen() {
  yield* ['a', 'b', 'c'];
}

gen().next(); // { value:"a", done:false }

[a, b, c] = new Set(['a', 'b', 'c']);
a // "a"
```

** A generator object is both, iterator and iterable:
