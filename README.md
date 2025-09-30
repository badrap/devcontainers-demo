# devcontainers-demo

This is a repository demonstrating devcontainer based development with Vue 3 and Vite. It has been bootstrapped by following Vue's [Quick Start page](https://vuejs.org/guide/quick-start.html), with the following modifications:

- Devcontainer configuration in [.devcontainer](./.devcontainer) subdirectory. For more information about devcontainers, see [Developing inside a Container](https://code.visualstudio.com/docs/devcontainers/containers).
- A custom [`Dockerfile`](.devcontainer/Dockerfile). Another option is to use [pre-built devcontainer images](https://github.com/devcontainers/images).
- The local profile directory is persisted between container rebuilds.
- Local Chromium installed inside the container for end-to-end testing.
- `.npmrc` file that disables install scripts with `ignore-scripts=true`.

## Recommended Development Environment Setup

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [VSCode](https://code.visualstudio.com/)
- [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Type-Check, Compile and Minify for Production

```sh
npm run build
```

### Run Unit Tests with [Vitest](https://vitest.dev/)

```sh
npm run test:unit
```

### Run End-to-End Tests with [Playwright](https://playwright.dev)

```sh
# Runs the end-to-end tests
npm run test:e2e
# Runs the tests of a specific file
npm run test:e2e -- tests/example.spec.ts
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```
