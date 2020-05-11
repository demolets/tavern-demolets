# Docker Run

This demolet shows how to effectively use the container using `docker run` and `alias`.

Probably the most porable and secure way to pass secrets to the tests is to use environment variables.  The below `alias` command will pass any environment variable starting with `CI_` to the container.  Some common variables:

```
CI_HOSTFQDN
CI_LOGIN
CI_PASSWORD
CI_TOKEN
```

The above examples will be used in later demolets.

## Alias it

Stick this in your `.bashrc` or similar:

```
alias tavern-ci="                       \
  docker run                            \
    --rm                                \
    -it                                 \
    --user=$(id -u):$(id -g)            \
    -v "'${PWD}'":/data                 \
    --env-file <(env | grep -P '^CI_' ) \
    -e PYTHONPATH=/data                 \
    tavern-ci:latest                    \
    tavern-ci                           \
"
```

## Source it

`source ~/.bashrc`

## Use it

`tavern-ci test_example.tavern.yaml -p no:warnings -vv`