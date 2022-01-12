spring-boot-chart
====================
A Helm chart for Kubernetes

Source code can be found [here](https://github.com/ManagedKube/helm-charts)

This `spring-boot-chart` Helm Chart can cover most needs for when you want to deploy your web application container to Kubernetes.  Instead of writing your own custom Helm Chart you can use this or use this as a starting point.

This chart will create these Kubernetes resources:
* Deployment
* Service
* Ingress
* Role
* Role binding
* Service Account
* Config Map

<Diagram here on what it will create you>

## Why use this chart
Instead of having to figure out and write the Kubernetes `Deployment`, `Service`, and `Ingress` yaml files which at the minimum can be over a 100 lines, you can fill in the following and this Helm chart will generate all of the other necessary items necessary for a valid Kubernetes deployment.
 ## Local Helm Testing

### Temlating out values:

Testing it out with the default values.
```
helm template --values values.yaml ./
```

Testing it out with a value from the `ci` folder:
```
helm template --values values.yaml --values ./ci/secrets-volumes-values.yaml ./
```
