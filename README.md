# scaler
Auto Scale the replicas of deployment at peak traffic hours.

## Getting Started
You’ll need a Kubernetes cluster to run against. You can use [KIND](https://sigs.k8s.io/kind) to get a local cluster for testing, or run against a remote cluster.
**Note:** Your controller will automatically use the current context in your kubeconfig file (i.e. whatever cluster `kubectl cluster-info` shows).

### Running on the cluster
1. Deploy the operator

```sh
kubectl apply -f deployment/manifests.yaml
```

2. Build and push your image to the location specified by `IMG`:

```sh
make docker-build docker-push IMG=<some-registry>/scaler:tag
```

3. Deploy the custom resource:

```sh
kubectl apply -f config/samples/api_v1alpha1_scaler.yaml
```



