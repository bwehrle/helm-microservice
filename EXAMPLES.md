
## Microservice chart

* Release name: is the service name combined with the branch the service came from (sha or name)

Deploy new httpbin microservice "staging" release
```sh
# Build helm chart locally
helm package charts/helm-microservice
helm install httpbin-r1 microservice-0.6.3.tgz --values example-httpbin-values.yaml --namespace httpbin
helm status httpbin-r1 --namespace httpbin
```


Uninstall httpbin microservice "staging" release
```sh
helm uninstall httpbin-r1 --namespace httpbin-helm
helm status httpbin-r1 --namespace httpbin-helm
```