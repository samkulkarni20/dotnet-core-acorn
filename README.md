# Github Explorer
======

The sample app uses a search form to browse GitHub repositories by name.

Check this link for more details in the official documentation by Microsoft: https://learn.microsoft.com/en-us/aspnet/core/host-and-deploy/scaling-aspnet-apps/scaling-aspnet-apps?view=aspnetcore-7.0&tabs=login-azure-cli


[_Acornfile_](.Acornfile)
```
containers: {
  web: {
    build: {
      context: "."
      dockerfile: "./Dockerfile"
    }
   env: {
      if args.dev { 
        "ASPNETCORE_ENVIRONMENT": "development"
      }
   }
    ports: publish: "80/http"
  }
}
```

## Deploy with Acorn

Make sure to [_Install Acorn_]: <https://docs.acorn.io/installation/installing> before running acorns. 

Clone this repo to get started and run below command to deploy this project

```bash
  acorn run
```

## Explaining the Acornfile


* `containers` section: describes the set of containers your Acorn app consists of

  * Note: app, db and cache are custom names of your containers
  * `app` - Our .NET7 application
    * `build`: build from Dockerfile that we created
    * `env`: environment variables, statically defined, referencing a secret or referencing an Acorn argument
    * `ports`: using the publish type, we expose the app inside the cluster but also outside of it using an auto-generated ingress resource

_Details for various parameters for your Acornfile_ : https://docs.acorn.io/reference/acornfile

## Run your Application

To start your Acorn app just run:

```bash
acorn run -n sample-app . 
```
The `-n sample-app` gives this app a specific name so that the rest of the steps can refer to it. If you omit `-n`, a random two-word name will be generated.

## Access your app

Due to the configuration `ports: publish: "8000/http"` under `containers.app`, our web app will be exposed outside of our Kubernetes cluster using the cluster's ingress controller. Checkout the running apps via

```bash
acorn apps
```

```bash
$ acorn apps
NAME        IMAGE          COMMIT         CREATED     ENDPOINTS                                          MESSAGE
sample-app   0ed9a2b95c69   114c50666ed9   3m22s ago   http://web-sample-app-98d916c5.local.oss-acorn.io   OK

```

## Development Mode

In development mode, Acorn will watch the local directory for changes and synchronize them to the running Acorn app. In general, changes to the Acornfile are directly synchronized, e.g. adding environment variables, etc. Depending on the change, the deployed containers will be recreated.

```bash
acorn dev -n sample-app
```






