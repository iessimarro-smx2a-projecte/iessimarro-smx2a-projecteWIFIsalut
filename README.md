# **_Projecte Intermodular WIFI SALUT_**

Exemple de repositori Github per al projecte Intermodular de 2n SMX - WIFI SALUT

## Descripció del repte

Disseny i implementació d'una **xarxa WiFi segura i segmentada** per a un centre de salut de tres plantes: 6 punts d'accés UniFi 6 Lite gestionats des d'un controlador centralitzat, tres xarxes sense fil separades per VLANs (**Admin**, **Salut** i **Convidats**) i autenticació 802.1X del personal administratiu contra un servidor FreeRADIUS.

- 📄 [Anàlisi inicial](docs/analisi-inicial.md)
- 🎯 [Document de repte (Annex A)](docs/memoria/document-repte.md)
- 🗓️ [Planificació, cronograma i fitxes d'activitat](docs/memoria/planificacio.md)
- 🤝 [Metodologia i normes del grup](docs/memoria/metodologia.md)

## Membres i rols

| Membre | Rol | Etiqueta |
| --- | --- | --- |
| AlumneA | Coordinador/a tècnic/a | `alumneA` |
| AlumneB | Tècnic/a d'instal·lació | `alumneB` |
| AlumneC | Tècnic/a de configuració | `alumneC` |

> Repositori model per a l'alumnat de 2n SMX (IES Simarro). Els membres són rols simulats.

## Estat del projecte

| Fita | Issues | Estat |
| --- | --- | --- |
| inici | #1 | 🔄 En progrés |
| Planificació i Anàlisi | #2, #3, #4 | 📋 Per fer |
| Instal·lació Física | #5, #6, #7 | 📋 Per fer |
| Configuració de Servidors | #8, #9, #10 | 📋 Per fer |
| Configuració de Xarxa | #11 a #15 | 📋 Per fer |
| Proves i Validació | #16 a #20 | 📋 Per fer |
| Documentació Final i Presentació | #21 a #25 | 📋 Per fer |

## Estructura del repositori del projecte WIFI SALUT

```
wifi-salut-implementation/
├── README.md
├── docs/
│   ├── memoria/
│   │   ├── memoria.md
│   │   ├── planificacio.md
│   │   ├── manual-usuari.md
│   ├── presentacio/
│   │   ├── presentacio.md
├── planols/
│   ├── planta-baixa.pdf
│   ├── planta-primera.pdf
│   └── planta-segona.pdf
├── configuracio/
│   ├── vlans/
│   ├── radius/
│   ├── unifi-controller/
│   └── ssids/
├── scripts/
│   └── backup/
├── pressupost/
│   └── pressupost-detallat.xlsx
└── proves/
    └── resultats-proves.md
```

### On es desa cada lliurable

Els lliurables de cada issue es desen dins d'aquesta estructura, a la ruta que indica l'apartat **Eixida** de la issue:

| Issue | Lliurable | Ruta |
| --- | --- | --- |
| #1 | Anàlisi inicial | `docs/analisi-inicial.md` |
| #1 | Document de repte (Annex A), planificació i metodologia | `docs/memoria/` |
| #2 | Plànols i topologia de xarxa | `planols/` |
| #3 | Pressupost i justificació | `pressupost/` |
| #4 | Disseny de VLANs | `configuracio/vlans/` |
| #5 | Instal·lació dels racks | `docs/instalacio-fisica.md` |
| #6 | Documentació del cablejat | `docs/documentacio-cablejat.md` |
| #7 | Instal·lació dels punts d'accés | `docs/instalacio-aps.md` |

## Elements del projecte a GITHUB Projects

### 1. Incidències (_Issues_)
Les **Incidències** són les tasques individuals del projecte. Són una eina de creació i seguiment de tasques relacionades amb un projecte.
Cada incidència es representa com un **"issue"** i contindrà un conjunt variable d'elements com poden ser: la descripció de la tasca, el temps d'execució, els membres assignats i l'estat actual.

Son configurables via camps editables (_custom fields_) visibles des de les propietats del projecte.

### 2. Etiquetes (_Labels_)
Les etiquetes permeten categoritzar les incidències per a facilitar-ne la gestió. Les incidències poden classificar-se per diferents categories.

### 3. Fites (_Milestones_)
Les fites permeten organitzar les incidències per complir un objectiu específic. Són un mecanisme per organitzar **Incidències** dins d'un repositori. 

S'utilitzen per **definir objectius específics en el desenvolupament del projecte**.

Cada **fita** conté la següent informació:
- Títol
- Descripció
- Data de venciment (Opcional)
- Percentatge de progrés, calculat respecte de les incidències obertes i tancades.
