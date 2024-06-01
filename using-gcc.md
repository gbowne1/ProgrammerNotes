# Using GCC

My gcc is currently in /usr/bin/gcc /usr/lib/gcc and is gcc version 8.3.0 (Debian 8.3.0-6)

## Important Flags

There are some important flags that can be used with GCC to compile C programs.
these were tested by doing each flag individually. These may or may not be documented.

### Lowercase flags

`-c` = Might need input files. instructs the compiler to perform a compilation but stop before linking

`-d` = Needs argument(s)

`-e` = Needs argument(s)

`-g` = Might need input files, used for debugging

`-h` = Needs argument(s)

`-l` = Needs argument(s)

`-n` = Might need input files

`-o` = Needs a filename after -o. This is used for output file(s)

`-p` = Might need input files

`-r` = Might need input files

`-s` = Might need input files

`-t` = Might need input files

`-v` = Prints version stack

`-w` = Might need input files

`-x` = Needs argument(s)

`-z` = Needs arguments

### Uppercase flags

====================================================================
-A = Needs assertions. Possibly use for target architecture
-B = Needs argument(s)
-C = Might need input files
-D = Macro name missing after -D, for PreProcesor Macros
-E = Might need input files
-F = Needs a path after this flag
-H = Might need input files
-I = Needs a path after this flag
-J = Needs argument(s)
-L = Needs argument(s)
-M = Might need input files
-N = Might need input files
-O = Might need input files
-P = Might need input files
-Q = Might need input files
-R = Needs argument(s)
-S = Might need input files
-T = Needs argument(s)
-U = Macro name missing after -U
-W = Might need input files
-X = Might need input files
-Z = Might need input files

## Optimization

`-mtune` =
`-march` =
`-O<level>` =
