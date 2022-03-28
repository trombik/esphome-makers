# `esphome-makers`

[![Tests and build](https://github.com/trombik/esphome-makers/actions/workflows/build.yml/badge.svg)](https://github.com/trombik/esphome-makers/actions/workflows/build.yml)

My `esphome` configuration files at
[Makers Siem Reap](http://info.mkrsgh.org/makerspace/).

## Installing

Clone the repository and install requirements:

* python
* `tox`
* `esphome` including necessary tool-chains, and packages

```console
tox
```

To reinstall the python virtual environment:

```console
tox -r
```

## Activating the `tox` environment

```console
source .tox/python/bin/activate
```

The file to source assumes variants of `bash` (`zsh` works).

## Running the server

```console
esphome dashboard config
```

The URL is [http://127.0.0.1:6052/](http://127.0.0.1:6052/).

## Compiling

```console
esphome compile config/*.yml
```

## Compiling and uploading

Over USB serial converter:

```console
esphome run --device /dev/cuaU0 config/foo.yml
```

Over the Air:

```console
esphome run config/foo.yml
```
