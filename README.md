# Voss HPK Wiki — Content and Git Storage

This repository (`vosshpk/wiki`) contains the Markdown articles, guides, and files for the **Voss Hang Gliding and Paragliding Club wiki**.

The club wiki is planned to run on **Wiki.js v2** in Google Cloud (Cloud Run + PostgreSQL 18). Wiki.js can connect to this repository through its built-in **Git Storage** module.

---

## 🔄 How synchronization works

1. **Editing in Wiki.js:**
   * Git Storage can push page content to this repository during scheduled synchronization.
2. **Editing through GitHub:**
   * Changes can be submitted through pull requests. Wiki.js must be configured to pull from the repository; changes appear at the next scheduled synchronization, not immediately.
3. **Avoiding conflicting changes:**
   * Do not edit the same page in Wiki.js and a GitHub pull request at the same time. Git Storage is not a pull-request review workflow, and concurrent changes can cause conflicts.

---

## 📁 Repository structure

```text
├── home.md                 # Wiki home page
├── flysteder/              # Launch and landing sites, airspace, wind directions
│   └── hanguren.md
├── sikkerhet/              # Emergency procedures, first aid, OBSREG
│   └── nodprosedyrer.md
├── klubben/                # Board, annual meetings, bylaws, membership
├── skoling/                # Courses, progression (PP2–PP5), checklists
├── utstyr/                 # Club wings, harnesses, reserve parachute packing
└── assets/                 # Images and attachments (uploaded through Wiki.js)
```

The existing folder names are retained because they are part of the page paths used by the wiki.

---

## ✍️ Contributing content

1. Create a branch or fork the repository.
2. Write or update articles in standard Markdown (`.md`).
3. Submit a **pull request** for review by the board or editors.
4. After the pull request is merged into `main`, Wiki.js should pick up the change during its next Git Storage synchronization. Check the synchronization status if a change does not appear.

The Git repository contains page content. Wiki.js users, system settings, and uploaded media are stored in PostgreSQL and covered by Cloud SQL backups.
