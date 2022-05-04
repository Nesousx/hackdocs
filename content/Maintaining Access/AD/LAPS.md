---
title: "LAPS"
date: 2022-05-04T13:03:15+02:00
---

# LAPS

## Get password in cleartext
`get-adcomputer -filter {ms-mcs-admpwdexpirationtime -like '*'} -prop 'ms-mcs-admpwd', 'ms-mcs-admpwdexpirationtime'`