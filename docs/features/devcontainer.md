# Devcontainer

!!! summary "Configuration"

    - **Main config file:** [`devcontainer.json`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/devcontainer.json)
    - **Dependencies:** [`requirements.txt`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/requirements.txt)
    - **Dockerfile:** [`Dockerfile`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/Dockerfile)
    - **Service definition:** [`compose.yml`](https://github.com/compilerla/template-devcontainer/blob/main/compose.yml)
    - **Finalization:** [`postAttach.sh`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/postAttach.sh)

## Introduction

[VS Code](https://code.visualstudio.com/) can be used together with Docker via the
[Remote - Containers](https://code.visualstudio.com/docs/remote/containers) extension to enable a container-based development
environment.

As a remote-first, cross-platform development team, Compiler uses devcontainers to ease the onboarding
and local development process for our engineering team, and to ensure our Open Source projects are widely accessible and easily
reproducable for others.

## The image

The devcontainer's image is called `compilerla/template-devcontainer`.

### Base

The image is based on [`python:3.11`](https://hub.docker.com/_/python), to ease installation of common tooling like
[`mkdocs`](docs.md) and [`pre-commit`](pre-commit.md).

### Setup

Most setup is performed as the non-root `$USER`, with a default of `compiler`.

A home directory is created at `/home/$USER` and the working directory is set to `/home/$USER/src`.

Additional command-line tools included in the image:

- `curl`
- `git`
- `pip`
- `wget`

See the official [`python` image on DockerHub](https://hub.docker.com/_/python) for more.

### Requirements

The `.devcontainer/requirements.txt` file lists [`PyPI`](https://pypi.org/) packages installed by default into the devcontainer.

### Extensions

The `devcontainer/devcontainer.json` file lists VS Code extensions installed with the devcontainer. These include:

- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) for supercharing the `git` experience
- [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) for visualizing the `git` commit history
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) for Markdown linting and style checking directly in VS Code
- [Mermaid Markdown Syntax Highlighting](https://marketplace.visualstudio.com/items?itemName=bpruitt-goddard.mermaid-markdown-syntax-highlighting) for editing Mermaid diagrams in [documentation](docs.md)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) for good default formatting and linting of most file types
