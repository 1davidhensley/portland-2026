# CLAUDE.md

PWA for David & Paula's Portland, OR trip (Fri Nov 6 – Sun Nov 8, 2026), built from `1davidhensley/victoria-2026`. All project docs are in `docs/`: read `docs/README.md` (how to update and redeploy) and `docs/KNOWN-ISSUES.md` (open items + version history) first.

Hard rules:
- **Bump `CACHE_NAME` in `sw.js` (`portland-2026-vN`) on every content change**, and add a row to the version history in `docs/KNOWN-ISSUES.md`.
- **Public site:** no confirmation numbers, prices, card details, or email addresses.
- Edit `dayData` in `index.html`, not hand-written HTML. Unknowns go in `tbd` / `confirm`; never invent facts.
- `node --check` the JS (sw.js + the inline script in index.html) and check the layout at ~390 px before committing.
- Do not modify the victoria-2026 repo.
