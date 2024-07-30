# template-devcontainer Docs

## Introduction

This is the documentation site for [`compilerla/template-devcontainer`](https://github.com/compilerla/template-devcontainer).

`template-devcontainer` is a [template repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository)
with a minimal [VS Code devcontainer](https://code.visualstudio.com/docs/remote/containers) setup.

`template-devcontainer` can be used as the basis for another language-specific devcontainer,
or as a quick ready-made Linux development environment.

Docs are built using [`mkdocs`](https://www.mkdocs.org/). This site is built using [`mkdocs-material`](https://squidfunk.github.io/mkdocs-material/).

## Use this template

[Generate a new repository from the template](https://github.com/compilerla/template-devcontainer/generate){.md-button}

## Why?

In no particular order, here are some reasons Compiler likes to use devcontainers as part of our software engineering workflow:

_Read more in our blog post: [How to support a platform-agnostic engineering team with VS Code Dev Containers](https://compiler.la/blog/2024/devcontainer-platform-agnostic-team)_.

| Reason                     | More                                                                                                                                                                                                                                                                                                                           |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Cross-platform**         | With only VS Code and Docker as dependencies, devcontainers allow developers on Linux, Mac, and Windows to work in a consistent environment, no matter the project's stack                                                                                                                                                     |
| **Easily extendable**      | The VS Code community maintains a [library of extensions](https://marketplace.visualstudio.com/VSCode) to add features and functionality to the development environment; individual personalizations can be made via [dotfiles](https://code.visualstudio.com/docs/remote/containers#_personalizing-with-dotfile-repositories) |
| **Enforce best practices** | Baking linters, `pre-commit` checks, test runners, and more into the devcontainer ensures the team's best practices are no-brainer always-on features of the development workflow                                                                                                                                              |
| **Rapid onboarding**       | By minimizing the steps from `git clone` to getting tests to pass or the app running locally, devcontainers make it easier to onboard as a new developer and spend time contributing instead of wallowing in environment setup                                                                                                 |
| **Unified code style**     | With common editor settings like code formatting on save, standard indentation characters and spacing, consistent line endings, and more, the team never has to worry about what the code looks like or accidentally committing BOMs                                                                                           |

## Prior art

This template was informed by our work on recent projects as a remote-first, cross-platform development team.

Some of our recent work built on the devcontainer pattern includes:

- [`cal-itp/benefits`](https://github.com/cal-itp/benefits) (Python/Django web app)
- [`cal-itp/eligibility-api`](https://github.com/cal-itp/eligibility-api) (Python API library)
- [`cal-itp/eligibility-server`](https://github.com/cal-itp/eligibility-server) (Python/Flask API server)
- [`cal-itp/hashfields`](https://github.com/cal-itp/hashfields) (Python CLI tool)
- [`cal-itp/mobility-marketplace`](https://github.com/cal-itp/mobility-marketplace) (Jekyll static site)
- [`compilerla/compiler.la`](https://github.com/compilerla/compiler.la) (Jekyll static site)
- [`compilerla/conventional-pre-commit`](https://github.com/compilerla/conventional-pre-commit) (Python pre-commit hook)
