# Voss HPK Wiki — Content and Git Storage

This repository (`vosshpk/wiki`) contains the Markdown pages for the **Voss Hang- og Paragliderklubb wiki**. The default-language pages in the repository root are written in Norwegian Nynorsk (`nn`). Wiki.js does not translate page content automatically: English page translations must be added separately under `en/` using the same paths.

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
├── en/                     # English page translations (locale: en; currently to be added)
├── klubben/                # Club information and governance
│   ├── om-klubben.md
│   ├── fasiliteter.md
│   ├── medlemskap.md
│   ├── styret.md
│   └── arsmoete.md
├── flysteder/              # Launch and landing sites, airspace, wind directions
│   ├── flysteder.md
│   ├── hanguren.md
│   └── skulebakke.md
├── sikkerhet/              # Emergency procedures, first aid, OBSREG
│   ├── flytrygging.md
│   └── nodprosedyrer.md
├── opplaering/             # Opplæring, progresjon og sjekklister
│   └── progresjon.md
├── utstyr/                 # Club equipment and maintenance
│   └── klubbutstyr.md
└── assets/                 # Images and attachments (uploaded through Wiki.js)
```

Folder names map directly to the page paths used by the wiki.

---

## ✍️ Contributing content

1. Create a branch or fork the repository.
2. Write or update articles in standard Markdown (`.md`).
3. Submit a **pull request** for review by the board or editors.
4. After the pull request is merged into `main`, Wiki.js should pick up the change during its next Git Storage synchronization. Check the synchronization status if a change does not appear.

The Git repository contains Markdown page content. Wiki.js users, settings, and uploaded media are stored in PostgreSQL on the VM's persistent data disk. Daily PostgreSQL dumps are stored in a private Google Cloud Storage backup bucket; Git is not a backup of the database or media.

## Language and initial import into Wiki.js

Set Nynorsk (`nn`) as the Wiki.js site locale and enable English (`en`) under **Administration → Locale → Multilingual Namespaces**. In Git Storage, keep **Always Locale Namespace** disabled to match this repository layout: base-language pages stay at the root and translated pages use the `en/` directory. If that option is enabled, the repo must instead use `nn/` and `en/` directories for all pages.

Connecting Git Storage does not by itself import all existing files. After the Git Storage status is healthy, use **Administration → Storage → Git → Import Everything** once to import the existing repository pages into a fresh Wiki.js database. Check the sync mode before running it: **pull** makes Git authoritative, **push** makes the wiki authoritative, and **sync** reconciles both sides. See the infrastructure repository's `GCP_SETUP_GUIDE.md` for the full deployment and operations notes.
