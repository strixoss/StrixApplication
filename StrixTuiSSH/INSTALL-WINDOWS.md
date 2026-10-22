# StrixTuiSSH on Windows

StrixTuiSSH can be installed natively on Windows with Windows PowerShell 5.1 or newer. Running it in Ubuntu under WSL 2 is also an option.

## Native Windows installation

### Requirements

- Windows PowerShell 5.1 or newer.
- Python 3.10 or newer, with the `venv` and `ensurepip` modules available. The installer checks for `python.exe` or the Python launcher `py.exe`.
- The Windows OpenSSH Client to connect to SSH hosts. If `ssh.exe` is not available, the installer warns you; install the OpenSSH Client optional feature in Windows to enable SSH connections.

### Install

Open PowerShell and download the installer script from the release:

```powershell
$installer = Join-Path $env:TEMP "install-strixtuissh.ps1"
Invoke-WebRequest `
  -Uri "https://github.com/strixoss/StrixApplication/releases/download/strixtuissh-v0.4.0/install.ps1" `
  -OutFile $installer
```

Review the downloaded script before running it:

```powershell
Get-Content $installer
```

Then run the installer for version `0.4.0`:

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File $installer -Version 0.4.0
```

The installer downloads the application package and its `SHA256SUMS`, verifies the package checksum, and installs StrixTuiSSH for the current user. To install another release, replace `0.4.0` with the version number available on the [GitHub Releases page](https://github.com/strixoss/StrixApplication/releases).

After installation, open a new PowerShell window and run:

```powershell
strixtuissh
```

### Uninstall

Download `install.ps1` from the release you installed, then run:

```powershell
powershell.exe -NoProfile -ExecutionPolicy Bypass -File $installer -Uninstall
```

By default, uninstalling keeps saved hosts and telemetry state. Use `-Purge` together with `-Uninstall` to remove that saved data as well.

## Alternative: install in WSL 2

To run the Linux release inside Ubuntu on Windows, open PowerShell as Administrator and install WSL 2 with Ubuntu:

```powershell
wsl --install -d Ubuntu
```

Restart Windows if prompted, launch **Ubuntu** from the Start menu, and finish its first-run setup. Then follow [the Linux installation instructions](./INSTALL-LINUX.md) in the Ubuntu terminal. Do not run the Linux shell installer directly from PowerShell or Command Prompt.
