Gateway Server Configuration
==============

in this repository I will save and share all the meaningful configuration files of my little internal server Keid (named after a white dwarf star.. it is a white old netbook..).
It is a gateway from my internal ethernet area and my wifi subnet

 * interfaces: /etc/network/interfaces
 * firewall: iptables configuration (in /etc/network/if-up.d)


Network configuration
---

###eth0
static 192.168.2.1
iptables: ACCEPT, MASQUERADE and FORWARD

###wlan0
static 192.168.1.253 (my access point/router has 192.168.1.254)
WPA-PSK configured in `/etc/network/interfaces`

