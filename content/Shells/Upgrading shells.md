---
title: "Upgrading Shells"
date: 2022-05-04T13:03:15+02:00
---

# Upgrading shell

## python method
`python -c 'import pty; pty.spawn("/bin/bash")'`

## script method
`SHELL=/bin/bash script -q /dev/null`

## common stuff
* Then type CTRL+Z ;
* Type `stty raw -echo;fg` then `reset`.

Also, make sure to use / test with sh, bash, etc. and python, python2, python3

Finally, adjust size, where X and Y are your own values :

`stty rows X columns Y`