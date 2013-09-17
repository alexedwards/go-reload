go-reload
=========

This is a Bash script for automatically reloading Go programs. It acts as a wrapper for `go run`, stopping and restarting the process whenever a `.go` file in the monitored directory is saved.

It comes in useful when developing Go web applications.

Installation
------------

1. Install [inotify-tools](https://github.com/rvoicilas/inotify-tools) and clone this repository:

```
$ sudo apt-get install inotify-tools
$ git clone https://github.com/alexedwards/go-reload.git
```

2. Make the script executable and move it to somewhere on your system path. For example:

```
$ cd go-reload
$ chmod +x go-reload
$ mv go-reload /usr/local/bin
```

Usage
-----

Use the script in place of `go run`. For example:

```
$ go-reload main.go
==> Press Ctrl+C to exit
Setting up watches.  Beware: since -r was given, this may take a while!
Watches established.
```