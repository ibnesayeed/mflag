mflag
====

[![Go Documentation](http://img.shields.io/badge/go-documentation-blue.svg?style=flat-square)][godocs]

[godocs]: http://godoc.org/github.com/tcnksm/mflag

This is fork of Docker's [mflag](https://github.com/docker/docker/tree/master/pkg/mflag) pacakge. `mflag` is fork of official [flag](https://golang.org/pkg/flag/) pacakge, which enables to use multiple flag for command line flag parsing. `mflag` is provided as docker's internal pacakge and has other docker internal dependencies, so every time we use it we need to fetch all docker code... (`go get` takes long time). This fork is independ package of `mflag`. You can use this without large code base dependencies.

## Features

This mflag includes more features, 

- More readable usage message format. 
- You can set `Synopsis`, `Description` and `Example` on usage message.

```bash
Usage:

  {{ .Synopis }}

Description:

  {{ .Description }}

Options:

  {{ .Option }} 

Examples:

  {{ .Example }}
```

