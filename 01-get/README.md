# Get


Check is website is up and returns `200`:

```
tavern-ci test_get.tavern.yaml
```

Some options to make output more sane:

```
tavern-ci test_get.tavern.yaml -p no:warnings -p no:cacheprovider
```

|item|description|
|----|-----------| 
| `-p` | plugin management.  stack with additional `-p <something>`
| `no:<plugin>` | disable this plugin
