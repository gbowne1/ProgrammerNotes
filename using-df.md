# Using df

Here are the flags that can be used with and what they do

My version of df seems to be

```shell
$ df --version
df (GNU coreutils) 8.30
Copyright (C) 2018 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <https://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Written by Torbjorn Granlund, David MacKenzie, and Paul Eggert.
```

## Lowercase flags

- df -a

- df -h

- df -i seems to list by Inodes Iused Ifree

- df -k seems to list by block size; 1k blocks?

- df -l

- df -m

- df -t requires an argument

- df -v

- df -x requires an argument

## Uppercase flags

- df -B requires an argument

- df -F requires an argument

- df -H

- df -P

- df -T

Any flag not listed here did not return any results when used on the command line by itself
or reported invalid option.
