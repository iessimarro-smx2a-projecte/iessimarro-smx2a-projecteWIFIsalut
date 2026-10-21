# Instal·lació física dels racks · WiFi SALUT

> **Issue:** #5 · Instal·lació Física dels Racks
> **Responsable:** AlumneB (tècnic/a d'instal·lació), amb el suport d'AlumneA i AlumneC
> **Fita:** Instal·lació Física · Setmana 3

## 1. Rack principal RP-P1 (sala tècnica, planta primera)

Armari mural 19" de 12U (600 × 450 mm), fixat a la paret amb 4 tacs M8 a 1,80 m de la part superior.

| U | Element | Observacions |
| :-: | --- | --- |
| 12 | Patch panel Cat6 24 ports | Arribada dels 6 enllaços d'AP i dels troncals |
| 11 | Organitzador de cables 1U | |
| 10 | Switch UniFi USW-24-PoE | Ports 1–16 amb PoE+ |
| 9 | Organitzador de cables 1U | |
| 8 – 5 | Servidor (safata fixa) | Servidor torre en posició horitzontal sobre safata |
| 4 | Lliure | Reserva per a ampliacions |
| 3 – 2 | SAI 1500 VA | Al fons del rack pel pes |
| 1 | Regleta PDU 8 preses | Connectada a la sortida del SAI |

### Passos realitzats

1. Marcar i trepar els ancoratges amb el nivell; comprovar que la paret no té instal·lacions encastades.
2. Fixar l'armari a la paret i connectar-ne la presa de terra.
3. Muntar el SAI i la regleta PDU a la part inferior.
4. Muntar el servidor sobre la safata, el switch i el patch panel amb femelles caixa i cargols M6.
5. Col·locar els organitzadors de cables entre el patch panel i el switch.
6. Connectar l'alimentació: SAI → PDU → switch i servidor.

## 2. Racks secundaris RS-PB i RS-P2

Armaris murals 19" de 6U, a la mateixa vertical que el rack principal (magatzem de la planta baixa i arxiu de la planta segona), al costat del patinet vertical.

| U | Element |
| :-: | --- |
| 6 | Patch panel Cat6 12 ports |
| 5 | Organitzador de cables 1U |
| 4 – 1 | Reserva per a un switch de planta en futures ampliacions |

## 3. Gestió de cables

- Cables d'alimentació per la part esquerra del rack i cables de dades per la dreta.
- Latiguillos d'1 m entre el patch panel i el switch, sense tensió i agrupats amb brides de velcro.
- Etiquetatge segons el format definit a la issue #6.

## 4. Comprovació final

| Comprovació | Resultat |
| --- | :-: |
| Racks anivellats i fixats a la paret | ✅ |
| Presa de terra connectada als tres racks | ✅ |
| Switch i servidor arrenquen alimentats des del SAI | ✅ |
| Prova de tall elèctric: el SAI manté els equips en marxa | ✅ |
| Porta del rack principal tancada amb clau (la custodia el coordinador/a) | ✅ |

## 5. Evidències fotogràfiques

Les fotografies s'adjunten com a comentari a la issue #5 i es pugen a `docs/img/` en la versió final de la memòria.

| Foto | Contingut |
| --- | --- |
| rack-principal-frontal.jpg | Vista frontal del RP-P1 amb tots els equips muntats |
| rack-principal-cables.jpg | Detall de la gestió de cables entre el patch panel i el switch |
| rack-secundari-pb.jpg | Rack RS-PB fixat a la paret del magatzem |
| rack-secundari-p2.jpg | Rack RS-P2 fixat a la paret de l'arxiu |
