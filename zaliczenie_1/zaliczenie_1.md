# Zadanie 1
## Sieci
### lan 1
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.0.0/22 | 192.168.0.1 | 192.168.3.254

### lan 2
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.10.0/22 | 192.168.10.1 | 192.168.13.254

### lan 3
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.20.0/22 | 192.168.20.1 | 192.168.23.254

### lan 0 (dla routerów)
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.100.0/24 | 192.168.100.1 | 192.168.100.254

## routery
### router 1
- adres interfejsu 1: 192.168.0.1/22
- adres interfejsu 2: 192.168.100.1/24

### router 2
- adres interfejsu 1: 192.168.10.1/22
- adres interfejsu 2: 192.168.100.2/24

### router 3
- adres interfejsu 1: 192.168.20.1/22
- adres interfejsu 2: 192.168.100.3/24

## Tablice routingu
### router 1
destination | next hop
--- | ---
192.168.10.0/22 | 192.168.100.2/24
192.168.20.0/22 | 192.168.100.3/24

### router 2
destination | next hop
--- | ---
192.168.0.0/22 | 192.168.100.1/24
192.168.20.0/22 | 192.168.100.3/24

### router 3
destination | next hop
192.168.0.1/22 | 192.168.100.1/24
192.168.10.0/22 | 192.168.100.2

# Zadanie 2
## Sieci
### lan 1
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.0.0/22 | 192.168.0.1 | 192.168.3.254

### lan 4
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.10.0/24 | 192.168.10.1 | 192.168.10.254

### lan 5
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.11.0/24 | 192.168.11.1 | 192.168.11.254

### lan 6
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.12.0/24 | 192.168.12.1 | 192.168.12.254

### lan 7
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.20.0.23 | 192.168.20.1 | 192.168.21.254

### lan 8
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.22.0/28 | 192.168.22.1 | 192.168.22.14

### lan 9
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.23.0/26 | 192.168.23.1 | 192.168.23.62

### lan 0 (dla routerów)
adres sieci | adres początkowy | adres końcowy
--- | --- | ---
192.168.100.0/24 | 192.168.100.1 | 192.168.100.254

### routery
### router 1
- adres interfejsu 1: 192.168.0.1/22
- adres interfejsu 2: 192.168.100.1/24

### router 2
- adres interfejsu 1: 192.168.10.1/24
- adres interfejsu 2: 192.168.11.1/24
- adres interfejsu 3: 192.168.12.1/24
- adres interfejsu 4: 192.168.100.2/24

### router 3
- adres interfejsu 1: 192.168.20.1/23
- adres interfejsu 2: 192.168.22.1/28
- adres interfejsu 3: 192.168.23.1/26
- adres interfejsu 4: 192.168.100.3/24

### Tablice routingu
### router 1
destination | next hop
--- | ---
192.168.10.0/22 | 192.168.100.3/24
192.168.20.0/22 | 192.168.100.3/24

### router 2
destination | next hop
192.168.0.0/22 | 192.168.100.3/24
192.168.20.0/22 | 192.168.100.3/24

### router 3
destination | next hop
--- | ---
192.168.0.1/22 | 192.168.100.1/24
192.168.10.0/22 | 192.168.100.2