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
| AP-P2-01 | Segona | Passadís d'administració | PP05 | 17 | 192.168.99.25 |
| AP-P2-02 | Segona | Davant de la sala de reunions | PP06 | 18 | 192.168.99.26 |

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
| AP-P2-01 | ✅ | ❌ | — | ❌ |
| AP-P2-02 | ✅ | ❌ | — | ❌ |
