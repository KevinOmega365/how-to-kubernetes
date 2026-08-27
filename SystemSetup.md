# Setup

## Instal

### WSL

1. Install WSL via Terminal
    1. Right-click the Windows Start Menu and select Terminal (Admin) or PowerShell (Admin).
    1. Type the following command and press Enter: ```wsl --install``` Note: This command automatically enables the required virtualization features, downloads the latest Linux kernel, and installs Ubuntu as the default Linux distribution.Step
1. Restart Your Computer
    1. Wait for the terminal to show that the installation is complete.
    1. Restart your machine to finalize the feature activation.
1. Configure Your Linux User AccountAfter rebooting, a Linux terminal window (Ubuntu) will open automatically.
    1. Enter a new UNIX username when prompted (this does not need to match your Windows username).
    1. Type a secure password and confirm it. (Note: The cursor will not move or show characters while typing the password; this is standard security behavior for Linux).

### kubectl

``` PowerShell
winget install -e --id Kubernetes.kubectl
```

### kind

``` PowerShell
winget install -e --id Kubernetes.kind
```

### Helm

``` PowerShell
winget install -e --id Helm.Helm
```

### Docker Desktop

``` PowerShell
winget install -e --id Docker.DockerDesktop
```

## Test

### 1. Check WSL

```powershell
wsl --status
```

**You should see:** information about WSL, including its default version and kernel.

You can also try:

```powershell
wsl --list --verbose
```

This should show your installed WSL distributions.

---

### 2. Check Docker

```powershell
docker --version
```

**You should see something like:**

```text
Docker version 28.x.x, build ...
```

Then try:

```powershell
docker info
```

This is a slightly more useful test because it checks whether the Docker engine is actually running.

---

### 3. Check kubectl

```powershell
kubectl version --client
```

**You should see:** the installed `kubectl` client version.

Then:

```powershell
kubectl config get-contexts
```

This introduces the user to `kubectl` configuration without requiring a Kubernetes cluster to be running.

---

### 4. Check kind

```powershell
kind version
```

**You should see something like:**

```text
kind v0.29.0 go1.24.x windows/amd64
```

Then:

```powershell
kind get clusters
```

If they haven't created a cluster yet, an empty result is perfectly fine. The important thing is that the command runs.

---

### 5. Check Helm

```powershell
helm version
```

**You should see something like:**

```text
version.BuildInfo{Version:"v3.x.x", ...}
```

Then:

```powershell
helm list
```

Again, an empty result is fine if they haven't installed any Helm releases yet.

---

### A nice progression for beginners

I'd actually give the user these **in this order**, because it gradually introduces useful command-line concepts:

```text
wsl --status
wsl --list --verbose

docker --version
docker info

kubectl version --client
kubectl config get-contexts

kind version
kind get clusters

helm version
helm list
```
