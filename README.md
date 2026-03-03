
# Single‑Page Tabbed Knowledge App (PWA, JSON Storage)

A lightweight, offline‑first **single‑page web app** for:
1) Documenting learning,  
2) Building a reusable knowledge base, and  
3) Tracking issues—  
with **JSON storage (IndexedDB)**, **print‑friendly outputs**, and **exports to Excel, OneNote, Access, and SQL**.

- **Phone + Web:** Progressive Web App (installable, offline‑capable)
- **Storage:** Client‑side IndexedDB with JSON export/import
- **Sync options:** OneDrive/SharePoint (Graph), GitHub, or SQL backend
- **Print:** Field‑ready SOPs/checklists

## Quick Start
1. Open `/docs/FEATURES.md` to understand core features.
2. Review `/docs/DATA_MODEL.md` for JSON schemas.
3. Deploy using `/deployment/DEPLOYMENT.md`.
4. Enable sync using `/sync/SYNC_ARCHITECTURE.md`.

## Project Structure
- `docs/` — Feature spec, data model, templates, print styles, exports, test plan, etc.
- `deployment/` — PWA manifest and service worker guides, hosting steps.
- `sync/` — OneDrive (Graph), SharePoint, GitHub, and SQL sync specs.

## Exports & Integrations
- Excel `.xlsx` (multi‑sheet), CSV
- OneNote (Markdown)
- Access (via CSV/XLSX)
- SQL (CSV/XLSX or REST/DDL)

## License
MIT
