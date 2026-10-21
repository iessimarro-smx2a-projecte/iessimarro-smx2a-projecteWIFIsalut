# Disseny de VLANs i esquema d'adreçament IP · WiFi SALUT

> **Issue:** #4 · Disseny de VLANs i esquema d'adreçament IP
> **Responsable:** AlumneA (coordinador/a tècnic/a)

## 1. Estructura de VLANs

| VLAN | Nom | Usuaris i equips | SSID associat |
| :-: | --- | --- | --- |
| 10 | ADMIN | Personal administratiu i direcció | `WIFISALUT-ADMIN` |
| 20 | SALUT | Personal sanitari (consultes i infermeria) | `WIFISALUT-SALUT` |
| 30 | CONVIDATS | Pacients i acompanyants | `WIFISALUT-CONVIDATS` |
| 99 | GESTIO | Switch, punts d'accés i servidor | Cap (no s'emet per WiFi) |

## 2. Pla d'adreçament

| VLAN | Subxarxa | Passarel·la (servidor) | Rang DHCP | Adreces útils |
| :-: | --- | --- | --- | :-: |
| 10 | 192.168.10.0/24 | 192.168.10.1 | 192.168.10.100 – 192.168.10.199 | 254 |
| 20 | 192.168.20.0/24 | 192.168.20.1 | 192.168.20.100 – 192.168.20.199 | 254 |
| 30 | 192.168.30.0/24 | 192.168.30.1 | 192.168.30.50 – 192.168.30.250 | 254 |
| 99 | 192.168.99.0/24 | 192.168.99.10 | Reserves estàtiques | 254 |

> La VLAN 30 té un rang més gran perquè a la sala d'espera hi pot haver molts dispositius alhora. El temps de concessió (*lease*) dels convidats serà curt (2 hores).

### Adreces fixes de la VLAN 99 (gestió)

| Equip | Adreça IP |
| --- | --- |
| Servidor Ubuntu (UniFi Controller, FreeRADIUS) | 192.168.99.10 |
| Switch UniFi USW-24-PoE | 192.168.99.2 |
| AP-PB-01 / AP-PB-02 | 192.168.99.21 / 192.168.99.22 |
| AP-P1-01 / AP-P1-02 | 192.168.99.23 / 192.168.99.24 |
| AP-P2-01 / AP-P2-02 | 192.168.99.25 / 192.168.99.26 |

## 3. Assignació de ports del switch

| Ports | Mode | VLANs | Ús |
| --- | --- | --- | --- |
| 1 – 6 | Troncal (*trunk*) | 99 sense etiqueta · 10, 20, 30 etiquetades | Punts d'accés (PoE+) |
| 7 – 16 | Accés | Reserva | Futurs dispositius PoE |
| 20 – 21 | Troncal | 10, 20, 99 | Racks secundaris RS-PB i RS-P2 |
| 24 | Troncal | 10, 20, 30, 99 etiquetades | Servidor Ubuntu |

## 4. Política de segmentació

| Origen \ Destinació | VLAN 10 | VLAN 20 | VLAN 30 | VLAN 99 | Internet |
| --- | :-: | :-: | :-: | :-: | :-: |
| **VLAN 10 · ADMIN** | — | ❌ | ❌ | ❌ | ✅ |
| **VLAN 20 · SALUT** | ❌ | — | ❌ | ❌ | ✅ |
| **VLAN 30 · CONVIDATS** | ❌ | ❌ | — | ❌ | ✅ (limitat) |
| **VLAN 99 · GESTIO** | ✅ | ✅ | ✅ | — | ✅ (actualitzacions) |

Criteris:

- Cap VLAN d'usuaris pot accedir a la VLAN de gestió: així ningú pot entrar a la configuració del switch, dels APs o del servidor des de la WiFi.
- La xarxa de convidats només ix a internet i té **aïllament de clients** activat: un dispositiu de la sala d'espera no veu els altres.
- El trànsit entre ADMIN i SALUT està bloquejat per defecte. Si cal una excepció (per exemple, una impressora compartida), s'obrirà una issue i es documentarà la regla.
- Les regles es configuren al servidor a la issue #15 i es verifiquen a la issue #19.
