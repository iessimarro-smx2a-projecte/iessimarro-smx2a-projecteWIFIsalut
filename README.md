# **_Projecte Intermodular WIFI SALUT_**

Exemple de repositori Github per al projecte Intermodular de 2n SMX - WIFI SALUT

## Descripció del repte

Disseny i implementació d'una **xarxa WiFi segura i segmentada** per a un centre de salut de tres plantes: 6 punts d'accés UniFi 6 Lite gestionats des d'un controlador centralitzat, tres xarxes sense fil separades per VLANs (**Admin**, **Salut** i **Convidats**) i autenticació 802.1X del personal administratiu contra un servidor FreeRADIUS.

- 📄 [Anàlisi inicial](docs/analisi-inicial.md)
- 🎯 [Document de repte (Annex A)](docs/document-repte.md)
- 🗓️ [Planificació, cronograma i fitxes d'activitat](docs/memoria/planificacio.md)
- 🤝 [Metodologia i normes del grup](docs/metodologia.md)

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
iessimarro-smx2a-projectewifisalut/
├── README.md
├── docs/
│   ├── analisi-inicial.md            (#1)
│   ├── document-repte.md             (#1)
│   ├── metodologia.md                (#1)
│   ├── topologia-xarxa.md            (#2)
│   ├── instalacio-fisica.md          (#5)
│   ├── documentacio-cablejat.md      (#6)
│   ├── instalacio-aps.md             (#7)
│   ├── memoria/
│   │   ├── planificacio.md           (#1)
│   │   ├── memoria.md                (#21)
│   │   ├── manual-usuari.md          (#22)
│   │   └── manual-tecnic.md          (#23)
│   └── presentacio/
│       └── presentacio.md            (#24)
├── planols/                          (#2)
│   ├── planta-baixa.pdf
│   ├── planta-primera.pdf
│   └── planta-segona.pdf
├── configuracio/
│   ├── vlans/                        (#4, #11)
│   ├── radius/                       (#10)
│   ├── unifi-controller/             (#9)
│   └── ssids/                        (#12, #13, #14)
├── scripts/
│   └── backup/                       (#25)
├── pressupost/
│   └── pressupost-detallat.xlsx      (#3)
└── proves/
    └── resultats-proves.md           (#16 a #20)
```

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
