# Introduction

Helper scripts to with deploying and testing on multiple devices.

Tested only on OS X.

## Installation

Use your favorite mechanism to adding the root folder of this repository
to your PATH.

For example, the following command does the trick when run in the root
folder:

```
$ echo export PATH=\$PATH:$(pwd) >> ~/.profile && source ~/.profile
```

## Android examples

```
$ madb install -r /path/to/some/file.apk
$ madb shell monkey -p some.package.name 1
$ madb shell am force-stop some.package.name

$ mstart some.package.name /folder/for/logs
```

## Troubleshoot

If scripts don't work or stop working, one can try to run:
```
killall adb
```
This might be sometimes needed if scripts don't exit cleanly and leave
adb processes hanging around.