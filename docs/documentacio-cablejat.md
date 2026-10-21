# Documentació del cablejat estructurat Cat6 · WiFi SALUT

> **Issue:** #6 · Cablejat Estructurat Cat6
> **Responsable:** AlumneB (tècnic/a d'instal·lació), amb el suport d'AlumneC
> **Fita:** Instal·lació Física · Setmana 3

## 1. Material i norma

- Cable **Cat6 U/UTP LSZH** (bobina de 305 m).
- Terminació segons la norma **T568B** als dos extrems.
- Al rack principal el cable es punxa al patch panel amb l'eina d'impacte; a l'extrem de l'AP es crimpa un connector RJ45 Cat6.
- Longitud màxima de l'enllaç permanent: 90 m (cap enllaç supera els 30 m).

## 2. Format d'etiquetatge

Cada cable porta la mateixa etiqueta als dos extrems, a 10 cm del connector:

```
<rack>-<port patch panel> / <destinació>
Exemple:  RP-P1-PP03 / AP-P1-01
```

## 3. Mapa de cables

| Etiqueta | Patch panel RP-P1 | Destinació | Planta | Longitud | Port del switch |
| --- | :-: | --- | --- | :-: | :-: |
| RP-P1-PP01 / AP-PB-01 | 1 | AP-PB-01 | Baixa | 25 m | 1 |
| RP-P1-PP02 / AP-PB-02 | 2 | AP-PB-02 | Baixa | 22 m | 2 |
| RP-P1-PP03 / AP-P1-01 | 3 | AP-P1-01 | Primera | 21 m | 3 |
| RP-P1-PP04 / AP-P1-02 | 4 | AP-P1-02 | Primera | 18 m | 4 |
| RP-P1-PP05 / AP-P2-01 | 5 | AP-P2-01 | Segona | 25 m | 5 |
| RP-P1-PP06 / AP-P2-02 | 6 | AP-P2-02 | Segona | 22 m | 6 |
| RP-P1-PP20 / RS-PB-T1 | 20 | Troncal rack RS-PB | Baixa | 10 m | 20 |
| RP-P1-PP21 / RS-PB-T2 | 21 | Troncal rack RS-PB | Baixa | 10 m | — (reserva) |
| RP-P1-PP22 / RS-P2-T1 | 22 | Troncal rack RS-P2 | Segona | 10 m | 21 |
| RP-P1-PP23 / RS-P2-T2 | 23 | Troncal rack RS-P2 | Segona | 10 m | — (reserva) |

Longitud total instal·lada: **174 m**.

> ⚠ Els APs s'han de connectar sempre als **ports 1 a 16** del switch, que són els únics amb PoE+. Correcció aplicada a la issue #34: AP-P2-01 i AP-P2-02 estaven assignats als ports 17 i 18, sense PoE.

## 4. Passos realitzats

1. Estendre els cables des del rack principal pel patinet vertical fins a cada planta.
2. Recórrer el fals sostre del passadís fins a la vertical de cada AP, deixant 1,5 m de coca a l'extrem.
3. Fixar els cables a la safata amb brides cada 50 cm, sense doblegar-los amb un radi inferior a 4 cm.
4. Punxar cada cable al patch panel (T568B) i crimpar el connector RJ45 a l'extrem de l'AP.
5. Etiquetar els dos extrems.
6. Comprovar la continuïtat de cada enllaç amb el comprovador de cable.

## 5. Prova de continuïtat

| Enllaç | Parells 1-2 | Parells 3-6 | Parells 4-5 | Parells 7-8 | Resultat |
| --- | :-: | :-: | :-: | :-: | :-: |
| PP01 → AP-PB-01 | ✅ | ✅ | ✅ | ✅ | Correcte |
| PP02 → AP-PB-02 | ✅ | ✅ | ✅ | ✅ | Correcte |
| PP03 → AP-P1-01 | ✅ | ✅ | ✅ | ✅ | Correcte |
| PP04 → AP-P1-02 | ✅ | ✅ | ✅ | ✅ | Correcte |
| PP05 → AP-P2-01 | ✅ | ✅ | ✅ | ✅ | Correcte |
| PP06 → AP-P2-02 | ✅ | ✅ | ✅ | ✅ | Correcte |
| PP20 – PP23 (troncals) | ✅ | ✅ | ✅ | ✅ | Correcte |


Tots els enllaços superen la prova de continuïtat i el mapa de fils és correcte.
