# lsof-offenders

List the top processes by number of open files descriptors.

Useful if some process eats all your file descriptors.

Tested on macOS and Ubuntu.

Example:

```
$ sudo lsof-offenders
nopen:2525  pid:250   name:socketfilterfw
nopen:328   pid:72373 name:Google Chrome
nopen:256   pid:87140 name:mysqld
nopen:223   pid:45374 name:Dropbox
...
total fds: 8931
```

## Setup

This python program depends on the [psutil](https://github.com/giampaolo/psutil) package and must run with root privileges:

```
$ pip install psutil
```

Make it available systemwide by putting it in your binary executable path:

```
$ cp lsof-offenders /usr/local/bin/
```
