# tests

Add multiple tests to a single test file.  this is useful for running a series of related tasks like setup or teardown.

- each test is an individual yaml block, so must be separated by `---`
- `test_name: <test_name>` required for each test block and must be unique
- `stages: ` required for each test
- `- name: <stage_name>` required for each stage in the test.  Must be unique for the test

## Examples:

Run all test blocks in the file:
```
tavern-ci test_get.tavern.yaml
```

Run only one test block in the file:
```
tavern-ci test_get.tavern.yaml::get_foo
```

