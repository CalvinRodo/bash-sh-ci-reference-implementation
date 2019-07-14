# BASH/SH CI Implementations

## Implementations

### Travis CI

 [![Build Status](https://travis-ci.com/CalvinRodo/bash-sh-ci-reference-implementation.svg?branch=master)](https://travis-ci.com/CalvinRodo/bash-sh-ci-reference-implementation)


We use the go language environment since it's required by shfmt, this saves us from having to install go ourselves.

## Linters - Static Code Analysis

Linters or Static Code Analyzers will check the programs source code for bugs, errors, and formatting issues. 

Static Code Analysis Satisfies the ITSG33 Control *SA-11(1) Static Code Analysis*

### Error Checking

Use `ShellCheck` to check your bash/sh for known issues.

**Link to tool:** https://github.com/koalaman/shellcheck

#### Command to Run
>To simplify installation of this tool we are running it from inside a docker container

`docker run --rm -v "$PWD:/mnt" koalaman/shellcheck:stable script-to-test.sh`

### Pretty Printers

Use `shfmt` to ensure your script is formatted using a standard format. We are using the [Google Shell Style Guide](https://google.github.io/styleguide/shell.xml) to format our scripts.

**Link to tool:** https://github.com/mvdan/sh

#### Command to run
> Unfortunately we cannot run shfmt from within a docker container as the diff functionality currently doesn't work  

`shfmt -d -i 2 -ci -w script-to-test.sh`
