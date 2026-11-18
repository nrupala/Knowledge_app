# Codetopo Profile — Knowledge App (nrupala/Knowledge_app)

**What this is.** The agent-facing map of this repository, generated with
Codetopo 0.9.1 (local engine, `~/.cargo/bin/codetopo`) so an arriving agent
can see what the repo holds — topology, trust boundaries, money surface —
before it submits or changes anything. Read this first; the graph snapshot
beside it (`snapshot.json`, `stats.json`) is the measured evidence.

- **Repo:** nrupala/Knowledge_app (public)
- **Commit profiled:** `2a1d60d089f5b44505f3d68d6e13d2c77655a596` (main, 2026-11-07)
- **Engine:** codetopo 0.9.1 · index run 2026-11-18
- **Graph:** 4 files walked · 0 failed · 13 nodes · 12 edges · audit chain valid (3 entries, head `51e2d158…b86c8`)
- **Nodes by kind:** doc 4 · file 4 · module 4 · package 1
- **Edges by kind:** contains 12

## Coverage honesty

**This graph has zero code symbols — because this repo contains no code
at the commit profiled.** The tree holds 9 files total: 4 Markdown files
(`README.md`, `CHANGELOG.md`, `CONTRIBUTING.md`, `TERMS.md`), `LICENSE`,
`NOTICE`, `.github/FUNDING.yml`, and two icon assets (`assets/icon.svg`,
`assets/icon-512.png`). Codetopo indexed the 4 Markdown files as Doc
nodes only. GitHub detects no languages for this repo. There are no
functions, classes, imports or call edges to report, and this profile
invents none.

**Named discrepancy (read this before trusting the README):** the
README describes a single-page PWA and points at `/docs/FEATURES.md`,
`/docs/DATA_MODEL.md`, `/deployment/DEPLOYMENT.md` and
`/sync/SYNC_ARCHITECTURE.md` — **none of those paths exist in this
tree**. The README is a plan/description of an app; the app itself is
not in this repository at this commit.

## Topology

There is no code topology. What the repo holds:

- `README.md` — the product description: a lightweight, offline-first
  single-page knowledge app (document learning, build a reusable
  knowledge base, track issues) with JSON storage in IndexedDB,
  print-friendly outputs, exports (Excel/CSV, OneNote, Access, SQL) and
  described sync options (OneDrive/SharePoint Graph, GitHub, SQL
  backend). All of this is **described, not implemented, in this repo**.
- `TERMS.md` — the standard product terms of 2351485 ALBERTA INC.
- `CHANGELOG.md`, `CONTRIBUTING.md` — house-standard repo documents.
- `LICENSE` (README states MIT), `NOTICE`, `assets/` (app icons),
  `.github/FUNDING.yml`.

An agent looking for the app should read the README as a spec pointer
and look for the implementation elsewhere; do not treat the described
`docs/`, `deployment/` or `sync/` structure as present.

## Trust boundaries

- **No code, no credentials, no data surface in this repo.** Greps for
  `stripe|paddle|secret|token|api_key|auth|password|billing|checkout|webhook`
  over the whole tree return a single hit: `CONTRIBUTING.md`'s standing
  rule "Secrets: never commit plaintext credentials." No secret, key,
  token value or account identifier exists in this repo.
- The README *describes* future trust-relevant behaviour (client-side
  IndexedDB storage; sync to OneDrive/SharePoint/GitHub/SQL) — none of
  it is implemented here, so none of it can be audited from this repo.

## Money surface

**None found — explicitly.** There is no payment, billing, checkout,
card, subscription or webhook surface in this repo, and no code at all
to carry one. Greps used:
`stripe|paddle|secret|token|api_key|auth|password|billing|checkout|webhook`
over the full tree — the only hit is the CONTRIBUTING secrets rule
named above.

## How an agent should approach

1. Read `README.md` as the product description — and hold the Coverage
   discrepancy in mind: its linked spec files are absent.
2. Do not look for code, tests or a build here; there is none at this
   commit. Do not report the described PWA as existing on this repo's
   evidence.
3. Regenerate this profile (below) if the repo's shape changes —
   above all if code or the missing spec directories land, at which
   point this becomes a real code profile.

## Regeneration

`docs/codetopo-profile/refresh.sh` (in this pack) re-downloads the repo
at a named ref, re-runs the index, and rewrites `snapshot.json`,
`stats.json` and the header block inputs of this profile. Regenerate at
every material change to the repo.
