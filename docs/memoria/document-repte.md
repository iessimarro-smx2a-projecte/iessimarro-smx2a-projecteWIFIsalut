# Document de repte (Annex A) · Projecte WiFi SALUT

> **Issue:** #1 · Documentació de l'anàlisi inicial
> **Responsable:** AlumneA · Revisat per tot el grup

| Camp | Contingut |
| --- | --- |
| **Títol del projecte** | WiFi SALUT: xarxa sense fil segura i segmentada per a un centre de salut |
| **Grup i membres** | AlumneA: coordinador/a tècnic/a · AlumneB: tècnic/a d'instal·lació · AlumneC: tècnic/a de configuració |
| **Centre i curs** | IES Simarro · 2n SMX A · Curs 2026-2027 |
| **Context i situació inicial** | El centre de salut de la comarca (tres plantes) no té una xarxa WiFi corporativa. Hi ha un únic punt d'accés domèstic a recepció, amb clau compartida i sense separar el personal de les persones usuàries. Això suposa un risc per a la confidencialitat de les dades sanitàries. |
| **Repte proposat** | Dissenyar i implementar una xarxa WiFi segura per al centre de salut, amb tres xarxes separades (Admin, Salut i Convidats), gestió centralitzada dels punts d'accés i autenticació individual del personal administratiu. |
| **Objectiu general** | Dotar el centre d'una xarxa sense fil amb cobertura completa, segmentada per VLANs i protegida amb autenticació 802.1X i tallafocs. |
| **Objectius específics** | 1. Analitzar l'edifici i dissenyar la ubicació dels 6 punts d'accés. 2. Elaborar el pressupost i seleccionar els equips. 3. Instal·lar els racks, el cablejat Cat6 i els punts d'accés. 4. Configurar el servidor Ubuntu amb UniFi Controller, FreeRADIUS i DHCP. 5. Configurar les VLANs, els SSIDs i el tallafocs. 6. Verificar la connectivitat i la seguretat, i documentar tot el procés. |
| **Mòduls professionals implicats** | MP01 — MP02 — MP05 — MP06 |
| **RA associats per mòdul** | MP01-RA3: Munta equips en bastidor (rack, switch, servidor). MP02-RA2: Desplega el cablejat estructurat d'una xarxa local. MP02-RA3: Configura els elements d'interconnexió (switch, VLANs, punts d'accés). MP05-RA2: Instal·la i configura serveis de xarxa (DHCP, controlador UniFi). MP06-RA3: Implanta tècniques d'autenticació i control d'accés (FreeRADIUS, 802.1X). |
| **Criteris de qualitat del repte** | Proximitat/rellevància: Sí · Treball en equip: Sí · Creativitat: Sí · Connexió professional: Sí |
| **Requeriments tècnics** | 6 APs UniFi 6 Lite, switch UniFi de 24 ports PoE, servidor amb Ubuntu Server 24.04 LTS, 1 rack principal de 12U i 2 racks secundaris de 6U, cable Cat6 LSZH, patch panels, SAI. |
| **Limitacions o restriccions** | Cinc setmanes d'execució; pressupost ajustat; el centre ha de continuar atenent pacients durant la instal·lació; no es poden fer regates a les parets. |
| **Validació del professorat** | Data: _(a completar pel professorat)_ · Valoració: _Aprovat / Aprovat amb canvis / No aprovat_ · Observacions: |
