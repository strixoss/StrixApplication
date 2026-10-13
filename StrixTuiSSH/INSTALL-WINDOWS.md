# StrixTuiSSH on Windows

StrixTuiSSH is currently distributed as a Linux terminal application. There is no native Windows installer. On Windows, run it in Windows Subsystem for Linux (WSL 2) with Ubuntu.

## 1. Install WSL 2 and Ubuntu

Open PowerShell as Administrator and run:

```powershell
wsl --install -d Ubuntu
```

Restart Windows if prompted, then launch **Ubuntu** from the Start menu. Complete Ubuntu's first-run setup by creating a Linux username and password.

If WSL is already installed, make sure the Ubuntu distribution uses WSL 2:

```powershell
wsl --set-version Ubuntu 2
```

## 2. Install StrixTuiSSH in Ubuntu

In the Ubuntu terminal, follow the Linux installation instructions in [the StrixTuiSSH release guide](./INSTALL-LINUX.md). The release installer is a shell script, so run it inside Ubuntu—not directly from PowerShell or Command Prompt.

For example, the release guide's commands can be run in Ubuntu as follows (replace the tag with the release you want):

```sh
curl -fsSLO https://github.com/strixoss/StrixApplication/releases/download/strixtuissh-v0.1.0/install.sh
sh install.sh
```

To verify the download before running it, use the checksum instructions in the release guide.

## 3. Start the application

Launch StrixTuiSSH from the Ubuntu terminal using the command installed by the release. The application's SSH connections use the network available to the WSL environment.

## Notes

- Install and run the application from the Ubuntu/WSL terminal; the release does not provide a native `.exe` or `.msi` installer.
- Release tags and available downloads are listed on the [GitHub Releases page](https://github.com/strixoss/StrixApplication/releases).
- See [the release guide](./INSTALL-LINUX.md) for versioning, verification, and release information.
