# Using dpkg

These are valid option flags in dpkg.

My dpkg is in /usr/bin/dpkg /usr/lib/dpkg /etc/dpkg /usr/share/dpkg /usr/share/man/man1/dpkg.1.gz and is
Debian 'dpkg' package management program version 1.19.8 (amd64).

## Lowercase option flags

`dpkg -a` says needs an action option. This creates an archive file

`dpkg -b` says --build needs a directory argument

`dpkg -c` says --contents takes exactly one argument

`dpkg -e` says --control needs a .deb filename argument

`dpkg -f` says --field needs a .deb filename argument

`dpkg -i` says requested operation requires superuser privilege

`dpkg -l` lists installed/installable pagages

`dpkg -p` lists packages

`dpkg -r` says requested operation requires superuser privilege

`dpkg -s` lists packages

`dpkg -x` --extract needs .deb filename and directory arguments

## Uppercase option flags

`dpkg -A` needs to be able to open the log file '/var/log/dpkg.log' and says --record-avail needs at least one package archive file argument

`dpkg -B` needs an action option. used to build a Debian package from a source directory

`dpkg -C` doesn't return anything just ends if used by itself, but used to check the integrity of a Debian package file

`dpkg -D` says option takes a value, but allows you to extract the contents of a Debian package file (.deb) without actually installing it

`dpkg -E` needs an action option, but used to extract the control information from a Debian package file (.deb)

`dpkg -G` needs an action option, but used to list the files installed by a specific Debian package

`dpkg -I` says --info needs a .deb filename argument

`dpkg -L` --listfiles needs at least one package name argument

`dpkg -N` says it needs an action option, but I could not find information on this option flag

`dpkg -O` needs an action option, but I could not find information on this option flag

`dpkg -P` says requested operation requires superuser privilege

`dpkg -R` needs an action option. used to remove a Debian package from your system. requires sudo

`dpkg -S` says  --search needs at least one file name pattern argument

`dpkg -V` returns version info?

`dpkg -X` says --vextract needs .deb filename and directory arguments
