Fail safe
---

```
public int size(File file) {
  if (!file.exists()) {
    return 0;
  }
  return file.length();
}
```

Fail fast
---

```
public int size(File file) {
  if (!file.exists()) {
    throw new IllegalArgumentException(
      "There is no such file; I can't get its length."
    );
  }
  return file.length();
}
```

If the method returns zero, it's not obvious whether the
file exists and its size is actually zero or if its name
is wrong and it is just not found. 

#### Takeaway

Software designed with the Fail Fast approach in mind
will crash frequently at the beginning but will improve
its stability with every fix and eventually become very
stable and robust.
