
```js
function sayMyName(name) {
  alert(`Hello ${name}`);
}
```
VS

```js
const sayMyName = (name) => {alert(`Hello ${name}!`)}
```

> The benefit to using a named function is that if you have a stack trace,
which means if you have an error and you want to figure out,
where did this go wrong, sometimes a line number as to where it happened
isn’t very helpful, so you need to know actually the name of the function
that it got called in.

[More](http://wesbos.com/arrow-functions/)
