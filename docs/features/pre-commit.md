# pre-commit

!!! summary "Configuration"

    - **Main config file:** [`.pre-commit-config.yaml`](https://github.com/compilerla/template-devcontainer/blob/main/.pre-commit-config.yaml)
    - **Initialization:** [`Dockerfile`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/Dockerfile)
    - **Finalization:** [`postAttach.sh`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/postAttach.sh)

## Introduction

[`pre-commit`](https://pre-commit.com/) is a Python framework for running "hooks" during various points in the `git commit`
workflow.

`pre-commit` hooks do things like enforce commit message formatting and check and automatically clean up file formatting.

Integrating these checks with the `git commit` workflow ensures every commit follows team conventions and reduces the chance
for simple syntax errors and other hidden bugs.

## Features

### Conventional Commits

Compiler follows the [Conventional Commits](https://www.conventionalcommits.org/) specification for writing commit messages.

[`compilerla/conventional-pre-commit`](https://github.com/compilerla/conventional-pre-commit) is a `pre-commit` hook that
enforces this convention for every commit.

### Markdownlint

[`markdownlint`](https://github.com/DavidAnson/markdownlint) is a static analysis tool (linter) for Markdown documents.

The related [`markdownlint-cli`](https://github.com/igorshubovych/markdownlint-cli#use-with-pre-commit) tool can be used as
a `pre-commit` hook.

### Pre-Commit Hooks

[`pre-commit-hooks`](https://github.com/pre-commit/pre-commit-hooks) is a collection of useful hooks maintained by the
`pre-commit` team.
