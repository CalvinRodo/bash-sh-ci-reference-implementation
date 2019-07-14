# BASH/SH CI Implementations

## Implementations

### Travis CI

We use the go language environment since it's required by shfmt, this saves us from having to install go ourselves.

## Linters - Static Code Analysis

## Error Checking

**ITSG-33 Control** *SA-11(1) Developer Security Testing*

Use ShellCheck to check your bash/sh for known issues.

https://github.com/koalaman/shellcheck

## Pretty Printers

Use `shfmt` to ensure your script is formatted using a standard format

Run shfmt from inside a docker container 

https://github.com/tmknom/shfmt

docker run --rm -v $PWD:/work tmknom/shfmt -i 2 -ci -w **/*.sh
