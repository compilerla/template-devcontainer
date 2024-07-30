# Documentation

!!! summary "Configuration"

    - **Main config file:** [`mkdocs.yml`](https://github.com/compilerla/template-devcontainer/blob/main/mkdocs.yml)
    - **Additional dependencies:** [`docs/requirements.txt`](https://github.com/compilerla/template-devcontainer/blob/main/docs/requirements.txt)
    - **Installation:** [`Dockerfile`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/Dockerfile)
    - **Service definition:** [`compose.yml`](https://github.com/compilerla/template-devcontainer/blob/main/compose.yml)

## Introduction

The devcontainer includes a system for building project documentation, useful for developing and publishing a full-featured
documentation website, either as a standalone entity or as part of a software library/project.

Documenation is written in plaintext files using the popular [Markdown syntax](https://www.markdownguide.org/basic-syntax/).
Besides being widely supported and straightfowrad to edit in a variety of platforms, documentation written as Markdown is
easily versioned by systems like `git`.

The Python-based [`mkdocs`](https://www.mkdocs.org/) tool builds Markdown documentation files into a website structure.

Themeing and additional documentation content functionality are provided by the
[`mkdocs-material`](https://squidfunk.github.io/mkdocs-material/) extension.

## Features

- Complete color themes for both light and dark modes
- Google Analytics support (with a `G-xxxxxxxxxx` configuration)
- Site search
- Icons from [`FontAwesome`](https://fontawesome.com/)
- [Diagram support via Mermaid.js](https://squidfunk.github.io/mkdocs-material/reference/diagrams/)
- Better site navigation with [`awesome-pages`](https://github.com/lukasgeiter/mkdocs-awesome-pages-plugin/)
- Redirect old URLs when content moves around with [`redirects`](https://github.com/mkdocs/mkdocs-redirects)

See the [`mkdocs-material` Reference](https://squidfunk.github.io/mkdocs-material/reference/) for more supported features.
