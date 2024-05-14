# using ifconfig

## Flags

`ifconfig -a` is `all` mode, useful for seeing all the interfaces that are configured on the system, regardless of their current state
`ifconfig -h` returns the help including hardware types
`ifconfig -s` returns a listing of things like MTU size as a table
`ifconfig -v` is `verbose` mode, useful when you need detailed information about the configuration of each interface
`ifconfig -V` returns version numbers

There seems to be no applicable uppercase flags as they do not return anything if you
do them individually which is how I tested, other than -V.

Apparently there are some others.. but I have not tested these, other than when I tried these did not return anything when done individually.

-s Shows statistics for each network interface.
-r Displays the network interfaces in reverse order.
-n Shows numerical addresses instead of trying to determine symbolic host, port, or user names.
-l Uses large addresses instead of trying to determine symbolic host, port, or user names.
-d Detach the given packet from the network stream.
-I Specifies the network interface to be configured.
-e Displays the Ethernet (MAC) address of the interface.
-M Displays the media type of the interface.
-m Displays the Maximum Transmission Unit (MTU) of the interface.
-p Sets the interface into promiscuous mode.
-q Suppresses the display of certain information.
-t Sets the timeout for the interface.
-u Specifies the unit number of the interface.
-w Writes the current configuration to the system's network configuration files.
-f This option was used to set the IP address of an interface to a fixed address.
-g Specifies the default gateway for the interface. This is more commonly managed with the ip route command in modern usage.
-I Specifies the network interface to be configured. This is a more general option.
-P Specifies the network prefix for the interface. This is more commonly managed with the ip addr command in modern usage.

`--` flags seem to be used with `up` as in `ifconfig eth0 192.168.1.1 -- up` or `ifconfig eth0 up -- 192.168.1.1 netmask 255.255.255.0`.
However, -- could be used for vebose flags like `--help`.

there are man pages at man ifconfig.
