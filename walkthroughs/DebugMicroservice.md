# Debug Microservice

## Source

<https://metalbear.com/mirrord/docs/guides/language-guides/how-to-debug-a-dotnet-microservice>

## Steps

### 0. Make sure you have the .NET 10.0 SDK (or higher) installed locally

``` terminal
dotnet --version
```

<https://dotnet.microsoft.com/download>

``` terminal
dotnet run --project src
```

Open Docker Desktop

``` terminal
kind create cluster --name mirrord-debug-example
```

``` terminal
docker build -t dotnet-guestbook:local .
```

``` terminal
kind load docker-image dotnet-guestbook:local --name mirrord-debug-example
```

``` terminal
kubectl create -f ./kube
```

``` terminal
mirrord exec -f mirrord.json -- dotnet run --project src
```

