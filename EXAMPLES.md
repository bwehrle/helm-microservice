
## Microservice chart

* Release name: is the service name combined with the branch the service came from (sha or name)

Deploy new httpbin microservice "staging" release
```sh
helm install httpbin-staging microservice-0.6.0.tgz --values example-httpbin-values.yaml --namespace httpbin-helm
helm status httpbin-staging --namespace httpbin-helm
```


Uninstall httpbin microservice "staging" release
```sh
helm uninstall httpbin-staging --namespace httpbin-helm
helm status httpbin-staging --namespace httpbin-helm
```