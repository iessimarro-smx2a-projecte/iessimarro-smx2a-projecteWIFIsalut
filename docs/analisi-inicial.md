# Anàlisi inicial · Projecte WiFi SALUT

> **Issue:** #1 · Documentació de l'anàlisi inicial
> **Responsable:** AlumneA (coordinador/a tècnic/a)
> **Fita:** inici (Fases 1 a 3)

## 1. Context

El centre de salut de la comarca ocupa un edifici de tres plantes (planta baixa, primera i segona). Actualment no disposa d'una xarxa sense fil corporativa: el personal treballa només amb els equips cablejats de les consultes i les persones usuàries no tenen cap connexió a la sala d'espera.

La direcció del centre ens demana una xarxa WiFi **segura**, **segmentada** i **gestionada de manera centralitzada**, que separe el trànsit del personal administratiu, del personal sanitari i de les persones convidades.

## 2. Estat actual de la infraestructura

| Element | Situació actual | Observacions |
| --- | --- | --- |
| Connexió a internet | Router de l'operador a la planta primera (sala tècnica) | Fibra simètrica de 600 Mbps |
| Xarxa cablejada | Preses RJ45 Cat5e a les consultes i a l'administració | Sense documentar ni etiquetar |
| Armaris de comunicacions | No n'hi ha. El router és damunt d'una prestatgeria | Cal un rack principal i racks de planta |
| Xarxa sense fil | Un punt d'accés domèstic a recepció, amb clau compartida | Cobertura insuficient i sense segmentació |
| Servidors | Cap servidor propi | Cal un servidor per als serveis de xarxa |
| Alimentació elèctrica | Presa a la sala tècnica sense SAI | Cal protegir els equips de comunicacions |

### Distribució dels espais

| Planta | Espais principals | Usuaris habituals |
| --- | --- | --- |
| Baixa | Recepció i admissió, sala d'espera, sala d'urgències | Personal administratiu, pacients i acompanyants |
| Primera | Consultes mèdiques, infermeria, sala tècnica | Personal sanitari |
| Segona | Administració, direcció, sala de reunions | Personal administratiu i direcció |

## 3. Requeriments funcionals

| Codi | Requeriment |
| --- | --- |
| RF1 | Cobertura WiFi a totes les zones de treball i a la sala d'espera de les tres plantes. |
| RF2 | Tres xarxes sense fil independents: **Admin** (personal administratiu), **Salut** (personal sanitari) i **Convidats** (pacients i acompanyants). |
| RF3 | El personal administratiu s'autentica amb usuari i contrasenya personals, no amb una clau compartida. |
| RF4 | Les persones convidades accedeixen a internet a través d'un portal captiu, amb temps i amplada de banda limitats. |
| RF5 | Des de la xarxa de convidats no s'ha de poder arribar a cap equip del centre. |
| RF6 | Tots els punts d'accés es gestionen des d'un únic controlador. |
| RF7 | La configuració de la xarxa queda documentada i se'n fa còpia de seguretat. |

## 4. Requeriments tècnics

| Codi | Requeriment |
| --- | --- |
| RT1 | 6 punts d'accés WiFi 6 (2 per planta), alimentats per PoE. |
| RT2 | Switch gestionable de 24 ports amb PoE+ i suport de VLANs (IEEE 802.1Q). |
| RT3 | Cablejat estructurat Cat6 LSZH (baixa emissió de fums, obligatori en edificis sanitaris). |
| RT4 | Rack principal a la planta primera i racks secundaris a la planta baixa i a la segona. |
| RT5 | Servidor amb Ubuntu Server LTS per a UniFi Network Application, FreeRADIUS, DHCP i tallafocs. |
| RT6 | Segmentació en 4 VLANs: 10 (Admin), 20 (Salut), 30 (Convidats) i 99 (Gestió). |
| RT7 | Autenticació WPA2-Enterprise (802.1X) contra FreeRADIUS per al SSID Admin. |
| RT8 | Sistema d'alimentació ininterrompuda (SAI) per als equips del rack principal. |

## 5. Mòduls professionals implicats

| Mòdul | Aportació al projecte |
| --- | --- |
| MP01 · Muntatge i manteniment d'equips | Muntatge dels racks, del switch i del servidor |
| MP02 · Xarxes locals | Cablejat estructurat, VLANs, punts d'accés i proves |
| MP05 · Serveis en xarxa | Ubuntu Server, DHCP, UniFi Controller i FreeRADIUS |
| MP06 · Seguretat informàtica | Autenticació 802.1X, segmentació, tallafocs i còpies de seguretat |

## 6. Limitacions

- **Temps:** cinc setmanes d'execució.
- **Pressupost:** limitat; cal justificar cada equip (vegeu la issue #3).
- **Activitat del centre:** les obres no poden interrompre l'atenció a pacients; els treballs amb soroll es fan fora de l'horari de consulta.
- **Edifici:** no es poden fer regates a les parets; el cablejat va per canaleta o pel fals sostre.

## 7. Documents relacionats

- [Document de repte (Annex A)](document-repte.md)
- [Planificació i fitxes d'activitat](memoria/planificacio.md)
- [Metodologia i normes del grup](metodologia.md)
