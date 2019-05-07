# Snap packages for Dart API

This repository contains the [snapcraft](https://snapcraft.io/) build files
to build a snap package for [Dart](https://www.dartlang.org/).

* The Dart distribution simply repackages the official **Linux x86_64** binaries.

* Current Dart API version is: **2.2.0**

## Building

To build the snaps, `cd` into `dart-sdk/` and call `snapcraft`, e.g.:

```bash
cd dart-sdk/
snapcraft
```

To install the snap package:

```bash
sudo snap install <snap-file>.snap --classic --dangerous
```

The snap package use classic confinement due to neccesary filesystem access. `--dangerous` is necessary because the local builds are not signed.

## Usage

After installation, all binaries are under the `dart-sdk` namespace (`dart-sdk.dart`, `dart-sdk.dart2js`, etc).

Therefore, it's reccomended to alias the binaries.

```bash
sudo snap alias dart-sdk.dart dart
sudo snap alias dart-sdk.dart2js dart2js
sudo snap alias dart-sdk.dartdevc dartdevc
sudo snap alias dart-sdk.dartanalyzer dartanalyzer
sudo snap alias dart-sdk.dartdoc dartdoc
sudo snap alias dart-sdk.dartfmt dartfmt
sudo snap alias dart-sdk.pub pub
```