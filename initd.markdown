---
type: post
title:  Managing XAP with init.d
categories: SBP
weight: 1900
parent: production.html
---


|Author|XAP Version|Last Updated | Reference | Download |
|------|-----------|-------------|-----------|----------|
| Patrick May| 10.0 | Sept 2014|    |    |




# Introduction
The standard for managing long running daemons and daemon-like processes on Unix
systems is via a script residing in the /etc/init.d directory. Typically these scripts provide
four capabilities:

- start<br>
- stop <br>
- restart<br>
- status

This basic set of features can manage a simple   XAP configuration. More complex configurations require correspondingly more functionality.

# An init.d Script Shell
A typical init.d script follows this pattern:


```console
#!/bin/sh

# Script description


start(){
}

stop(){
}

status(]{
}

case "$1" in start)
    start
    ;;

    stop)
        stop
    ;;

    restart)
     stop
     start
   
```