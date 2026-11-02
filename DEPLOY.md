# Conference Companion deployment

This repository owns the DEMO conference package, install branding and its own GitHub Pages deployment. The attendee engine, schemas and validators come from `anniantola/conference-companion` during the Pages build. The workflow checks out the tested v1.2.15 engine commit `eeb7e57f412b63c98a65c07364eeae15b4e17888` into `.engine`, validates this conference, stages only attendee files into `_site`, and deploys the result. The two repositories keep separate Git histories and Pages deployments. To adopt a later engine release, update the pinned `ref` in `.github/workflows/deploy.yml` and rerun validation before publishing.

For local checks, keep `conference-companion` beside this repository, then run `npm test` and `npm run stage`. Set `CONFERENCE_ENGINE_DIR` to a different engine checkout when needed. The `_site` output is generated and ignored by Git.

Existing v1.2.12 attendee records remain in browser storage after this engine upgrade, but the new deployment-scoped store does not automatically assign those older origin-wide records to DEMO. Restore a personal backup in this deployment if available. If no backup exists, keep the browser profile and site data intact for assisted recovery.

Conference: DEMO
Data version: 1
Generated: 2026-10-30T10:15:01.645Z
