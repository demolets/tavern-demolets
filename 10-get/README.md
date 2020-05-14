# Get


Check if website is up and returns `200`.  The included tests are:
  - just GET
  - GET with basic auth
  - GET with custom headers

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
