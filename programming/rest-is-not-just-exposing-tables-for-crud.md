Core ideas [Ref](https://stackoverflow.com/a/6850287/867461)

- It can involve several separate operations on server
- REST is about manipulating resources which is ultimately mapped to CRUD operations
- REST is designed keeping in mind client knows as little as possible

Taking an example of car purchase:

- For purchasing a new car

```
POST /api/v1/purchase

// Its perfectly fine, it doesn't matter if it involves several resources
on the server side
```

- Approve a purchase

```
(PUT|PATCH "approved=true") /api/v1/purchase/:id

// Since we are consistent with the notion of Purchase as a resources
this is a fine approach too
```
