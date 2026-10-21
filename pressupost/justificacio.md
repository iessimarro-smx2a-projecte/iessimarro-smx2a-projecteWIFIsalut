# Justificació del pressupost · WiFi SALUT

> **Issue:** #3 · Pressupost i llistat d'equipament
> **Responsable:** AlumneC (tècnic/a de configuració)
> **Full de càlcul:** [pressupost-detallat.xlsx](pressupost-detallat.xlsx) (fulls *Pressupost*, *Comparativa* i *Pressupost PoE*)

## 1. Resum

| Concepte | Import |
| --- | ---: |
| Base imposable | 3.011,50 € |
| IVA (21 %) | 632,42 € |
| **Total** | **3.643,92 €** |

Els preus són **orientatius**, consultats a dos distribuïdors en línia, i s'han de confirmar amb un pressupost formal abans de fer la comanda.

## 2. Criteris de selecció dels equips

| Equip | Elecció | Justificació |
| --- | --- | --- |
| Punts d'accés | UniFi 6 Lite (×6) | WiFi 6, alimentació PoE, muntatge al sostre i gestió centralitzada gratuïta amb UniFi Network Application. |
| Switch | UniFi USW-24-PoE | 24 ports GbE, VLANs 802.1Q i 95 W de PoE+ als **ports 1 a 16**. S'integra al mateix controlador que els APs. |
| Servidor | Servidor torre d'entrada amb RAID 1 | Allotja UniFi Controller, FreeRADIUS, DHCP i tallafocs. El RAID 1 protegeix la configuració davant la fallada d'un disc. |
| Cable | Cat6 U/UTP **LSZH** | En un edifici sanitari el cable ha de ser de baixa emissió de fums i lliure d'halògens. |
| SAI | 1500 VA en format rack | Manté el switch, el servidor i els APs (via PoE) durant un tall elèctric curt. |

## 3. Comprovació del pressupost PoE

| Càlcul | Valor |
| --- | ---: |
| Consum màxim d'un UniFi 6 Lite | 12 W |
| Consum de 6 APs | 72 W |
| Potència PoE del switch | 95 W |
| **Marge disponible** | **23 W (ús del 76 %)** |

> ⚠ Només els **ports 1 a 16** del switch subministren PoE+. Els APs s'han de connectar sempre a aquests ports.

## 4. Càlcul del cable

| Tram | Longitud aproximada |
| --- | ---: |
| 6 enllaços d'AP (de 18 a 25 m cadascun) | 134 m |
| 4 troncals cap als racks secundaris (2 per rack) | 40 m |
| Marge del 20 % | 35 m |
| **Total** | **≈ 209 m** → 1 bobina de 305 m |
