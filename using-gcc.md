# Using GCC

My gcc is currently in /usr/bin/gcc /usr/lib/gcc and is gcc version 8.3.0 (Debian 8.3.0-6)

## Important Flags

There are some important flags that can be used with GCC to compile C programs.
these were tested by doing each flag individually. These may or may not be documented.

using GNU g++ (for C++) may use these same flags as gcc.

### Lowercase flags

`-c` = Might need input files. instructs the compiler to perform a compilation but stop before linking

`-d` = Needs argument(s). can be used several ways. does disassembly,  specifies a directory to search for
header files or provides additional debugging information.

`-e` = Needs argument(s). used to emit preprocessed source code. `gcc -e myprogram.c -o myprogram.i`

`-g` = Might need input files, used to enable debugging information `gcc -g myprogram.c -o myprogram`

`-h` = Needs argument(s). display a brief help message

`-l` = Needs argument(s). used to link your program with a specific library `gcc -l<library_name> myprogram.c -o myprogram`

`-n` = Might need input files? not a standard option.

`-o` = Needs a filename after -o. used to specify the output filename for the compiled program. `gcc -o output_filename source_file.c`

`-p` = Might need input files. not a standard option

`-r` = Might need input files. not a standard option

`-s` = Might need input files. can be used several different ways. strips symbols

`-t` = Might need input files

`-v` = used to print the compiler version information and the command line used for compilation. `gcc -v myprogram.c -o myprogram`

`-w` = Might need input files. used to suppress warnings during compilation

`-x` = Needs argument(s). used to specify the language of the source code file `gcc -x <language> <source_file> -o <output_file>`

`-z` = Needs arguments. used to enable optimizations specific to embedded systems `gcc -z <optimization_option> <source_file> -o <output_file>`

### Uppercase flags

====================================================================
-A = Needs assertions. Possibly use for target architecture, but this controls pre-processor assertions.

-B = Needs argument(s) but specifies alternate compiler toolchain locations.

-C = Might need input files. Keeps comments during processing?

-D = Macro name missing after -D, for PreProcesor Macros

-E = Might need input files.  Preprocess only; do not compile or link.

-F = Needs a path after this flag, Specify a path for certain files.

-H = Might need input files. Print the names of header files included.

-I = Needs a path after this flag, Add a directory to the list of directories to be searched for header files.

-J = Needs argument(s) Used for parallel builds; needs specific arguments.

-L = Needs argument(s) Add a directory to the library search path.

-M = Might need input files Generate makefile dependencies.

-N = Might need input files

-O = Might need input files,  Set optimization level (e.g., -O0, -O1, -O2, -O3, -Os, -Ofast).

-P = Might need input files Preprocess only; do not include line numbers in the output

-Q = Might need input files. Print information about the compiler's internal workings.

-R = Needs argument(s)

-S = Might need input files Compile to assembly language

-T = Needs argument(s), Specify a linker script

-U = Macro name missing after -U ; undefine a pre-processor macro

-W = Might need input files. -W <warning> enable specific warnings

-X = Might need input files

-Z = Might need input files

## Optimization

`-mtune` =
`-march` =
`-O<level>` =
