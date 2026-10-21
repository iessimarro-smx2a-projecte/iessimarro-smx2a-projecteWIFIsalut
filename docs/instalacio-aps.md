# Instal·lació física dels punts d'accés · WiFi SALUT

> **Issue:** #7 · Instal·lació Física dels Punts d'Accés
> **Responsable:** AlumneB (tècnic/a d'instal·lació), amb el suport d'AlumneC
> **Fita:** Instal·lació Física · Setmana 3

## 1. Material

- 6 punts d'accés **UniFi 6 Lite** amb el seu suport de sostre.
- Escala, trepant, tacs i cargols del kit de l'AP.
- Latiguillos Cat6 d'1 m al rack principal.
- Portàtil amb l'aplicació WiFiman i `arp-scan` per al descobriment inicial.

## 2. Ubicació i adreçament previst

| AP | Planta | Ubicació (plànol #2) | Enllaç | Port del switch | IP de gestió prevista (#4) |
| --- | --- | --- | --- | :-: | --- |
| AP-PB-01 | Baixa | Passadís de recepció | PP01 | 1 | 192.168.99.21 |
| AP-PB-02 | Baixa | Davant d'urgències | PP02 | 2 | 192.168.99.22 |
| AP-P1-01 | Primera | Passadís de consultes | PP03 | 3 | 192.168.99.23 |
| AP-P1-02 | Primera | Davant d'infermeria | PP04 | 4 | 192.168.99.24 |
| AP-P2-01 | Segona | Passadís d'administració | PP05 | 5 | 192.168.99.25 |
| AP-P2-02 | Segona | Davant de la sala de reunions | PP06 | 6 | 192.168.99.26 |

## 3. Passos realitzats

1. Marcar la posició de cada AP al sostre del passadís segons el plànol de la issue #2.
2. Fixar el suport de sostre amb tacs i passar el cable per l'orifici central.
3. Connectar el cable a l'AP i encaixar-lo al suport girant-lo fins que fa clic.
4. Al rack principal, connectar cada port del patch panel al port del switch indicat al mapa de cables (#6).
5. Comprovar que cada AP s'encén i observar el LED.

## 4. Llista de verificació

| AP | Muntat | LED encés | Consum PoE (W) | Descobert |
| --- | :-: | :-: | :-: | :-: |
| AP-PB-01 | ✅ | ✅ | 9,8 | ✅ |
| AP-PB-02 | ✅ | ✅ | 10,1 | ✅ |
| AP-P1-01 | ✅ | ✅ | 9,6 | ✅ |
| AP-P1-02 | ✅ | ✅ | 9,9 | ✅ |
| AP-P2-01 | ✅ | ✅ | 10,0 | ✅ |
| AP-P2-02 | ✅ | ✅ | 9,7 | ✅ |

Consum PoE total: **59,1 W** de 95 W disponibles (62 %), per davall del màxim calculat a la issue #3 (72 W).

## 5. Incidències

| Issue | Problema | Solució |
| --- | --- | --- |
| #34 (`bug`) | AP-P2-01 i AP-P2-02 no s'encenien: estaven connectats als ports 17 i 18, que no tenen PoE. | Connectar-los als ports 5 i 6 i corregir el mapa de cables (#6). |

## 6. Descobriment inicial

Amb un portàtil connectat al switch, abans d'instal·lar el controlador UniFi (#9):

```bash
sudo arp-scan --localnet | grep -i ubiquiti
```

| Resultat | Interpretació |
| --- | --- |
| Es detecten **6 adreces MAC** amb el fabricant Ubiquiti | Els sis APs reben alimentació i responen a la xarxa |
| LED **blanc fix** als sis APs | Estat «pendent d'adopció»: esperen el controlador |

L'adopció dels APs i l'assignació de les IPs de gestió (192.168.99.21 a .26) es fan a la issue #9.

## 7. Evidències fotogràfiques

Les fotografies s'adjunten com a comentari a la issue #7 i es pugen a `docs/img/` en la versió final de la memòria.

| Foto | Contingut |
| --- | --- |
| ap-pb-01.jpg … ap-p2-02.jpg | Cada AP muntat al sostre, amb l'etiqueta del cable visible |
| switch-poe.jpg | Ports 1 a 6 del switch amb el LED de PoE encés |
| wifiman-descobriment.png | Captura del descobriment dels sis APs |
