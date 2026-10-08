# Quick tool check

A one-liner to check tool installation

``` PowerShell
Get-Command az, wsl, docker, kind, kubectl, helm -ErrorAction SilentlyContinue | Select-Object Name, Source
```

NB: Check the output list; it won't tell you what is missing

## Local dev requirements

* wsl
* docker
* kind
* kubectl

## Azure dev requirements

* az
* kubectl
* helm
