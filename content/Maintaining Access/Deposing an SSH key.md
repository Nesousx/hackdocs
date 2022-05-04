---
title: "Deposing an SSH key"
date: 2021-02-10T17:23:05+01:00
---

## Generate key
`ssh-keygen -f $key`

## Place it
`cat $key.pub`, then place it under `~/.ssh/authorized_keys`

## Change rights

`chmod 600 ~/.ssh/authorized_keys`
`chmod 600 $key`
