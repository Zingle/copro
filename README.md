copro MySQL DB dump tools
=========================

Install
-------
```sh
sudo -H npm install -g copro
```

Tools
-----

### ddlt - DDL transformer

Transform MySQL DDL from STDIN.

#### Examples

##### filter a schema

```sh
# filter out DDL for `foo-data` schema
cat dump.sql | ddlt --schema foo-data --skip
```

##### filter a relation

```sh
# filter out DDL for `foo-data.foo` relation
cat dump.sql | ddlt --schema foo-data --relation foo --skip
```

##### multiple filters

```sh
# filter out DDL for `foo` schema and `bar.baz` relation
cat dump.sql | ddlt --schema foo --skip --schema bar --relation baz --skip
```
