# Planificació del projecte · WiFi SALUT

> **Issue:** #1 · Documentació de l'anàlisi inicial (Fases 3 i 4)
> **Responsable:** AlumneA, amb les aportacions de tot el grup

## 1. Rols del grup

| Rol | Membre | Etiqueta a GitHub |
| --- | --- | --- |
| Coordinador/a tècnic/a | AlumneA | `alumneA` |
| Tècnic/a d'instal·lació | AlumneB | `alumneB` |
| Tècnic/a de configuració | AlumneC | `alumneC` |

Cada issue porta l'etiqueta del membre responsable. Quan la tasca és compartida, porta l'etiqueta de tots dos (o dels tres).

## 2. Fites (*milestones*)

| Fita | Setmanes | Issues |
| --- | --- | --- |
| inici | Prèvia (fases 1 a 3) | #1 |
| Planificació i Anàlisi | S1–S2 | #2, #3, #4 |
| Instal·lació Física | S3 | #5, #6, #7 |
| Configuració de Servidors | S3–S4 | #8, #9, #10 |
| Configuració de Xarxa | S3–S4 | #11 a #15 |
| Proves i Validació | S5 | #16 a #20 |
| Documentació Final i Presentació | S4–S5 | #21 a #25 |

> AlumneA instal·la el servidor Ubuntu (#8) a la setmana 3, en paral·lel al muntatge físic, perquè la configuració de les VLANs (#11) necessita les interfícies VLAN i el DHCP del servidor. Les VLANs han d'estar llestes abans que el controlador UniFi (setmana 4) hi vincule cada SSID.

## 3. Diagrama de Gantt

| Issue · Tasca | Responsable | Prèvia | S1 | S2 | S3 | S4 | S5 |
| --- | --- | :-: | :-: | :-: | :-: | :-: | :-: |
| #1 · Documentació de l'anàlisi inicial | AlumneA | ██ |  |  |  |  |  |
| #2 · Plànols de plantes i topologia de xarxa | AlumneB |  | ██ | ██ |  |  |  |
| #3 · Pressupost i llistat d'equipament | AlumneC |  | ██ |  |  |  |  |
| #4 · Disseny de VLANs i esquema d'adreçament IP | AlumneA |  | ██ | ██ |  |  |  |
| #5 · Instal·lació física dels racks | AlumneB |  |  |  | ██ |  |  |
| #6 · Cablejat estructurat Cat6 | AlumneB |  |  |  | ██ |  |  |
| #7 · Instal·lació física dels punts d'accés | AlumneB |  |  |  | ██ |  |  |
| #8 · Instal·lació del servidor Ubuntu | AlumneA |  |  |  | ██ |  |  |
| #9 · Instal·lació del controlador UniFi | AlumneC |  |  |  |  | ██ |  |
| #10 · Configuració del servidor FreeRADIUS | AlumneA |  |  |  |  | ██ |  |
| #11 · Configuració de VLANs | AlumneA |  |  |  | ██ | ██ |  |
| #12 · Configuració SSID Admin | AlumneC |  |  |  |  | ██ |  |
| #13 · Configuració SSID Salut | AlumneC |  |  |  |  | ██ |  |
| #14 · Configuració SSID Convidats | AlumneC |  |  |  |  | ██ |  |
| #15 · Configuració de regles de tallafocs | AlumneA |  |  |  |  | ██ |  |
| #16 · Proves de connectivitat de xarxa | AlumneA + AlumneC |  |  |  |  |  | ██ |
| #17 · Proves d'autenticació RADIUS | AlumneA |  |  |  |  |  | ██ |
| #18 · Proves del portal de convidats | AlumneC |  |  |  |  |  | ██ |
| #19 · Validació de seguretat | AlumneA + AlumneC |  |  |  |  |  | ██ |
| #20 · Proves de rendiment | AlumneC |  |  |  |  |  | ██ |
| #21 · Documentació memòria final del projecte | Tots |  |  |  |  | ██ | ██ |
| #22 · Creació del manual d'usuari | AlumneC |  |  |  |  |  | ██ |
| #23 · Manual tècnic d'administració | AlumneA |  |  |  |  |  | ██ |
| #24 · Preparació presentació final | Tots |  |  |  |  |  | ██ |
| #25 · Scripts de còpia de seguretat de configuració | AlumneA |  |  |  |  |  | ██ |

Llegenda: ██ = setmana activa. Les dates concretes de cada setmana són les de la data límit de cada fita.

## 4. Tauler Kanban (GitHub Projects)

| Columna | Significat | Qui la mou |
| --- | --- | --- |
| 📋 Per fer | Issue creada, encara no iniciada | Automàtic en afegir-la al tauler |
| 🔄 En progrés | Tasca en curs | El membre responsable, quan comença |
| 👀 En revisió | Tasca acabada i *pull request* fusionada | El membre responsable, quan la lliura |
| ✅ Fet | Tasca validada i issue tancada | El professorat, en validar-la |

## 5. Fitxes d'activitat (Annex B)

Cada tasca té la seua fitxa amb els 8 camps obligatoris. El número d'activitat coincideix amb el número de la issue.

### A1 · Documentació de l'anàlisi inicial

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Documentació de l'anàlisi inicial · issue #1 |
| Per a què? (RA) | MP02-RA2 · PI-RA1 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | docs/analisi-inicial.md, docs/document-repte.md i README.md |
| Instruccions | Visitar el centre → recollir l'estat actual → redactar requeriments → completar l'Annex A → actualitzar el README |
| Recursos | Visita al centre, plantilla Annex A |
| Quan? (Durada) | 4 h · Prèvia |
| Com s'avaluarà? | Rúbrica de documentació |

### A2 · Plànols de plantes i topologia de xarxa

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Plànols de plantes i topologia de xarxa · issue #2 |
| Per a què? (RA) | MP02-RA2 |
| Com? | Individual · Responsable: AlumneB |
| Suport/format | planols/*.pdf i docs/topologia-xarxa.md |
| Instruccions | Obtindre plànols → marcar 2 APs per planta → traçar rutes de cablejat → ubicar racks → dibuixar la topologia |
| Recursos | Plànols del centre, Python/LibreOffice Draw, Packet Tracer |
| Quan? (Durada) | 6 h · S1, S2 |
| Com s'avaluarà? | Rúbrica MP02 (ubicació d'APs i rutes) |

### A3 · Pressupost i llistat d'equipament

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Pressupost i llistat d'equipament · issue #3 |
| Per a què? (RA) | MP01-RA1 · PI-RA2 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `pressupost/pressupost-detallat.xlsx` |
| Instruccions | Llistar equips → consultar preus de dos proveïdors → calcular IVA i total → justificar l'elecció |
| Recursos | Catàlegs de distribuïdors, full de càlcul |
| Quan? (Durada) | 4 h · S1 |
| Com s'avaluarà? | Rúbrica de pressupost (justificació i càlcul) |

### A4 · Disseny de VLANs i esquema d'adreçament IP

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Disseny de VLANs i esquema d'adreçament IP · issue #4 |
| Per a què? (RA) | MP02-RA3 · MP06-RA3 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `configuracio/vlans/disseny-vlans.md` |
| Instruccions | Definir VLANs → assignar subxarxes → reservar IPs fixes → definir regles entre VLANs |
| Recursos | Packet Tracer, calculadora IP |
| Quan? (Durada) | 4 h · S1, S2 |
| Com s'avaluarà? | Rúbrica MP02 (coherència del pla IP) |

### A5 · Instal·lació física dels racks

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Instal·lació física dels racks · issue #5 |
| Per a què? (RA) | MP01-RA3 |
| Com? | Grup, liderat per AlumneB · Responsable: AlumneB |
| Suport/format | docs/instalacio-fisica.md amb fotos |
| Instruccions | Marcar ancoratges → fixar racks → muntar patch panel, switch, SAI i servidor → organitzar cables → fotografiar |
| Recursos | Rack 12U, 2 racks 6U, tacs, cargols, nivell, trepant |
| Quan? (Durada) | 5 h · S3 |
| Com s'avaluarà? | Observació directa + rúbrica MP01 |

### A6 · Cablejat estructurat Cat6

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Cablejat estructurat Cat6 · issue #6 |
| Per a què? (RA) | MP02-RA2 |
| Com? | Grup, liderat per AlumneB · Responsable: AlumneB |
| Suport/format | docs/documentacio-cablejat.md i mapa de cables |
| Instruccions | Estendre cables → punxar al patch panel → crimpar a l'extrem de l'AP → etiquetar → comprovar continuïtat |
| Recursos | Bobina Cat6 LSZH, canaleta, crimpadora, eina d'impacte, comprovador |
| Quan? (Durada) | 8 h · S3 |
| Com s'avaluarà? | Observació directa + informe de proves |

### A7 · Instal·lació física dels punts d'accés

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Instal·lació física dels punts d'accés · issue #7 |
| Per a què? (RA) | MP02-RA3 |
| Com? | Parelles (AlumneB + AlumneC) · Responsable: AlumneB |
| Suport/format | docs/instalacio-aps.md (llista de verificació) i fotos |
| Instruccions | Fixar suports → muntar APs → connectar al switch PoE → verificar LED i consum PoE → descobriment inicial |
| Recursos | 6 APs UniFi 6 Lite, escala, trepant, tacs |
| Quan? (Durada) | 4 h · S3 |
| Com s'avaluarà? | Observació directa + llista de verificació |

### A8 · Instal·lació del servidor Ubuntu

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Instal·lació del servidor Ubuntu · issue #8 |
| Per a què? (RA) | MP05-RA1 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `docs/instalacio-servidor.md` |
| Instruccions | Instal·lar SO → xarxa → actualitzacions → SSH → ufw |
| Recursos | Servidor, ISO Ubuntu Server 24.04 LTS |
| Quan? (Durada) | 3 h · S3 |
| Com s'avaluarà? | Rúbrica MP05 |

### A9 · Instal·lació del controlador UniFi

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Instal·lació del controlador UniFi · issue #9 |
| Per a què? (RA) | MP05-RA2 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `configuracio/unifi-controller/setup.md` |
| Instruccions | Instal·lar l'aplicació → configuració inicial → adoptar APs → actualitzar firmware |
| Recursos | Servidor Ubuntu, UniFi Network Application |
| Quan? (Durada) | 3 h · S4 |
| Com s'avaluarà? | Rúbrica MP05 |

### A10 · Configuració del servidor FreeRADIUS

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Configuració del servidor FreeRADIUS · issue #10 |
| Per a què? (RA) | MP06-RA3 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `configuracio/radius/instalacio-radius.md` |
| Instruccions | Instal·lar → clients.conf → usuaris → EAP-PEAP → radtest |
| Recursos | Servidor Ubuntu, freeradius, freeradius-utils |
| Quan? (Durada) | 3 h · S4 |
| Com s'avaluarà? | Rúbrica MP06 |

### A11 · Configuració de VLANs

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Configuració de VLANs · issue #11 |
| Per a què? (RA) | MP02-RA3 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `configuracio/vlans/config-vlans.md` |
| Instruccions | VLANs al switch → interfícies VLAN al servidor → DHCP per VLAN → encaminament |
| Recursos | Switch gestionable, servidor |
| Quan? (Durada) | 4 h · S3, S4 |
| Com s'avaluarà? | Rúbrica MP02 |

### A12 · Configuració SSID Admin

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Configuració SSID Admin · issue #12 |
| Per a què? (RA) | MP06-RA3 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `configuracio/ssids/admin.md` |
| Instruccions | Crear SSID → VLAN 10 → WPA2-Enterprise contra RADIUS |
| Recursos | UniFi Controller, FreeRADIUS |
| Quan? (Durada) | 2 h · S4 |
| Com s'avaluarà? | Rúbrica MP06 |

### A13 · Configuració SSID Salut

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Configuració SSID Salut · issue #13 |
| Per a què? (RA) | MP02-RA3 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `configuracio/ssids/salut.md` |
| Instruccions | Crear SSID → VLAN 20 → WPA2/WPA3-Personal |
| Recursos | UniFi Controller |
| Quan? (Durada) | 1 h · S4 |
| Com s'avaluarà? | Rúbrica MP02 |

### A14 · Configuració SSID Convidats

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Configuració SSID Convidats · issue #14 |
| Per a què? (RA) | MP06-RA3 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `configuracio/ssids/convidats.md` |
| Instruccions | Crear SSID → VLAN 30 → portal captiu i límits |
| Recursos | UniFi Controller |
| Quan? (Durada) | 2 h · S4 |
| Com s'avaluarà? | Rúbrica MP06 |

### A15 · Configuració de regles de tallafocs

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Configuració de regles de tallafocs · issue #15 |
| Per a què? (RA) | MP06-RA3 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `configuracio/tallafocs.md` |
| Instruccions | Política per defecte → regles entre VLANs → proves |
| Recursos | Servidor Ubuntu (nftables/ufw) |
| Quan? (Durada) | 3 h · S4 |
| Com s'avaluarà? | Rúbrica MP06 |

### A16 · Proves de connectivitat de xarxa

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Proves de connectivitat de xarxa · issue #16 |
| Per a què? (RA) | MP02-RA4 |
| Com? | Parelles · Responsable: AlumneA + AlumneC |
| Suport/format | `proves/resultats-proves.md` |
| Instruccions | Connectar a cada SSID → IP → passarel·la → internet |
| Recursos | Portàtil, mòbil, ping, iperf3 |
| Quan? (Durada) | 2 h · S5 |
| Com s'avaluarà? | Informe de proves |

### A17 · Proves d'autenticació RADIUS

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Proves d'autenticació RADIUS · issue #17 |
| Per a què? (RA) | MP06-RA3 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `proves/resultats-proves.md` |
| Instruccions | Credencials correctes i incorrectes → registres |
| Recursos | radtest, portàtil |
| Quan? (Durada) | 1 h · S5 |
| Com s'avaluarà? | Informe de proves |

### A18 · Proves del portal de convidats

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Proves del portal de convidats · issue #18 |
| Per a què? (RA) | MP06-RA3 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `proves/resultats-proves.md` |
| Instruccions | Accés → límit de temps → límit de velocitat |
| Recursos | Mòbil |
| Quan? (Durada) | 1 h · S5 |
| Com s'avaluarà? | Informe de proves |

### A19 · Validació de seguretat

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Validació de seguretat · issue #19 |
| Per a què? (RA) | MP06-RA3 |
| Com? | Parelles · Responsable: AlumneA + AlumneC |
| Suport/format | `proves/resultats-proves.md` |
| Instruccions | Aïllament entre VLANs → aïllament de clients → accés a gestió |
| Recursos | nmap, ping |
| Quan? (Durada) | 2 h · S5 |
| Com s'avaluarà? | Informe de proves |

### A20 · Proves de rendiment

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Proves de rendiment · issue #20 |
| Per a què? (RA) | MP02-RA4 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `proves/resultats-proves.md` |
| Instruccions | Velocitat per planta → mapa de cobertura |
| Recursos | iperf3, WiFiman |
| Quan? (Durada) | 2 h · S5 |
| Com s'avaluarà? | Informe de proves |

### A21 · Documentació memòria final del projecte

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Documentació memòria final del projecte · issue #21 |
| Per a què? (RA) | PI-RA5 |
| Com? | Grup · Responsable: Tots |
| Suport/format | `docs/memoria/memoria.md` |
| Instruccions | Recollir evidències → redactar → revisar |
| Recursos | Tot el repositori |
| Quan? (Durada) | 6 h · S4, S5 |
| Com s'avaluarà? | Rúbrica de memòria |

### A22 · Creació del manual d'usuari

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Creació del manual d'usuari · issue #22 |
| Per a què? (RA) | PI-RA5 |
| Com? | Individual · Responsable: AlumneC |
| Suport/format | `docs/memoria/manual-usuari.md` |
| Instruccions | Connexió a cada SSID → problemes freqüents |
| Recursos | Captures |
| Quan? (Durada) | 2 h · S5 |
| Com s'avaluarà? | Rúbrica de documentació |

### A23 · Manual tècnic d'administració

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Manual tècnic d'administració · issue #23 |
| Per a què? (RA) | PI-RA5 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `docs/memoria/manual-tecnic.md` |
| Instruccions | Accessos → procediments → manteniment |
| Recursos | Configuracions |
| Quan? (Durada) | 3 h · S5 |
| Com s'avaluarà? | Rúbrica de documentació |

### A24 · Preparació presentació final

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Preparació presentació final · issue #24 |
| Per a què? (RA) | PI-RA5 |
| Com? | Grup · Responsable: Tots |
| Suport/format | `docs/presentacio/presentacio.md` |
| Instruccions | Guió → diapositives → assaig |
| Recursos | Repositori, tauler Kanban |
| Quan? (Durada) | 3 h · S5 |
| Com s'avaluarà? | Rúbrica de comunicació |

### A25 · Scripts de còpia de seguretat de configuració

| Camp | Contingut |
| --- | --- |
| Tasca (Què?) | Scripts de còpia de seguretat de configuració · issue #25 |
| Per a què? (RA) | MP06-RA1 |
| Com? | Individual · Responsable: AlumneA |
| Suport/format | `scripts/backup/` |
| Instruccions | Script → programació → prova de restauració |
| Recursos | Bash, cron |
| Quan? (Durada) | 2 h · S5 |
| Com s'avaluarà? | Rúbrica MP06 |
