# Options

Add options to `pytest.ini`:

```
[pytest]
addopts = --tb=no -p no:warnings -p no:cacheprovider -vv
```

|item|description|
|----|-----------| 
| `[pytest]` | must be here for all options
| `addopts = <switches>` | options that would normally go on the command line can be placed here.  These can be overriden on the command line
| `--tb=<something>`     | traceback control.  can be one of 'auto', 'long', 'short', 'no', 'line', 'native'
| `-vv`                  | controls verbosity.  `-v` and `-vv` will show individual stages and parameter iterations

More `pytest.ini` options will be explored throughout the demolets.