# Maritime Chartering Radar

## Public application

- Application: https://hanymahdy2.github.io/Railway/
- Dated vessel-screening report: https://hanymahdy2.github.io/Railway/leads_2026-10-30.html
- Screening data CSV: https://hanymahdy2.github.io/Railway/charter_leads_2026-10-30.csv
- GitHub Actions deployment history: https://github.com/hanymahdy2/Railway/actions

## Current browser features

- Enter multiple charter requirements in one text box.
- Separate requirements with headings such as `Requirement 1:`, `Vessel 2:`, numbered sections, or blank-line-separated paragraphs.
- Extract vessel quantity, DWT, TEU, crane/gear requirements, vessel type, target region, and charter duration where expressed clearly.
- Scan all rows in the currently imported dataset for every requirement; do not stop after the first candidate.
- Display a separate ranked shortlist for each requirement, with match score, recorded specs, port/area, open date, owner, broker/contact, source link, and AIS timestamp when supplied.
- Recognize common Arabic and English quantities, minimums, regions and vessel types.

## How to use

1. Open the application link above.
2. Load the basic vessel-particulars database, or import your own CSV.
3. Paste multiple requirements. Use one heading per requirement, or leave a blank line between separate paragraphs.
4. Select **Analyze all requirements and find matches** (Arabic UI: **حلّل كل الطلبات وابحث عن التطابقات**).
5. Review each requirement's candidates, match basis, source, availability claim and position timestamp.
6. For additional open-position and AIS data, import a permitted CSV with fields such as:

`name, imo, vessel_type, dwt, teu, cranes_mt, area, current_position, open_port, open_date, availability_status, owner, owner_email, commercial_manager, commercial_manager_email, broker, broker_email, contact, lat, lon, ais_timestamp, published_at, source_url`

The app scans the full imported dataset, but shows the top 20 candidates per requirement in the results table.

## Important data limitations

- The bundled public vessel-particulars CSV is a static identity/specifications dataset. It does **not** by itself provide live positions or current open-for-charter availability.
- GitHub Pages is a static website. This build does **not** yet connect to a live AIS provider, chartering circular inbox, or a live global open-tonnage network.
- AIS position is not proof that a vessel is unemployed, free, or open for charter.
- An imported `Open` / `Free` / open-port / open-date claim is labelled as a **reported** position and must be confirmed directly with the owner or an authorized broker. Old listings should be reconfirmed.
- Geographic matching currently uses recorded port/area text and common region aliases. Coordinates are displayed if imported, but are not automatically reverse-geocoded into a region.
- For real live positions, AIS Trail publishes plan limits: its Free plan has a 24-hour delay and no area queries; live positions and area scanning require paid tiers. AIS alone still does not prove commercial availability. See https://aistrail.com/pricing and https://aistrail.com/docs/.
- For open-tonnage/cargo-market circulars, BTS Coasting describes a closed chartering network, open-position exchange, inbox integration, live AIS and a Maritime API. Access requires a commercial account/agreement. See https://www.btscoasting.com/products/.

## Repository files

- `index.html`: browser application.
- `leads_2026-10-30.html`: dated public-source vessel screening report; not a firm offer.
- `charter_leads_2026-10-30.csv`: structured screening records for spreadsheet import.

## Security and publication

This GitHub repository is public. Do not place API keys, passwords, private chartering circulars, confidential broker emails, or personal contact datasets in the repository. Any future provider integration must keep credentials in a server-side secret store, not in browser JavaScript or committed files.
