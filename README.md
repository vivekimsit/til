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
