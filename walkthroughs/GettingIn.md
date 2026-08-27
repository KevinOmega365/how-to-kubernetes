# getting in

Log into Azure CLI and AKS (Azure Kubernetes Service)

``` PowerShell
az login
```

``` PowerShell
az aks get-credentials `
  --resource-group df-rg-aks-swedencentral-prototype `
  --name df-cluster-swedencentral-prototype `
  --overwrite-existing
```

``` PowerShell
kubelogin convert-kubeconfig -l azurecli
```

``` PowerShell
kubectl auth whoami
```

``` PowerShell
kubectl get ns
```

``` PowerShell
kubectl get svc -A
```

``` PowerShell
kubectl get pods -n df-common -w
```
