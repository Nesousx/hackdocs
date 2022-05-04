---
title: "Command history"
date: 2021-02-10T17:23:05+01:00
---

## Linux

Command history can be found `/~.bash_history`. Make sure to check variant for other such as zsh, fish, etc.

Also, the `history` command can be used.

## Windows
### cmd

`doskey /history`

### Powershell

PowerShell command history can be found in :

`Users\$name\appdata\roaming\Microsoft\Windows\PowerShell\PSReadline` then `gc ConsoleHost_history.txt`

You can also try `Get-History | Format-List -Property *`


