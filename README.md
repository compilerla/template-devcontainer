# template-devcontainer

A [template repository][template-repo] with a minimal [VS Code devcontainer][devcontainer] setup.

The base Docker image for the devconatiner is `python:3.10` and includes support for common dev tooling like `git`, `curl`,
`pip`, and `pre-commit`.

The [`pre-commit` configuration][pre-commit-config] includes a number of useful [`pre-commit-hooks`][pre-commit-hooks] as well
as Compiler's [`conventional-pre-commit`][conventional-pre-commit] hook.

## Usage

### Create a new repository

[Create a new repository from this template][generate].

### Run the devcontainer

With the `Remote - Containers` extension enabled, open the folder containing this repository inside VS Code.

You should receive a prompt in the VS Code window; click `Reopen in Container` to run the development environment inside the devcontainer.

If you do not receive a prompt, or when you feel like starting from a fresh environment:

1. `Ctrl/Cmd+Shift+P` to bring up the command palette in VS Code
1. Type `Remote-Containers` to filter the commands
1. Select `Rebuild and Reopen in Container` to completely rebuild the devcontainer
1. Select `Reopen in Container` to reopen the most recent devcontainer build

## License

[Apache 2.0](LICENSE)

[conventional-pre-commit]: https://github.com/compilerla/conventional-pre-commit
[devcontainer]: https://code.visualstudio.com/docs/remote/containers
[generate]: https://github.com/compilerla/template-devcontainer/generate
[pre-commit-config]: .pre-commit-config.yaml
[pre-commit-hooks]: https://github.com/pre-commit/pre-commit-hooks
[template-repo]: https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository
