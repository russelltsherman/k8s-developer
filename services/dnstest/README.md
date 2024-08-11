# DNS Test

verify correct function of integrating host dns resolver with kubernetes cluster

create cluster

```sh
bin/cluster create
```

install dns test resources

```sh
kubectl apply --filename=services/dnstest/dnstest.yaml
```

verify ns lookups within kubernetes

```sh
PROFILE=$(basename $(git rev-parse --show-toplevel))
nslookup hello-john.lo $(minikube ip --profile=$PROFILE)
nslookup hello-jane.lo $(minikube ip --profile=$PROFILE)
```

verify dns resolution from host

```sh
curl http://hello-john.lo
curl http://hello-jane.lo
```
