# Voss HPK Wiki — Content and Git Storage

This repository (`vosshpk/wiki`) contains the Markdown pages for the **Voss Hang- og Paragliderklubb wiki**. The default-language pages in the repository root are written in Norwegian Nynorsk (`nn`); English translations are stored under `en/` with matching paths. Wiki.js does not translate page content automatically.

The club wiki runs on **Wiki.js v2** on a Google Compute Engine VM, with PostgreSQL 18. Wiki.js connects to this repository through its built-in **Git Storage** module.

---

## 🔄 How synchronization works

1. **Editing in Wiki.js:**
   * Git Storage can push page content to this repository during scheduled synchronization.
2. **Editing through GitHub:**
   * Changes can be submitted through pull requests. With Git Storage set to bidirectional sync, merged changes are imported on the next scheduled synchronization (or after an administrator runs **Force Sync**).
3. **Avoiding conflicting changes:**
   * Do not edit the same page in Wiki.js and a GitHub pull request at the same time. Git Storage is not a pull-request review workflow, and concurrent changes can cause conflicts.

---

## 📁 Repository structure

```text
├── home.md                 # Nynorsk home page (base locale: nn)
├── en/                     # English page translations (locale: en)
├── fly.md                  # Flying section index
├── fly/                    # Flying sites and visiting-pilot guidance
│   ├── flysteder.md        # One consolidated page, including Hanguren and Skulebakken
│   └── besokande-pilotar.md
├── styret.md               # Board members and board instructions
├── styret/
│   └── styreinstruks.md
├── dagleg-leiar.md         # Managing director overview
├── dagleg-leiar/
│   ├── stillingsinstruks.md
│   └── fullmaktsmatrise.md
├── klubbutstyr.md          # Equipment and facilities index
├── klubbutstyr/            # Equipment, clubhouse, boat, trailer and car
│   ├── utstyr.md
│   ├── fasiliteter.md
│   ├── bat.md
│   ├── tilhenger.md
│   ├── bil.md
│   └── opptrekk-landvinsj.md
├── organisatorisk.md       # Governance documents index
├── organisatorisk/         # AGM, organisation plan, strategy, programme and bylaws
│   ├── arsmoete.md
│   ├── organisasjonsplan.md
│   ├── programplan-2025.md
│   ├── styringsdokument.md
│   ├── vedtekter.md
│   └── utval.md
├── klubben/                # Club information and governance
│   ├── handbok.md          # Handbook index and outstanding topics
│   ├── om-klubben.md
│   ├── medlemskap.md
│   └── overnatting.md
├── sikkerhet/              # Emergency procedures, first aid, OBSREG
│   ├── flytrygging.md
│   ├── nodprosedyrer.md
│   └── tryggleiksgruppe.md
├── opplaering/             # Opplæring, progresjon og sjekklister
│   └── progresjon.md
└── assets/
    ├── landvinsj-transport.jpg
    └── landvinsj-kontrollboks.jpg
```

Folder names map directly to the page paths used by the wiki.

---

## ✍️ Contributing content

1. Create a branch or fork the repository.
2. Write or update articles in standard Markdown (`.md`).
3. Submit a **pull request** for review by the board or editors.
4. After the pull request is merged into `main`, Wiki.js should pick up the change during its next Git Storage synchronization. Check the synchronization status if a change does not appear.

The Git repository contains the Markdown wiki pages and two extracted winch photos; source PDFs are converted to text and are not retained in this repository. Embedded photos use the public GitHub `main` branch. Wiki.js users, settings, and files uploaded through its Assets tool are stored in PostgreSQL on the VM's persistent data disk. Daily PostgreSQL dumps are stored in a private Google Cloud Storage backup bucket.

## Language and initial import into Wiki.js

Set Nynorsk (`nn`) as the Wiki.js site locale and enable English (`en`) under **Administration → Locale → Multilingual Namespaces**. In Git Storage, keep **Always Locale Namespace** disabled to match this repository layout: base-language pages stay at the root and translated pages use the `en/` directory. If that option is enabled, the repo must instead use `nn/` and `en/` directories for all pages.

Connecting Git Storage does not by itself import all existing files. After the Git Storage status is healthy, use **Administration → Storage → Git → Import Everything** once to import the existing repository pages into a fresh Wiki.js database. Check the sync mode before running it: **pull** makes Git authoritative, **push** makes the wiki authoritative, and **sync** reconciles both sides. See the infrastructure repository's `GCP_SETUP_GUIDE.md` for the full deployment and operations notes.
