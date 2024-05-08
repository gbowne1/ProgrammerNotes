# Using GNU linker ld

## ld flags

My tests were done with doing these flags individually on a single command line.  ld usually exists at /usr/bin/ld.  My ld is GNU ld (GNU Binutils for Debian) 2.31.1.

### Lowercase flags

ld -d   `ld: no input files` used to enable dynamic linking of libraries. tells the linker to generate dynamic rather than static object files
ld -g   `ld: no input files` used to generate debugging information in the output file.
ld -i   `ld: no input files`
ld -m   `ld: missing argument to -m`  used to specify the output format. The argument to -m is the name of the output format, such as elf's
ld -n   `ld: no input files`
ld -q   `ld: no input files`
ld -r   `ld: no input files` used to generate a relocatable output file.
ld -s   `ld: no input files`
ld -t   `ld: no input files` used to generate debugging information in the output file.
ld -v   reports the version
ld -x   `ld: no input files`

### Uppercase flags

ld -E   `ld: no input files`
ld -G   `ld: no input files`
ld -M   `ld: no input files` used to generate a map file that shows how the linker mapped input sections to output section
ld -N   `ld: no input files`
ld -Q   `ld: no input files`
ld -S   `ld: no input files`
ld -U   `ld: no input files`
ld -V   returns the version plus supported emulations
ld -X   `ld: no input files`

## untested flags

ld -T       used to specifiy the linker file used
ld -o       Specifies the name of the output file (executable or library) to be generated
ld -l       Links against the specified library, searching for it in the standard library directories.
ld -pie     Creates a position-independent executable (PIE), which can be loaded at any address in memory
ld -u       Prevents garbage collection of the specified external symbol.
ld -L       Adds a directory to the library search path.

## Use of ld

`ld -T linker.script input1.o input2.o -o output`
