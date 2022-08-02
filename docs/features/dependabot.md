# Dependabot

!!! summary "Configuration"

    - **Main config file:** [`.github/dependabot.yml`](https://github.com/compilerla/template-devcontainer/blob/main/.github/dependabot.yml)

## Introduction

[Dependabot](https://docs.github.com/en/code-security/dependabot) is GitHub's service for keeping repository dependencies
up to date and staying ahead of security vulnerabilities in open source packages.

Based on the configured package ecosystems, Dependabot will send alerts to repository administrators for security-related events
in referenced packages. Dependabot will also open Pull Requests to update dependencies when fixes are published.

## Features

### GitHub Actions

Watches for updates to GitHub Actions workflow steps, e.g. [`actions/checkout`](https://github.com/actions/checkout).

Read more about [Keeping actions up to date with Dependabot](https://docs.github.com/en/code-security/dependabot/working-with-dependabot/keeping-your-actions-up-to-date-with-dependabot)
