Below two jsx expressions are equivalent:

```
<MyTextBox autocomplete />
```

```
<MyTextBox autocomplete={true} />
```

Later is not recommended because it matches with the object shorthand notation `{foo}` === `{foo: foo}`
