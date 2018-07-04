It's one of the good exampe usage of the anonnymous class.

```java
Map<String, Integer> ages = new HashMap<String, Integer>(){{
    put("David", 30);
    put("John", 25);
    put("Mary", 29);
    put("Sophie", 22);
}};
```
