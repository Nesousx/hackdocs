---
title: "nmap"
date: 2021-02-10T17:23:05+01:00
---

## Classic scan (for HTB box)

````text
sudo nmap -sC -sV -oA scans\$box_name
````


## Full scan
````text
sudo nmap -p- -T4 scans\$box_name
````
