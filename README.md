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
```

## Setup

This is a Python 2 program. Install the package `pip install psutil`. `lsof-offenders` must run as sudo, so make sure to install `psutil` for whatever version of python you will be running as root.
