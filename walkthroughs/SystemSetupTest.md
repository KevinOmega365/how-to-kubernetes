# Test

## 1. Check WSL

```powershell
wsl --status
```

**You should see:** information about WSL, including its default version and kernel.

## 2. Check Docker

```powershell
docker --version
```

**You should see something like:**

```text
Docker version 28.x.x, build ...
```

## 3. Check kubectl

```powershell
kubectl version --client
```

**You should see:** the installed `kubectl` client version.

## 4. Check kind

```powershell
kind version
```

**You should see something like:**

```text
kind v0.29.0 go1.24.x windows/amd64
```

## 5. Check Helm

```powershell
helm version
```

**You should see something like:**

```text
version.BuildInfo{Version:"v3.x.x", ...}
```
