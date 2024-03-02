# Windows
To use [Labs4grabs.io](http://labs4grabs.io/){target=_blank} on Windows, you have two options.

- Enable WSL2 and install tools like kubectl and openssh-client on the subsystem.
- Install kubectl and openssh-client directly on Windows using PowerShell.

## Powershell
1. Follow [this](https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/){target=_blank} guide to install `kubectl` on Windows.

2. Follow [this](https://learn.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse?tabs=powershell){target=_blank} guide to install `openssh-client` on Windows.

## WSL2
1. Open Powershell.

2. Run `wsl --install` command which will install the Linux subsystem.

3. Follow [this](https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/){target=_blank} guide to install `kubectl`.

4. To install `openssh-client` in your WSL2 environment run the following:
    ```
    sudo apt update
    sudo apt install openssh-client
    ```

!!! info "Download directories"
    If you are using WSL2, the directory for your downloads from the Labs4grabs Slack workspace is located at `/mnt/c/Users/<your_username>/Downloads`. Therefore, you would use the command below to get the list of pods:
    ```
    kubectl --kubeconfig /mnt/c/Users/<your_username>/Downloads/kubeconfig.yaml get po -A
    ```
