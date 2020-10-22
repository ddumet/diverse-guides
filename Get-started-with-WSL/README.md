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
* One can run linux command from windows command prompt, using the ```wsl``` prefix. E.g.:
```bash
wsl ls
```
* Running ```wsl.exe``` or ```bash.exe``` switches to a linux command line environment, using the path of the current dir (mounted on ***/mnt/c***).

    Type ```exit``` to exit this environment.
* One can also run windows command from linux shell. E.g.:
```bash
ipcongig.exe
```

## Configure Visual Studio Code to work with WSL
1. Install **Remote - WSL** extension

## Use multiple distributions
* Several different distribution can be installed.
* ```wslconfig /list``` (or ```wsl --list```) lists all installed distribution
* ```wsl --list --verbose``` lists installed distribution and their WSL version (1 or 2).

