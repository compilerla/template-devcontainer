# Reference the pre-built image

!!! summary "Configuration"

    - **Workflow file:** [`.github/workflows/publish-devcontainer.yml`](https://github.com/compilerla/template-devcontainer/blob/main/.github/workflows/publish-devcontainer.yml)
    - **GHCR Packages:** [`compilerla/template-devcontainer`](https://github.com/compilerla/template-devcontainer/pkgs/container/template-devcontainer)
    - **Minimal devcontainer.json:** [`devcontainer.pre-built.json`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/devcontainer.pre-built.json)

`template-devcontainer` maintains a [GitHub Actions](https://github.com/features/actions) workflow that publishes Docker
images to [GitHub Container Registry (GHCR)](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry).

The publish is triggered for every push to the `main` branch, and multiple image tags are created:

- `main` uses the default Python version of 3.11
- `main_3.10` uses Python 3.10
- `main_3.12` uses Python 3.12

There are also corresponding tags for the git SHA of the commit on `main` that triggered the build
(e.g. `sha`, `sha_3.10`, and `sha_3.12`).

This makes the pre-built devcontainer image available for use in other projects, potentially decreasing startup and onboarding
time even further.

## From a `devcontainer.json` configuration

The pre-built devcontainer image can be used as the basis for another `devcontainer.json` configuration, similar to how one
might reference any other image on Docker Hub or GHCR:

```json
{
  "name": "compilerla/template-devcontainer-pre-built",
  "image": "ghcr.io/compilerla/template-devcontainer:main",
  // initialize pre-commit hooks on attach (assumes .pre-commit-config.yaml)
  "postAttachCommand": "pre-commit install --overwrite"
  // other settings
}
```

Our [`devcontainer.pre-built.json`](https://github.com/compilerla/template-devcontainer/blob/main/.devcontainer/devcontainer.pre-built.json)
shows a minimal example to get a devcontainer running with the same configuration as the normal `devcontainer.json`, using the
pre-built image.

See the full [`devcontainer.json` Reference](https://code.visualstudio.com/docs/remote/devcontainerjson-reference) for details.

## Using Docker Compose

In a `docker-compose.yml` or `compose.yml` file, you can reference the GHCR image directly in a service definition:

```yaml
services:
  myservice:
    image: ghcr.io/compilerla/template-devcontainer:main
    volume: ./:/home/compiler/src
```

Note the `volume` entry mapping the current directory (with the `compose.yml` file) into the [devcontainer working directory](../features/devcontainer.md#setup).

And then starting the service with:

```shell
docker compose up myservice
```

This is perhaps a less useful approach, with the default `CMD` and `ENTRYPOINT` set in such a way as to make the container
essentially hang (useful when attaching from VS Code).
