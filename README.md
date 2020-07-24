# asdf-qt
A plugin for [asdf](https://asdf-vm.com) adding version management for QT.

Currently handles just the open-source distributions of QT 5.

## install plugin
```sh
$ asdf plugin-add qt https://github.com/jamesstidard/asdf-qt.git
```

## install pre-compile qt
Installing from the pre-compiled binaries, this plugin will need access to
both `xmllint` (to parse the xml manifests) and `7z` (to unzip the downloaded archives).

### macOS
```sh
# xmllint already installed
$ brew install p7zip
```

### Ubuntu
```sh
$ sudo apt-get update && sudo apt install -y libxml2-utils p7zip-full p7zip-rar 
```

Once those are on your system you can:

```sh
$ asdf install qt 5.13.2
```

## install qt from source
You can install from the source repository instead of using the pre-compiled binaries
by using the version format "ref:<branch-or-tag-name>".

QT has branches named for the version, so be aware of the different between "ref:5.13.2"
vs "ref:v5.13.2". The former will install from the head of the branch "5.13.2", where as
"v5.13.2" will install the tagged final release source.

If you're building from source make sure you have the appropriate pre-requisites and a 
lot of patience waiting for the build to complete. The required build tools can be found 
[here](https://wiki.qt.io/Building_Qt_5_from_Git#System_Requirements).

```sh
$ asdf install qt ref:v5.13.2
```
