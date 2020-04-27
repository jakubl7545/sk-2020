## System operacyjny w środowisku sieciowym

☻### Zadania


1. Z wykorzystaniem maszyny wirtualnej, zainstaluj SO oraz wypisz parametry konfiguracji IP tj:
   * Adres
   * Maska
   * Adres bramy
   * DNS 1
   * DNS 2
    
    Powyższe parametry uzyskaj na wszystkich z wymienionych systemów

   * [Linux Alpine](https://alpinelinux.org/)
   * [Linux Debian](https://www.debian.org/)
   * [Linux CentOS](https://www.centos.org/)
   * Windows 

2. Sprawdź oraz przygotuj charakterystykę dla przykładowego urządzenia w Twojej sieci domowej
   * Adres
   * Maska
   * Adres bramy
   * DNS 1
   * DNS 2
  
    Przygotuj dokumentację graficzną Twojej sieci domowej, uwzględnij adresy i urządzenia

3. Zarejestruj konto w CISCO Academy celem pobrania Packet tracer 
   https://www.netacad.com/courses/packet-tracer

4. Dlaczego umiejętnosci z zakresu sieci komputerowych mogą mi się przydać? :)


### Charakterystyka systemu operacyjnego

| Charakterystyka           | wartość               | komentarz                |
| -------------             |:-------------:        | -----:                    |
| nazwa                     | linux                 | debian 10                  |
| cfg interfejsów           | /etc/network/interfaces | debian 10         |
| Konfiguracja ip           | ``$ ip addr ``         | shows all eth interfaces   | 
| Tablica routingu          | ``$ ip route show ``  |     | 
| check nameservers (DNS)   | ``$ cat /etc/resolv.conf ``  |     | 

### Konfiguracja połączenia sieciowego

| Parametr | wartość           | komentarz |
| ------------- |:-------------:| -----:|
| Adres IP      | 192.168.241.129        | przydzielony przez DHCP |
| Maska podsieci| 192.168.241.129/**24** | **255.255.255.0**    |
| Brama         | 192.168.241.2         | default from route table |
| DNS 1         | 192.168.241.2      | cat /etc/resolv.conf     |

### Charakterystyka urządzenia w sieci domowej

| Parametr | wartość           | komentarz |
| ------------- |:-------------:| -----:|
| Adres IP      | 10.71.196.0        | przydzielony przez DHCP |
| Maska podsieci| 192.168.241.129/**20** | **255.255.240.0**    |
| Brama         | 10.71.192.1         | default from route table |
| DNS 1         | 217.113.224.135      |  ipconfig /all     |
