Sipcalc Features include:
- IPv4
  * Multiple address and netmask input formats.
  * Retrieving of address information from interfaces.
  * Classfull and CIDR output.
  * Multiple address and netmask output formats (dotted quad, hex, number
    of bits).
  * Output of broadcast address, network class, Cisco wildcard, hosts/range,
    network range.
  * Output of multiple types of bitmaps.
  * Output of a userdefined number of extra networks.
  * Multiple networks input from commandline.
  * Parsing of a newline seperated list of networks from standard input (STDIN).
  * The ability to "split" a network based on a smaller netmask, now also with
    recursive runs on the generated subnets.
  * DNS resolution.
- IPv6
  * Compressed and expanded input addresses.
  * Compressed and expanded output.
  * Standard IPv6 network output.
  * v4 in v6 output.
  * Reverse dns address generation.
  * The ability to "split" a network based on a smaller netmask, now also with
    recursive runs on the generated subnets.
  * DNS resolution.
  
Clone this repository and `cd` into it.
   ```shell
   git clone https://github.com/AppImage/sagarkhandve/Sipcalc.git
   cd Sipcalc/
   chmod +x Sipcalc
   ./Sipcalc --help

Usage: sipcalc [OPTIONS]... <[ADDRESS]... [INTERFACE]... | [-]>

Global options:
  -a, --all			All possible information.
  -d, --resolve			Enable name resolution.
  -h, --help			Display this help.
  -I, --addr-int=INT		Added an interface.
  -n, --subnets=NUM		Display NUM extra subnets (starting from
				the current subnet). Will display all subnets
				in the current /24 if NUM is 0.
  -u, --split-verbose		Verbose split.
  -v, --version			Version information.
  -4, --addr-ipv4=ADDR		Add an ipv4 address.
  -6, --addr-ipv6=ADDR		Add an ipv6 address.

IPv4 options:
  -b, --cidr-bitmap		CIDR bitmap.
  -c, --classful-addr		Classful address information.
  -i, --cidr-addr		CIDR address information. (default)
  -s, --v4split=MASK		Split the current network into subnets
				of MASK size.
  -w, --wildcard		Display information for a wildcard
				(inverse mask).
  -x, --classful-bitmap	Classful bitmap.

IPv6 options:
  -e, --v4inv6			IPv4 compatible IPv6 information.
  -r, --v6rev			IPv6 reverse DNS output.
  -S, --v6split=MASK		Split the current network into subnets
				of MASK size.
  -t, --v6-standard		Standard IPv6. (default)

Address must be in the "standard" dotted quad format.
Netmask can be given in three different ways:
 - Number of bits    [/nn]
 - Dotted quad       [nnn.nnn.nnn.nnn]
 - Hex               [0xnnnnnnnn | nnnnnnnn]

Copyright (C) Sagar Khandve <i.sagarkhandve@gmail.com>.

