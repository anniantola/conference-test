# Conference Companion deployment

This repository owns the DEMO conference package, install branding and its own GitHub Pages deployment. The attendee engine, schemas and validators come from `anniantola/conference-companion` during the Pages build. The workflow checks out the tested v1.2.14 engine commit `f829d7ca7536e521b959826c8251ce64a09d5d1a` into `.engine`, validates this conference, stages only attendee files into `_site`, and deploys the result. The two repositories keep separate Git histories and Pages deployments. To adopt a later engine release, update the pinned `ref` in `.github/workflows/deploy.yml` and rerun validation before publishing.

For local checks, keep `conference-companion` beside this repository, then run `npm test` and `npm run stage`. Set `CONFERENCE_ENGINE_DIR` to a different engine checkout when needed. The `_site` output is generated and ignored by Git.

Conference: DEMO
Data version: 1
Generated: 2026-10-30T10:15:01.645Z
