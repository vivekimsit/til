
By default all the tables in the DB are in `public` schema but
its not a good practice to keep all the tables in the `public` schema.

#### Creating a names schema

```
$ CREATE SCHEMA <name>;
```

#### Check all the existing schemas in the DB

```
$ SELECT schema_name FROM information_schema.schemata;
```

#### Droping the existing schema

```
$ DROP SCHEMA <name> CASCADE;
```
