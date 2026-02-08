---
name: "📂 New Repository Request"
about: Propose a new sub-repository to manage growth and maintain minimal standards.
title: "[REPO]: "
labels: enhancement, structural
---

## 🏛️ Rationale for Sub-Repositories
SpocWiki creates sub-repositories as new folders (e.g., `Topic/`) to:
- **Keep `_Standards` Repository Minimal:** Maintain a lightweight, manageable  for the organization.
- **Manage Growth:** Move structures that have become too large or too deep into dedicated Sub-Repositories.

## 🏷️ Sub-Repository Naming Convention 

To maintain a traceable hierarchy, we follow a strict naming pattern:
- **Root Repositories:** New top-level domains in `_Standards` (e.g., `Science`, `Geo`).
- **Sub-Repositories:** Typically named after the last part of their **parent-repo** followed by a **Dash** and their **Folder Name** in that parent repo.
  - *Example:* `Europe` (parent) + `Germany` (folder) → **`Europe-Germany`**
  - *Example:* `Europe-Germany` (parent) + `Bayern` (folder) → **`Germany-Bayern`** 
  - this provides a clear trail in the Repository Hierarchy 

## 🌎 Scope & Hierarchy 

Creating a new repository requires consent from maintainers and the following technical "handshake":

- [ ] **`ReadMe.md`**: A root file in the new repo that mirrors the content of the parent's folder-note (e.g., `Topic.md`).
- [ ] **`CheckoutTopic.ps1`**: A PowerShell script to automate checking out the new repository into the local `Topic/` folder.
- [ ] **`.gitIgnore` Entry**: An entry in the parent repository to exclude the new folder, avoiding Git Submodule handling.

## ✅ Verification 

- [ ] I have checked that this data is not already covered elsewhere.
- [ ] I am willing to prepare the `.ps1` and `ReadMe.md` files according to SpocWiki standards.
- [ ] I understand that all naming must follow the Conventions, avoid spaces and are globally unique across all Repositories.

