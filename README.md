# Scope

A pipeline for pulling public container images from Docker Hub Registry into the hmctspublic Azure Container Registry.

To add a new image, open a new PR and add the required setup in the azure-pipelines.yml file. 

# Example:

We want to add "alpine:3" to our repository. 

```
strategy:
  matrix:
    postgres:
      imageName: 'postgres'
      version: '11.9'
    alpine:
      imageName: alpine
      version: '3'
```

The new image will be available at hmctspublic.azurecr.io/base/alpine:3 

