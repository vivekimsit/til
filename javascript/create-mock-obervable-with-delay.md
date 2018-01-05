#### Sometimes it helps during development

```js
  getContact(id) {
    return Observable.of({
      id: id,
      name: 'Foo bar',
      website: 'http://example.com',
    }).delay(3000);
  }
```
