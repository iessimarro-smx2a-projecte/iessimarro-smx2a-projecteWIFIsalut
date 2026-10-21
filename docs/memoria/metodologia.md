# Metodologia de treball · WiFi SALUT

> **Issue:** #1 · Documentació de l'anàlisi inicial (Fase 5)
> **Responsable:** AlumneC, acordat per tot el grup

## 1. Metodologia

El projecte es desenvolupa amb **Aprenentatge Basat en Projectes (ABP)** en un grup de tres persones. El professorat fa de tutor/a: revisa el tauler Kanban cada setmana, valida les tasques i tanca les issues.

## 2. Rols

| Rol | Membre | Responsabilitats principals | A qui informa |
| --- | --- | --- | --- |
| Coordinador/a tècnic/a | AlumneA | Decisions tècniques, servidor, VLANs i seguretat; comunicació amb el tutor/a | Tutor/a del projecte |
| Tècnic/a d'instal·lació | AlumneB | Plànols, racks, cablejat i muntatge dels punts d'accés | Coordinador/a |
| Tècnic/a de configuració | AlumneC | Pressupost, controlador UniFi, SSIDs, proves i documentació d'usuari | Coordinador/a |

## 3. Normes internes

| Àmbit | Norma acordada |
| --- | --- |
| Reunions de seguiment | Reunió breu setmanal (15 min, dimecres al taller). Es registra al Diari del Grup a GitHub Discussions. |
| Presa de decisions | Consens entre els 3 membres. En cas de desacord, decideix el coordinador/a i queda registrat. |
| Gestió d'incidències | Qualsevol problema tècnic s'obri com a issue amb l'etiqueta `bug` en menys de 24 h. |
| Comunicació interna | Canal principal: GitHub Discussions. Urgent: missatgeria instantània del grup. |
| Commits i freqüència | Mínim 1 commit per membre i setmana, en format *Conventional Commits*. |
| Gestió de conflictes | Si no es resol en 48 h, s'escala al tutor/a. Cap conflicte queda sense registrar. |

## 4. Flux de treball amb Git i GitHub

Cada issue es treballa en una branca pròpia i s'integra a `main` amb una *pull request*.

| Pas | Qui | Què es fa |
| --- | --- | --- |
| 1 | Responsable | Mou la targeta a 🔄 **En progrés** i crea la branca a partir de `main` |
| 2 | Responsable | Fa els commits enllaçats amb la issue (`Refs #n`) |
| 3 | Responsable | Obri la *pull request* cap a `main` i marca la llista de comprovació de la issue |
| 4 | Coordinador/a | Revisa la *pull request* i la fusiona |
| 5 | Responsable | Mou la targeta a 👀 **En revisió** |
| 6 | Professorat | Valida la tasca, deixa un comentari i tanca la issue (✅ **Fet**) |

### Noms de branca

`tipus/número-descripcio-curta`, per exemple:

```
docs/1-analisi-inicial
feat/5-instalacio-racks
feat/7-instalacio-aps
fix/34-aps-sense-poe
```

### Missatges de commit

Format *Conventional Commits*, amb la referència a la issue al peu:

```
git commit -m "feat(aps): muntar els punts d'accés de la planta baixa" -m "Refs #7"
```

| Tipus | Ús |
| --- | --- |
| `feat` | Nou element de la instal·lació o de la configuració |
| `fix` | Correcció d'un error (normalment enllaçat amb una issue `bug`) |
| `docs` | Documentació |
| `chore` | Tasques de manteniment del repositori |

> ⚠ No s'utilitza `Closes #n` ni `Fixes #n`: tancarien la issue automàticament en arribar a `main`, sense la validació del professorat.
