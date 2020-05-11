# Docker Run

This demolet shows how to effectively use the container using `docker run` and `alias`

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