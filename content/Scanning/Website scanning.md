---
title: "Website scanning"
date: 2021-02-10T17:23:05+01:00
---

# Nikto
## Classic scan

`nikto -h $site`


# Gobuster

## Classic scan
`gobuster dir -u $site -w "/usr/share/wordlists/SecLists/Discovery/Web-Content/raft-small-words.txt" -t 20 -o scans/gobuster`

## VHOST scan

`gobuster vhost -u $site -w "/usr/share/wordlists/SecLists/Discovery/DNS/subdomains-top1million-5000.txt" -t 20 -o scans/gobuster_vhost`

``

# Wordpress

## Classic Wordpress scan
Quick scan :
`wpscan --url $site`

## Aggressive scan
In order to enumerate all plugins :
`wpscan --url $site --plugins-detection aggressive`

## With token
`wpscan --url $site --api-token $token`
