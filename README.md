# Magnolia Clinic Hub

Staff website for Magnolia Clinic: cleaning schedule, supplies, CLIA QC, NDC/Lot, calendar, sticky notes, admin.

Live at https://magnolia-clinic-hub.jacob-d91.workers.dev

Completely separate from the Aligned Clinic Hub: its own Cloudflare Worker (`magnolia-clinic-hub`), its own D1 database, its own repo.

- `worker.js` is the whole site. Pushing to `main` redeploys it.
- `wrangler.toml` holds the D1 binding (`DB`) and the 30-minute cron for reminder emails.
- `source/` holds the sources and build scripts that generate `worker.js`.

No passwords, keys or the first-time setup code live in this repo; they are stored in the D1 database.
