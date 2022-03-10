# Azure CLI for OpenShift


This helm chart deploys azure cli in openshift cluster as privileged root container

## Add helm repo

```shell
helm repo add pthankav https://ponson-thankavel.github.io/helm-charts
```

## Dry Run

``shell
helm upgrade azurecli pthankav/azurecli-openshift --dry-run --debug --install --namespace azurecli-ns --timeout 10m
``
  
## Deploy

``shell
helm upgrade azurecli pthankav/azurecli-openshift --debug --install --namespace azurecli-ns --timeout 10m
``

## Steps

1. Deploy the application
2. Run 'oc get pods' to find the running azurecli pod
3. Get shell access to azure cli pod 'oc exec -it pod/<azurecli pod name> -- sh'
4. login to azure using 'az login'
5. run other azure cli commands
