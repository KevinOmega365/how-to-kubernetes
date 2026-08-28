# Setup

## Install

### WSL

**todo: add adding a distro**

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
