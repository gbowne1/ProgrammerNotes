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

it appears to be in /usr/bin/df /usr/share/man/man1/df.1.gz

## Lowercase flags

- `df -a` used to display information about all mounted file systems on your system, including those that are not mounted on a regular directory.

- `df -h` similar to `-a`. in a more user friendly manner.

- df -i similar to `-a` but seems to list the Inodes Iused Ifree

- df -k seems to list by block size; 1k blocks?

- df -l provides more detailed information as compared to just using `df`

- df -m used to display information about mounted file systems with the sizes and usage reported in megabytes (MB).

- df -t requires an argument. displays information about mounted file systems, focusing on their file system types.

- df -v  provides a more verbose output compared to the basic df command.

- df -x requires an argument. not a standard option. could not find any information on this option flag.  just returns requires an arg.

## Uppercase flags

- df -B requires an argument. displays information about mounted file systems with the sizes and usage reported in bytes (B) instead of the default 1024-byte blocks.

- df -F requires an argument. not a standard option.

- df -H must be same as `df -h`

- df -P displays information about mounted file systems, focusing on their physical block size and usage.

- df -T  shows the total and free space for all mounted file systems on your system. 

Any flag not listed here did not return any results when used on the command line by itself
or reported invalid option.

By default, df displays information in 1024-byte blocks.