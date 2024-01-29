# Helm Repo


## Installation

### Add Helm repository

```bash
helm repo add bwehrle-ms https://bwehrle.github.io/helm-microservice/
helm repo bwehrle-ms
```

### Configure the chart

The following items can be set via `--set` flag during installation or configured by editing the `values.yaml` directly (need to download the chart first).

#### Configure the way how to expose the microservice service:

- **Ingress**: The ingress controller must be installed in the Kubernetes cluster.
- **ClusterIP**: Exposes the service on a cluster-internal IP. Choosing this value makes the service only reachable from within the cluster.
- **NodePort**: Exposes the service on each Node’s IP at a static port (the NodePort). You’ll be able to contact the NodePort service, from outside the cluster, by requesting `NodeIP:NodePort`.
- **LoadBalancer**: Exposes the service externally using a cloud provider’s load balancer.

#### Configurations

For other configurations, please see the [values.yaml](values.yaml) file. This file lists the configurable parameters of the microservice chart and the default values.

### Install the chart

Install the microservice helm chart with a release name `my-release`:

```bash
helm install my-release bwehrle-ms/microservice
```

## Uninstallation

To uninstall/delete the `my-release` deployment:

```bash
helm uninstall my-release
```

## Contributing

Feel free to contribute by making a [pull request](https://github.com/cetic/helm-microservice/pull/new/master).

Please read the official [Contribution Guide](https://github.com/helm/charts/blob/master/CONTRIBUTING.md) from Helm for more information on how you can contribute to this Chart.

## License

[Apache License 2.0](/LICENSE)
