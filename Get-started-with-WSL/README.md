# Get-started-with-WSL 
This simple guide to get started with the **Windows Subsystem for Linux**.

*Based on https://docs.microsoft.com/en-us/learn/modules/get-started-with-windows-subsystem-for-linux/*

## Enabling WSL and installing a distribution
### Enabling WSL
1. Open PowerShell as an admin
2. type the command:
    ```PowerShell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```
3. Restart computer if prompted
### Install a linux distribution
1. Start the Microsoft Store app and search for a linux distribution. Using Ubuntu (**Ubuntu 18.04 LTS**) here.
2. Select **Get** and then **Install**.
3. Select **Launch** or type the name of the distribution in **Start** menu.
4. Choose a username. ***Can be anything, it has no bearing on the windows username***.
5. Update distribution:
    ```bash
    sudo apt update -y
    sudo apt upgrade -y
    ```

## Integration between Windows and Linux file systems
* One can run linux command from windows command prompt or powershell prompt, using the ```wsl``` prefix. E.g.:
    ```bash
    wsl ls
    ```
* Running ```wsl.exe``` or ```bash.exe``` switches to a linux command line environment, using the path of the current dir (mounted on ***/mnt/c***).

    **Attention!** In case there's more than one distibution installed, the environment will be the one of the ***default*** distribution. See below to know how to change distribution.

    Type ```exit``` to exit this environment.
* One can also run windows command from linux shell. E.g.:
    ```bash
    ipcongig.exe
    ```

## Configure Visual Studio Code to work with WSL
1. Install **Remote - WSL** VSC extension

## Use multiple distributions
*ALl commands below are powershell commands.*
* Several different distribution can be installed.
* ```wslconfig /list``` (or ```wsl --list```) lists all installed distribution
* ```wsl --list --verbose``` lists installed distribution and their WSL version (1 or 2).
* To change the default distribution (i.e. set the distribution used by default!):
    ```bash
    wsl --set-default <distribution-name>
    ```
    For instance:
    ```bash
    wsl --set-default Ubuntu-18.04
    ```
* To change the WSL version (1 or 2) used by the distribution:
    ```bash
    wsl --set-version <distribution-name> <version>
    ```
    For instance:
    ```bash
    wsl --set-version Ubuntu-18.04 2
    ```
* To remove a distribution:
    ```bash
    wsl --unregister <distribution-name>
    ```

