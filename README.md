# Voss HPK Wiki — Innhold & Git Storage

Dette repositoriet (`vosshpk/wiki`) inneholder alle Markdown-artikler, guider og filer for **Voss Henge- og Paragliderklubb sin Wiki**.

Klubbens wiki kjører på **Wiki.js v2** i Google Cloud (Cloud Run + PostgreSQL 16), og er koblet direkte til dette repositoriet via Wiki.js sin innebygde **Git Storage**-modul.

---

## 🔄 Hvordan synkronisering fungerer

1. **Redigering i nettleseren (Wiki.js):**
   * Når en godkjent bruker redigerer eller oppretter en side i nettleseren, oppretter Wiki.js automatisk en Git-commit og pusher endringen til `main`-branchen i dette repositoriet.
2. **Redigering direkte i GitHub:**
   * Du kan også gjøre endringer direkte i GitHub (via Pull Request eller direkte commit).
   * Wiki.js trekker (puller) regelmessig nye commits fra GitHub og oppdaterer innholdet på nettsiden automatisk.

---

## 📁 Struktur

```text
├── home.md                 # Hovedside / forside i wikien
├── flysteder/              # Start- og landingssteder, luftrom, vindretninger
│   └── hanguren.md
├── sikkerhet/              # Nødprosedyrer, førstehjelp, OBSREG
│   └── nodprosedyrer.md
├── klubben/                # Styret, årsmøter, vedtekter, medlemskap
├── skoling/                # Kurs, progresjon (PP2-PP5), sjekklister
├── utstyr/                 # Klubbvinger, seler, pakking av nødskjerm
└── assets/                 # Bilder og vedlegg (opplastet via Wiki.js)
```

---

## ✍️ Hvordan bidra med innhold

1. Opprett en branch eller gjør en `fork`.
2. Skriv eller oppdater artikler i standard Markdown (`.md`).
3. Send inn en **Pull Request** for vurdering av styret / redaktører.
4. Når PR-en merges til `main`, oppdateres klubbwikien automatisk!
