---
id: routing
title: Routing Between Micro Apps
---

While in most cases you only need to work within your Micro App you will also come across a situation where you will need to run all your micro apps and navigate between them to test end to end flows.

## Routing between Micro Apps on local development enviroment

Nx comes with its own internal proxy setup.
Have a look at the proxy.conf file located in the root of the application.
As a thumbrule on local we would run each micro app on a different port and use the proxy file to map the the different microapps to the respective URL patterns

You can define on which ports each of your micro app should run by defining the port option in the workspace.json file as follows.

```
"serve": {
          "executor": "@nrwl/web:dev-server",
          "options": {
            "buildTarget": "react-app:build",
            "port": 4200
          },

```

An example of a path in the proxy.conf would look something like this

```
  "/catalog/**/*": {
    "target": "http://localhost:4201",
    "secure": false
  },
  "/account": {
    "target": "http://localhost:4203",
    "secure": false
```

## Setting up Routing on Kubernetes

To setup app level routing in your kubernetes Ingress template file add the relevant host information as follows:

```
apiVersion: networking.k8s.io/v1beta1
kind: Ingress
metadata:
  name: <appName>
spec:
  tls:
    - hosts:
        - <site.com>
      secretName: genesis-tls
  rules:
    - host: <site.com>
      http:
        paths:
        - path: /<appPath>
          backend:
            serviceName: spark-web-account
            servicePort: 80

```
