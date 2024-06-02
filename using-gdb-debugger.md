# using the GNU debugger gdb

My version of the GNU debugger gdb is GNU gdb (Debian 8.2.1-2+b3) 8.2.1
It is in /usr/bin/gdb /etc/gdb /usr/include/gdb /usr/share/gdb

## lowercase flags

`gdb -b` requires an argument. starts GDB in batch mode. `gdb -b <batch_file_name>`

`gdb -c` requires an argument. allows you to specify a command to be executed immediately after GDB starts.

`gdb -d` requires an argument. allows you to debug a running process `gdb -d <PID>`

`gdb -e` requires an argument.  used to specify an environment variable to be set for the program being debugged.

`gdb -f` starts the repl. used to specify a core file for debugging. `gdb -f <core_file_name>`

`gdb -h` prints the help

`gdb -i` requires an argument. used to start GDB in interactive mode. `gdb -i <program_name>`

`gdb -l` requires an argument. not a common option flag.

`gdb -n` starts the repl. not a common option flag

`gdb -p` requires an argument. used to specify the PID (Process ID) of a running process that you want to attach to and debug.

`gdb -q` used to suppress the initial startup message when launching GDB. just says (gdb).

`gdb -r` starts the repl.  used to restart a program that has crashed or terminated abnormally.

`gdb -s` requires an argument.  is a shorthand for the step command. `gdb -s <program_name>`

`gdb -t` says option `-t` is ambiguous might be `-tui` or `-tty`

`gdb -u` says option `-ui` requires an argument

`gdb -v` prints the version

`gdb -w` starts the repl. used to set watchpoints. `gdb -w <program_name>` from there you can use the watch command.

`gdb -x` requires an argument. used to execute a GDB command script. `gdb -x <script_name> <program_name>`

There's only 1 upperase flag

`gdb -D` requires an argument. used to define preprocessor macros for the program being debugged

Help is in `gdb --help` or `gdb -h`