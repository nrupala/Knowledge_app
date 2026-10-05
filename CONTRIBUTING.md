# Contributing — Knowledge_app

## PR-flow discipline (Portfolio Certification Program)

- Draft PR → tests green → owner merges. NO direct pushes to `main`.
- Every PR adds a CHANGELOG entry under `## [Unreleased]`.
- Where a version file exists, every PR bumps semver (patch=fix,
  minor=feature); merge commits reference the PR number; releases are
  tagged `vX.Y.Z`.

## Notes

- This repository currently holds only documentation and licensing files
  (README.md, LICENSE). The `/docs`, `/deployment`, and `/sync`
  directories described in the README are not yet committed — if they
  are added later, the docs must describe their real behavior; never
  invent features.
- Secrets: never commit plaintext credentials.
