I have been trying to block ipad device with iptables based on the static dhcp lease, but it didn't work. Because ipad also uses ipv6 

https://superuser.com/questions/1104484/disable-ipv6-with-openwrt
A simpler approach would be to SSH into your OpenWrt router and execute the following commands:

uci set 'network.lan.ipv6=on'
uci set 'network.wan.ipv6=on'
uci set 'dhcp.lan.dhcpv6=enabled'
/etc/init.d/odhcpd enable 
uci commit
