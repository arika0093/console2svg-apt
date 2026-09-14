# APT repository for console2svg

This repository publishes the official APT repository for [console2svg](https://github.com/arika0093/console2svg).

The repository tracks the latest stable GitHub Release and supports `amd64` and `arm64`. Generated repository metadata and packages are published to the `apt` branch and served directly by GitHub over HTTPS.

## Install

```sh
echo 'deb [trusted=yes] https://raw.githubusercontent.com/arika0093/console2svg-apt/apt stable main' | sudo tee /etc/apt/sources.list.d/console2svg.list
sudo apt update
sudo apt install console2svg
```

Updates are then handled normally:

```sh
sudo apt update
sudo apt upgrade console2svg
```

## Repository signing

The repository is currently unsigned, so the source entry explicitly uses `trusted=yes`. Packages and indexes are served over HTTPS and release assets are verified against GitHub's SHA-256 digest before publication, but this is not a substitute for an APT repository signature.

A future signing setup should keep the private OpenPGP key in a GitHub Actions secret or an external signing service; the private key must never be committed to this public repository.
