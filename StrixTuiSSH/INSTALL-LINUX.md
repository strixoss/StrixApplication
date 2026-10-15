# StrixTuiSSH — Linux Releases

StrixTuiSSH is a terminal (TUI) SSH client for Linux, written in Python.

This repository is used **only for distributing releases**. It contains no source code and is not used for development.

## Installation

The installer requires Python 3.10 or newer with `venv` and `ensurepip`, plus
`sha256sum` and either `curl` or `wget`. It installs for the current user and
does not require root privileges.

Download the installer from the release you want and run it:

```sh
curl -fsSLO https://github.com/strixoss/StrixApplication/releases/download/strixtuissh-v0.3.5/install.sh
sh install.sh --version 0.3.5
```

To install a different version, replace `strixtuissh-v0.3.5` in the URL with
the tag of that release and change `--version 0.3.5` to its version number.
To install the latest release instead, run `sh install.sh` without `--version`.
All releases are listed here:

**https://github.com/strixoss/StrixApplication/releases**

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