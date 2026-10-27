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
├── dagleg-leiar/           # Managing director role and procedures
│   ├── dagleg-leiar.md
│   ├── stillingsinstruks.md
│   ├── fullmaktsmatrise.md
│   └── personalrutinar.md
├── fly/                    # Flying sites, visiting-pilot guidance and ROS analyses
│   ├── flysteder.md        # One consolidated page, including Hanguren and Skulebakken
│   ├── besokande-pilotar.md
│   ├── ROS.md              # Index of site risk analyses
│   └── ROS/                # Markdown analyses for nine flying sites
├── klubben/                # Club information, membership and activities
│   ├── om-klubben.md
│   ├── medlemskap.md
│   ├── medlemsfordelar.md
│   ├── aktivitetar.md
│   ├── frivillig-arbeid.md
│   ├── forsikring.md
│   └── overnatting.md
├── klubbutstyr/            # Equipment, clubhouse, boat, trailer and car
│   ├── utstyr.md
│   ├── fasiliteter.md
│   ├── klubbhus.md
│   ├── bat.md
│   ├── tilhenger.md
│   ├── bil.md
│   └── opptrekk-landvinsj.md
├── kommunikasjon/          # Communications plans, roles, privacy and incidents
│   ├── intern-kommunikasjonsplan.md
│   ├── ekstern-kommunikasjonsplan.md
│   ├── ansvar-kommunikasjon-og-myndigheit.md
│   ├── kommunikasjon-ved-hendingar.md
│   └── kommunikasjon-og-personvern.md
├── opplaering/             # Training, progression and course guidance
│   ├── progresjon.md
│   ├── rammer-for-kursing.md
│   └── rammer-progresjonskurs.md
├── organisatorisk/         # AGM, organisation plan, strategy, programme and bylaws
│   ├── arsmoete.md
│   ├── organisasjonsplan.md
│   ├── programplan-2025.md
│   ├── styringsdokument.md
│   ├── lov.md
│   └── roller.md
├── rutiner/                # Equipment and facility maintenance procedures
│   ├── arshjul.md          # Annual routine calendar
│   ├── bat-og-fortoying.md
│   ├── bil.md
│   ├── flyutstyr.md
│   ├── startplassar.md
│   ├── tilhenger.md
│   ├── klubbhus.md
│   └── klubbvogn.md
├── styret/                 # Board overview, members, instructions and committees
│   ├── styret.md
│   ├── styreinstruks.md
│   └── utval.md
├── sikkerhet/              # Emergency procedures, first aid, OBSREG
│   ├── flytrygging.md
│   ├── nodprosedyrer.md
│   └── tryggleiksgruppe.md
├── en/                     # English page translations (locale: en)
├── assets/
│   ├── landvinsj-transport.jpg
│   ├── landvinsj-kontrollboks.jpg
│   └── ros/                # Map screenshots cropped from the ROS source PDFs
└── tandem/                 # Member-only content (configure Wiki.js access)
    ├── kompensasjon-2026.md # Member-only tandem compensation
    ├── eigenfrasegn.md      # Links to current official NLF print forms
    └── archived 2023/2024 tandem source pages
```

Folder names map directly to the page paths used by the wiki. The wiki itself is the club handbook; there is no separate handbook page. The source guide in `docs/veileder-klubbhandbok-pr-august-2023.docx` was considered as a checklist for relevant topics and placeholders. Its applicable themes are distributed across the club, board, managing director, governance, training, equipment and safety sections. Generic team-sport topics that do not fit hang- and paragliding have not been copied as if they applied.

---

## ✍️ Contributing content

1. Create a branch or fork the repository.
2. Write or update articles in standard Markdown (`.md`).
3. Submit a **pull request** for review by the board or editors.
4. After the pull request is merged into `main`, Wiki.js should pick up the change during its next Git Storage synchronization. Check the synchronization status if a change does not appear.

The Git repository contains the Markdown wiki pages, two winch photos and map screenshots cropped from the ROS source PDFs; source PDFs are not stored in this repository. Images embedded in pages currently use the public GitHub `main` branch. If this repository is private, public Wiki.js visitors will not be able to load those GitHub-hosted images; upload them through Wiki.js Assets and update the page links if the wiki pages are public. Wiki.js users, settings, and files uploaded through its Assets tool are stored in PostgreSQL on the VM's persistent data disk. Daily PostgreSQL dumps are stored in a private Google Cloud Storage backup bucket.

### Member-only pages

In Wiki.js, create a `Members` group and grant it `read:pages` with page rules for paths starting with `/tandem` and `/en/tandem`. In the `Guests` group, add more specific `Deny` rules for `read:pages` on both paths; also remove any broad guest rule that would otherwise expose these pages. The internal communications and incident pages may also need member-only access; review `/kommunikasjon/intern-kommunikasjonsplan`, `/kommunikasjon/ansvar-kommunikasjon-og-myndigheit`, `/kommunikasjon/kommunikasjon-ved-hendingar` and their `/en/` translations. Test while signed out and with a normal member account. Wiki.js page permissions do not protect the Git repository: if this repository is public, its Markdown is public on GitHub too. Keep confidential/member-only page source out of a public repository, or make the repository private before syncing it.

## Language and initial import into Wiki.js

Set Nynorsk (`nn`) as the Wiki.js site locale and enable English (`en`) under **Administration → Locale → Multilingual Namespaces**. In Git Storage, keep **Always Locale Namespace** disabled to match this repository layout: base-language pages stay at the root and translated pages use the `en/` directory. If that option is enabled, the repo must instead use `nn/` and `en/` directories for all pages.

Connecting Git Storage does not by itself import all existing files. After the Git Storage status is healthy, use **Administration → Storage → Git → Import Everything** once to import the existing repository pages into a fresh Wiki.js database. Check the sync mode before running it: **pull** makes Git authoritative, **push** makes the wiki authoritative, and **sync** reconciles both sides. See the infrastructure repository's `GCP_SETUP_GUIDE.md` for the full deployment and operations notes.
