go-reload
=========

**Note:** This repository is now archived. Please use the excellent https://github.com/air-verse/air for your live reloading needs!

---

This is a Bash script for automatically reloading Go programs. It acts as a wrapper for `go run`, stopping and restarting the process whenever a `.go` file in your current directory or `$GOPATH/src` folder is modified or moved.

It comes in useful when developing Go web applications.

Installation
------------

1) Install [inotify-tools](https://github.com/rvoicilas/inotify-tools) and clone this repository:

```
$ sudo apt-get install inotify-tools
$ git clone https://github.com/alexedwards/go-reload.git
```

2) Make the script executable and move it to somewhere on your system path. For example:

```
$ cd go-reload
$ chmod +x go-reload
$ sudo mv go-reload /usr/local/bin/
```

Usage
-----

Use the script in place of `go run`. For example:

```
$ go-reload main.go
== Go-reload
>> Watching directories, CTRL+C to stop
```

By default `go-reload` watches for changes to `*.go` files only. You can change this behaviour so that all file types are watched by using the `-a` flag. For example:

```
$ go-reload -a main.go
== Go-reload
>> Watching directories, CTRL+C to stop
```

