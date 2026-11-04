# StrixTuiSSH — Linux Releases

StrixTuiSSH is a terminal (TUI) SSH client for Linux, written in Python.

This repository is used **only for distributing releases**. It contains no source code and is not used for development.

## Installation

The installer requires Python 3.10 or newer with `venv` and `ensurepip`, plus
`sha256sum` and either `curl` or `wget`. It installs for the current user and
does not require root privileges.

Download the installer from the release you want and run it:

```sh
curl -fsSLO https://github.com/strixoss/StrixApplication/releases/download/strixtuissh-v0.6.0/install.sh
sh install.sh --version 0.6.0
```

To install a different version, replace `strixtuissh-v0.6.0` in the URL with
the tag of that release and change `--version 0.6.0` to its version number.
To install the latest release instead, run `sh install.sh` without `--version`.
All releases are listed here:

**https://github.com/strixoss/StrixApplication/releases**

### ARMv7 (32-bit ARM) machines

On 32-bit ARM (armv7) there are no prebuilt wheels for some dependencies
(e.g. `pycryptodomex`), so they are compiled during installation. Before
running `install.sh` for version 0.6.0, install a compiler and the Python
headers:

- Debian / Raspberry Pi OS / Ubuntu: `sudo apt install build-essential python3-dev`
- Fedora: `sudo dnf install gcc python3-devel`
- Alpine: `apk add build-base python3-dev`

Then run the installer again.

Alternative without a compiler: install `python3-pycryptodomex` from your
distribution, provided the virtual environment is created with
`--system-site-packages`.

### Review before running

`install.sh` is a shell script that runs on your machine. Read it before executing it:

```sh
less install.sh
```

### Package verification

The installer downloads the application package and its `SHA256SUMS` file,
then verifies the package checksum before installing it. `SHA256SUMS` covers
the application packages, not `install.sh`; review the installer script before
running it.

## Versioning

Release tags use the format `strixtuissh-vMAJOR.MINOR.PATCH` and follow [Semantic Versioning](https://semver.org/). While the major version is `0`, the interface and configuration may change between minor versions. Read the release notes before updating.

Pre-releases are marked as *Pre-release* on the releases page.

## Reporting issues

Issues and pull requests are **disabled** in this repository. Please report bugs and feature requests through the project's main channel: `<link to issue tracker / contact>`.

## License

See the license terms included with each release.