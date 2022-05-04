---
title: "LFI"
date: 2022-05-04T13:03:15+02:00
---

# LFI
## Get user running a process with file

* cat `/proc/self/status` check `gid` and `uid`
* Correlate with `/etc/passwd`

## Command execution with LFI

* Get content of `/cat/proc/environ` (from webserver)

Then :
* Run command in user-agent string:` <? php echo "hello"; ?>`
* If mail access, then send a mail with a command inside and run the command via ?ls=command (see [Beep video](https://www.youtube.com/watch?v=XJmBpOd__N8&t=963))
