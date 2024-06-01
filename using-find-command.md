# Using find

Here are the flags that can be used with and what they do

My version of `find` seems to be:

```shell
find (GNU findutils) 4.6.0.225-235f
```

My version of find comes from /usr/bin/find /usr/share/man/man1/find.1.gz /usr/share/info/find.info-2.gz
/usr/share/info/find.info-1.gz /usr/share/info/find.info.gz

## Lowercase flags

find -a says `find: invalid expression; you have used a binary operator '-a' with nothing before it.`

find -d says `ind: warning: the -d option is deprecated; please use -depth instead, because the latter is a POSIX-compliant feature.`

find -o says `find: invalid expression; you have used a binary operator '-o' with nothing before it.`

## Uppercase flags

find -D says `find: Missing argument after the -D option.`

find -H lists files in the directory

find -L lists files in the directory

find -O says `find: The -O option must be immediately followed by a decimal integer`

find -P lists files in the directory

Any flag not listed here did not return any results when used on the command line by itself
or reported invalid option.

there is a help at `find --help`

The usage is typically:
find <starting_directory> <expression> <action>

There is a manual here: <https://www.gnu.org/software/findutils/find>

you can also do:

find -name
find -size
find -type
find -print
find -delete (use with caution)
find -exec (executes a command)
