# Using uname

I have never really explored uname though my uname comes from /usr/bin/uname and is from

uname (GNU coreutils) 8.30 from the FSF.

- uname -a `Linux gregbowne 4.19.0-16-amd64 #1 SMP Debian 4.19.181-1 (2021-03-19) x86_64 GNU/Linux`

- uname -i `unknown` prints the hardware platform

- uname -m `x86_64` prints the machine hardware name aka the architecture of the CPU

- uname -n `gregbowne`

- uname -o `GNU/Linux` prints the operating system

- uname -p `unknown`  prints the processor information

- uname -r `4.19.0-16-amd64` is the kernel release

- uname -s `Linux` this prints the kernel name

- uname -v `#1 SMP Debian 4.19.181-1 (2021-03-19)`

Help is available by uname --help  and currently shows:

$ uname --help
Usage: uname [OPTION]...
Print certain system information.  With no OPTION, same as -s.

  -a, --all                print all information, in the following order,
                             except omit -p and -i if unknown:
  -s, --kernel-name        print the kernel name
  -n, --nodename           print the network node hostname
  -r, --kernel-release     print the kernel release
  -v, --kernel-version     print the kernel version
  -m, --machine            print the machine hardware name
  -p, --processor          print the processor type (non-portable)
  -i, --hardware-platform  print the hardware platform (non-portable)
  -o, --operating-system   print the operating system
      --help     display this help and exit
      --version  output version information and exit

GNU coreutils online help: <https://www.gnu.org/software/coreutils/>
Full documentation at: <https://www.gnu.org/software/coreutils/uname>
or available locally via: info '(coreutils) uname invocation'

Uppercase/Capitalized flags don't seem to work here.. but hasn't been tested fully.
