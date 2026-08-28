# Install

## Install WSL and Ubuntu

### WSL

1. Install WSL ```wsl --install```
    1. The installer will request to run as administrator. Expect a prompt.
    1. Reboot
1. Install Ubuntu: ```wsl --install -d Ubuntu```
    1. Enter a new Linux username when prompted (this does not need to match your Windows username).
    1. Type a secure password and confirm it. (Note: The cursor will not move or show characters while typing the password; this is standard security behavior for Linux).

#### Copy paste

``` PowerShell
wsl --install
```

``` PowerShell
wsl --install -d Ubuntu
```

#### Further reading

[Microsoft Learn on how to install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)

---

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

NB: The installer will request to run as administrator. Expect a prompt.
