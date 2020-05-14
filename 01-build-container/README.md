# Build Docker Container

If python 3 is not already installed the test box, it can be easier to just build a docker container instead of getting dev or build box configured.

## Requirements/Suggestions

The following is needed to build and run the container:
  - `docker`
  - your user account in the `docker` group.  This helps not use `root` for anything
  - `Dockerfile` that you create.   You can use the included one for a starting point

## Build

1. Build it: `docker build -t tavern-ci:latest .`
2. Use it: `tavern-ci --help`

