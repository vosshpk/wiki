# Voss HPK Wiki — Content and Git Storage

This repository (`vosshpk/wiki`) contains Markdown content for the **Voss Hang- og Paragliderklubb wiki**.
Pages are grouped by locale under `nn/` and `en/`; Wiki.js does not translate page content automatically.
Wiki.js instances connect to this repository through the built-in **Git Storage** module.

---

## 🔄 How synchronization works

1. **Editing in Wiki.js:**
   * Git Storage can push page content to this repository during scheduled synchronization.
2. **Editing through GitHub:**
   * Changes can be submitted through pull requests.
     With Git Storage set to bidirectional sync, merged changes are imported on the next scheduled synchronization (or after an administrator runs **Force Sync**).
3. **Avoiding conflicting changes:**
   * Do not edit the same page in Wiki.js and a GitHub pull request at the same time.
     Git Storage is not a pull-request review workflow, and concurrent changes can cause conflicts.

---

## 📁 Repository structure

Markdown content is grouped by locale in `nn/` and `en/`.
Within each locale, folder and file names determine the wiki page paths.
Add, rename or move pages in those trees and update any links that point to them; this README intentionally does not maintain a page-by-page inventory.

The top-level `assets/` directory contains images used by pages.
The wiki is the club handbook; there is no separate handbook page.

For Wiki.js 3, the infrastructure repository has a navigation generator that reads these locale trees and uses Markdown headings for labels.
The sidebar can be regenerated after pages are added, renamed or removed.

---

## ✍️ Contributing content

1. Create a branch or fork the repository.
2. Write or update articles in standard Markdown (`.md`).
3. Submit a **pull request** for review by the board or editors.
4. After the pull request is merged into `main`, Wiki.js should pick up the change during its next Git Storage synchronization.
   Check the synchronization status if a change does not appear.

The Git repository contains the Markdown wiki pages, two winch photos and map screenshots cropped from the ROS source PDFs; source PDFs are not stored in this repository.
Images embedded in pages currently use the public GitHub `main` branch.
If this repository is private, public Wiki.js visitors will not be able to load those GitHub-hosted images; upload them through Wiki.js Assets and update the page links if the wiki pages are public.
Wiki.js users, settings, and files uploaded through its Assets tool are stored in PostgreSQL on the VM's persistent data disk.
Daily PostgreSQL dumps are stored in a private Google Cloud Storage backup bucket.

### Public access

All wiki pages are publicly accessible.
Do not put personal or confidential records in the wiki or this repository; store them in approved systems with appropriate access controls.
If this repository is public, its Markdown is public on GitHub too.

## Language and initial import into Wiki.js

The repository uses `nn/` and `en/` locale directories.
Configure Wiki.js Multilingual Namespaces and Git Storage to preserve both locale namespaces and keep the file paths aligned with the page paths.

Connecting Git Storage does not by itself import all existing files.
After the Git Storage status is healthy, use **Administration → Storage → Git → Import Everything** once to import the existing repository pages into a fresh Wiki.js database.
Check the sync mode before running it: **pull** makes Git authoritative, **push** makes the wiki authoritative, and **sync** reconciles both sides.
See the infrastructure repository's `GCP_SETUP_GUIDE.md` for the full deployment and operations notes.
