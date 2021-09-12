---
id: home
title: Welcome
---

## Genesis

This project is a seed for anyone looking to build a microfrontend / micro app architecture using [Nx](https://nx.dev)

To fully understand how NX works please read up at [Nx](https://nx.dev)

### Clone the Repo

Clone the app using this url

```
 git clone https://pscode.lioncloud.net/psinnersource/xt/micro-frontend/genesis.git
```

Generate an access token and use it in the place of your password.

### Install dependencies

At root of your folder, to make sure all your dependencies are installed.

```
npm install
or
yarn install
```

### Install NX

Installing NX globally will make things much easier

```
npm install -g nx
or
yarn global add nx
```

### Updating the workspace

To update workspace, use this command to update all your dependencies.

```
nx migrate latest
```

Running the migration, use this command so that the repo can match all the update dependencies.

```
nx migrate --run-migrations
```

To fully understand how NX updating works please read up at [Nx Update](https://nx.dev/latest/react/core-concepts/updating-nx)
