---
id: dev-server
title: Running ESBuild Dev Server
---

## Running dev server using latest ES Builds

Dev servers running ES Build load and run 1000x faster than the dev servers running via the default webpack.

The demo `react-app` uses vite-js to run the dev builds. and the `node-app` uses esbuild.

To Run the React App using vite run `nx vite <app-name>` eg: `yarn nx vite react-app`.
This would start off the app using Vite-js.
To convert any app to run via vite add the following command to the workspace.json file.

```
"vite":{
  "builder": "@nrwl/workspace:run-commands",
  "options": {
    "command": "cd apps/react-app && vite"
  }
```

The `node-app` runs using ESBuild, and you can run it using the following command `yarn nx esbuild node-app`
This is made possible by adding the following command to the workspace.json file.

```
"esbuild": {
  "executor": "@nrwl/workspace:run-commands",
  "options": {
    "command": "cd apps/node-app && esbuild ./src/main.js --bundle --outfile=main.js --platform=node && node main"
  }
}

```
