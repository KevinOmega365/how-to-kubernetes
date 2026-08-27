# Hello Kebernetes -- in Docker (kind)

## Start Docker

``` PowerShell
Start-Process "C:\Program Files\Docker\Docker\Docker Desktop.exe"
```

Create a cluster

``` PowerShell
kind create cluster --name dataflow-poc
```

## Create a pod

Create a yaml file (on your desktop): podmanifest.yaml

``` YAML
apiVersion: v1
kind: Pod
metadata:
  name: hello-dataflow-pod
  labels:
    app.kubernetes.io/name: hello-dataflow
    app.kubernetes.io/part-of: dataflow
    dataflow.io/resource-scope: platform
spec:
  containers:
    - name: web
      image: docker.io/nginxinc/nginx-unprivileged:1.27-alpine
      ports:
        - containerPort: 8080
          name: http

```

Note: the path to the YAML may be different

``` PowerShell
kubectl apply -f ~\Desktop\podmanifest.yaml
```

## List the pod

``` PowerShell
kubectl get pods
```

## Describe the pod

``` PowerShell
kubectl describe pod hello-dataflow-pod
```

## Port foward to the nginx pod

``` PowerShell
kubectl port-forward pod/hello-dataflow-pod 8080:8080
```

Open <http://localhost:8080>

## Look at the logs

``` PowerShell
kubectl logs hello-dataflow-pod
```

## Delete the pod

``` PowerShell
kubectl delete -f ~\Desktop\podmanifest.yaml
```

## View the clusters

``` PowerShell
kind get clusters
```

## Delete the cluster

``` PowerShell
kind delete cluster --name dataflow-poc
```
