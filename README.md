Gateway Server Configuration
==============

in this repository I will save and share all the meaningful configuration files of my little internal server Keid (named after a white dwarf star.. it is a white old netbook..)

It is a gateway filtering and natting from my internal ethernet area to my wifi subnet (connected to Internet)

 * interfaces: /etc/network/interfaces
 * firewall: iptables configuration (in /etc/network/if-up.d)
 * dnsmasq.conf
 * hosts-adv
 


Network configuration
---

###eth0
static 192.168.2.1
iptables: ACCEPT, MASQUERADE and FORWARD

###wlan0
static 192.168.1.253 (my access point/router has 192.168.1.254)
WPA-PSK configured in `/etc/network/interfaces`



Services
---
#### DHCP and DNS (with blacklist)
Using dnsmasq (see configuration file dnsmasq.conf), this gateway provides dhcp to the subnet and dns resolution.

In particular, it adds some specific hosts from my subnet (using /etc/hosts) and blacklists some domains (see hosts-adv)

