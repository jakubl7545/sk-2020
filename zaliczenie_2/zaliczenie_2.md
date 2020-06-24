# Zadanie 1
## Konfiguracja interfejsów sieciowych
### PC1
plik konfiguracyjny - /etc/network/interfaces
# WAN
auto eth0
iface eth0 inet dhcp
# LAN 1
auto eth1
iface eth1 inet static
address 192.168.0.1
netmask 255.255.252.0
### PC2
plik konfiguracyjny - /etc/network/interfaces
# LAN 1
auto eth0
iface eth0 inet dhcp

## DHCP
instalacja pakietu - apt-get install isc-dhcp-server
plik konfiguracyjny - /etc/dhcp/dhcpd.conf

subnet 192.168.0.0 netmask 255.255.252.0 {
  range 192.168.0.2, 192.168.3.254;
  option domain-name-servers 8.8.8.8, 199.85.126.10;
  option routers 192.168.0.1;
}

host printer {
  hardware ethernet <MAC address>;
  fixed_address 192.168.0.100;
}

## Translacja adresów dla kluczowych zasobów
plik konfiguracyjny - /etc/hosts
192.168.0.1 router.mojaorganizacja.pl
192.168.0.100 drukarka.mojaorganizacja.pl
192.168.0.200 erp.mojaorganizacja.pl

## NAT
Włączenie przekazywania pakietów między interfejsami
plik konfiguracyjny - /etc/sysctl.conf
# Uncomment the next line to enable packet forwarding for IPv4
net.ipv4.ip_forward=1
instalacja pakietu - apt-get install iptables
Włączenie NAT
iptables -t nat -a postrouting -o eth0 -j masquerade