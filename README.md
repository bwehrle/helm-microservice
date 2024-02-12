# A Helm Chart for DRY microservice deployments


## Introduction

This helm chart deploys a microservice for demonstration purposes with use with Ivro and Istio.
It creates:
* VirtualServiceBase
* VirtualServiceHttpRoute
* Ingress Gateway
* Service
* Deployment

## Prerequisites

- Kubernetes cluster 1.10+
- Helm 3.0.0+
- PV provisioner support in the underlying infrastructure.
- Istio
- Ivro

## Installation

### Add Helm repository

```bash
helm repo add bwehrle-ms https://bwehrle.github.io/helm-microservice/
helm repo update
```

### Configure the chart

The following items can be set via `--set` flag during installation or configured by editing the `values.yaml` directly (need to download the chart first).

#### Configurations

For other configurations, please see the [example values](example-httpbin-values.yaml) file. This file lists the configurable parameters of the microservice chart and the default values.

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
