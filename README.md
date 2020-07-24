# asdf-qt
A plugin for [asdf](https://asdf-vm.com) adding version management for QT.

Currently handles just the open-source distributions of QT 5.

## prerequisites
This plugin builds QT from source, so make sure that your machine have the tools. These can be found [here](https://wiki.qt.io/Building_Qt_5_from_Git#System_Requirements).

## install plugin
```sh
$ asdf plugin-add qt https://github.com/jamesstidard/asdf-qt.git
```

## install pre-compile qt
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
