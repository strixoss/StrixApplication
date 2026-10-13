# StrixTuiSSH — Linux Releases

StrixTuiSSH is a terminal (TUI) SSH client for Linux, written in Python.

This repository is used **only for distributing releases**. It contains no source code and is not used for development.

## Installation

Download the installer from the release you want and run it:

```sh
curl -fsSLO https://github.com/strixoss/StrixApplication/releases/download/strixtuissh-v0.1.0/install.sh
sh install.sh
```

To install a different version, replace `strixtuissh-v0.1.0` in the URL with the tag of that release. All releases are listed here:

**https://github.com/strixoss/StrixApplication/releases**

### Review before running

`install.sh` is a shell script that runs on your machine. Read it before executing it:

```sh
less install.sh
```

### Verifying the installer

Each release includes a `SHA256SUMS` file. To verify the downloaded installer:

```sh
curl -fsSLO https://github.com/strixoss/StrixApplication/releases/download/strixtuissh-v0.1.0/SHA256SUMS
sha256sum -c SHA256SUMS --ignore-missing
```

If the check fails, do not run the script.

## Versioning

Release tags use the format `strixtuissh-vMAJOR.MINOR.PATCH` and follow [Semantic Versioning](https://semver.org/). While the major version is `0`, the interface and configuration may change between minor versions. Read the release notes before updating.

Pre-releases are marked as *Pre-release* on the releases page.

## Reporting issues

Issues and pull requests are **disabled** in this repository. Please report bugs and feature requests through the project's main channel: `<link to issue tracker / contact>`.

## License

See the license terms included with each release.