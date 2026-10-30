# Maritime Chartering Radar — Permanent Browser Link

## One-time GitHub Pages activation

The application and the dated screening report have been committed to the public repository:
https://github.com/hanymahdy2/Railway/tree/main/Maritime_Chartering_Radar

The deployment workflow is already present at:
https://github.com/hanymahdy2/Railway/blob/main/.github/workflows/maritime-radar-pages.yml

To activate the permanent public site once:

1. Open https://github.com/hanymahdy2/Railway/settings/pages
2. Under **Build and deployment**, set **Source** to **GitHub Actions** and save.
3. Open https://github.com/hanymahdy2/Railway/actions
4. Select **Deploy Maritime Chartering Radar to GitHub Pages**.
5. Select **Run workflow** on branch `main`.

After GitHub reports a successful deployment, the permanent application URL is:
https://hanymahdy2.github.io/Railway/

The dated vessel-screening report will be:
https://hanymahdy2.github.io/Railway/leads_2026-10-30.html

The CSV lead list will be:
https://hanymahdy2.github.io/Railway/charter_leads_2026-10-30.csv

## Files

- `index.html`: browser application wrapper (gzip-compressed self-contained HTML).
- `leads_2026-10-30.html`: screened vessel leads, contacts, source links, and caveats.
- `charter_leads_2026-10-30.csv`: structured data for Excel/import.

## Limitations

The GitHub Pages deployment is **not yet confirmed**. Do not describe the Pages URLs above as live until the Actions workflow has completed successfully. The GitHub repository files themselves are public and already committed.

The vessel shortlist is a public-source screening report, not a firm offer or confirmed time-charter availability. Availability, class, crane certificates, latest AIS position and employment must be reconfirmed directly with the owner, manager or authorized broker before circulation.
