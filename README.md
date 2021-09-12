# Genesis

This project is a seed for anyone looking to build a microfrontend / micro app architecture using [Nx](https://nx.dev).

To fully understand how NX works please read up at [Nx](https://nx.dev)

## Quick Start

- Install NX CLI Globally
  `yarn global add nx`

- Install the VS Code [Nx Console](https://marketplace.visualstudio.com/items?itemName=nrwl.angular-console) extension.

## Install dependencies

`yarn install`

## Documentation

- To see detailed documentation:
  `nx run docs:serve`

## Create micro-applications

- React application with webpack 5 configuration `nx generate @nrwl/react:application <application name>`

- React application with ViteJs configuration `nx g @wanews/nx-vite:react <application name>`

## Run Micro-Apps

`nx run <application name>:serve`

---

## Create shared utilities and components

- Create react component in shared library `nx generate @nrwl/react:component --name=<component name> --project=ui-kit`
- Create share utility `nx generate @nrwl/workspace:library --name=<shared-util-name>`

## StoryBook

Genesis is pre-configured to use story book with shared components:

- To run StoryBook `nx run ui-kit:storybook`

- To create story file for components `nx generate @nrwl/react:stories --project=ui-kit`

## Nx Cloud

### Computation Memoization in the Cloud

Nx Cloud pairs with Nx in order to enable you to build and test code more rapidly, by up to 10 times. Even teams that are new to Nx can connect to Nx Cloud and start saving time instantly.

Teams using Nx gain the advantage of building full-stack applications with their preferred framework alongside Nx’s advanced code generation and project dependency graph, plus a unified experience for both frontend and backend developers.

Visit [Nx Cloud](https://nx.app/) to learn more.


