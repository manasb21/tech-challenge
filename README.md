
# 2-Kubernetes

This is a simple application deployment in kubernetes, it's configured to work locally with minikube and helm.

Please find the base code under [2-kubernetes](2-kubernetes)

You'll need those to verify your code deploying in minikube (of course k3s or microk8s are also perfectly ok).

You can deploy the current code and your changes with:

```
helm upgrade --install --kube-context minikube --values 2-kubernetes/helm/values.yaml kubernetes-task 2-kubernetes/helm/
```

## Questions

1. This application is currently not working properly, can you figure out why, so you can at least access the service with a port-forward?
2. Deploy 3 times the same service+deployment (3 services + 3 deployments) but each of them should show a different string:
   - Hello Freund
   - Hello Amigo
   - Hello Друг
3. Add the necessary code to expose this service to outside of the cluster. Also, when querying different endpoints it should show each of the different services you created on the previous step:
   - `http://<address>/de` should show "Hello Freund"
   - `http://<address>/es` should show "Hello Amigo"
   - `http://<address>/ua` should show "Hello Друг"

> NOTE: Each of these questions are necessary to complete the next one

You can propose all your changes on a single request.


