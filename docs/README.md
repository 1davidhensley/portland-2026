# Portland 2026 Trip App

An offline-capable, installable web app (PWA) for David & Paula's Portland, OR weekend, **Fri Nov 13 – Sun Nov 15, 2026** (moved from Nov 6–8), staying at the Kimpton Hotel Vintage.

- **Live:** https://1davidhensley.github.io/portland-2026/
- **Repo:** https://github.com/1davidhensley/portland-2026 (public, GitHub Pages from `main` / root)
- **Template:** built from [`victoria-2026`](https://github.com/1davidhensley/victoria-2026) (same single-file layout, look, day cards, map links, offline service worker). It is an independent copy and shares nothing with Victoria at runtime.

## What's in it

- **Fri 13:** drive down (I-205 split at Salmon Creek), Columbia Sports Cards & More and In-N-Out (Vancouver, WA), ORB Sports Cards (Oregon City), Kimpton Hotel Vintage, a 1-hr Guardian Games card evaluation at 5:00, dinner at Dolly Olive.
- **Sat 14 (wine day):** Eminent Domaine and Anacréon in Newberg, back to the hotel, then Guardian Games for three card evaluations (3:00, 4:00 and 5:30). Lunch, dinner and the driver are open.
- **Sun 15:** breakfast, Powell's City of Books (optional), check-out, drive home.
- **Travel & Stay**, **Resources** (a "Still open" to-do panel, wine-day tips, Guardian Games appointments, money, emergency, getting around, ideas), **Packing** checklist.
- Live weather from Open-Meteo once the trip is within 16 days. Before that, and when offline, it shows November averages.
- **Rose City Card Set:** twelve collectible Portland-fact cards, three to a pack. One pack is open before the trip and one unlocks each trip day. Collected cards are saved on each phone.
- Hero art (Mt. Hood over a fir treeline) and a few hidden surprises; see "Fun stuff" below.
- A footer version tag shows whether the installed copy is current.

## Files

```
index.html      The whole app: markup, CSS, JS, and the trip data (dayData, travelData, resources, packingList)
sw.js           Service worker. CACHE_NAME = 'portland-2026-vN'
manifest.json   PWA name, colors, icon
CLAUDE.md       Short rules for Claude when editing (points here)
docs/           README.md (this file), KNOWN-ISSUES.md, ROADMAP.md
```

No build step, no packages, no framework.

## Ground rules

1. **Bump `CACHE_NAME` in `sw.js` on every content change** (`portland-2026-v1` → `v2` → …). Without it, installed copies on the phones keep showing old data. This bit us on the London app.
2. **The site is public.** Never add confirmation numbers, prices, card details, or email addresses. Venue names, addresses, times, and public phone numbers are fine.
3. **Never invent facts.** Unknowns go in a stop's `tbd`; addresses or hours that need checking go in `confirm`; ideas that aren't booked get `suggested: true`.
4. **Validate before committing:** `node --check` on the JavaScript, and look at the layout at phone width (~390 px).
5. Log open questions and each version in `docs/KNOWN-ISSUES.md`.

## How to update the itinerary

Edit the data in `index.html`, not the HTML. Each day in `dayData` has `stops[]`. Stop fields:

| Field | What it does |
|---|---|
| `time`, `emoji`, `name`, `details` | Basics. `details` may contain simple HTML (`<strong>`, `<a href="tel:…">`). |
| `mapsQuery` | Adds a 📍 Open in Maps button. |
| `mapsLinks: [{label, q}]` | Extra Maps buttons, e.g. when there are two possible addresses. |
| `walkTo`, `walkMapsQuery` | Dashed walking line after the stop, with a walking-directions link. |
| `transportDir` | Step-by-step driving/transit box. |
| `checklist: []` | Tickable items (saved on the phone). |
| `reservation` | Green "📋 …" tag. |
| `included` | "✓ Included" tag (e.g. hotel breakfast). |
| `pick: 'Paula'` | "💖 Paula's pick" tag. |
| `optional: true` | "Optional" tag and hollow dot. |
| `confirm` | Amber "Confirm before going" box. |
| `alert` | Red warning box (e.g. the Anacréon GPS issue). |
| `tbd` | "⚠️ TBD: …" line. |
| `options: [{name, details, mapsQuery}]` | Side-by-side choices for an undecided stop (used for Saturday dinner until v2). |

Saturday has `isWine: true`, which gives it the wine accent color. A day's `note` shows a box at the top of its card. A `resources` group with `open: true` starts expanded (used for "Still open").

## Fun stuff (spoilers)

- **Card set:** edit `cardSet` and `cardPacks` in `index.html`. Card fields: `id`, `emoji`, `name`, `rarity` (`common`, `uncommon`, `rare`, `holo`, `secret`), `fact`, `spot`. Pack fields: `id`, `emoji`, `label`, `day` (the trip day it unlocks; leave out for "open now"), `opens`, `cards`. The never-invent-facts rule applies to card facts too: check each one against a source and hedge where sources differ.
- **Secret rare:** the `secret` card isn't in a pack. Tapping Bigfoot in the hero treeline (left of Mt. Hood) awards it.
- **Hidden taps:** the "Portland 2026" title five times (rose shower); any day's weather bar (rain).
- **Celebrations:** ticking the last packing item, ticking "Pick up the wine allocation", and completing the 12-card set.
- Animations are skipped when the phone has Reduce Motion on. Saved state: `pdx-cards` and `pdx-set-done` in localStorage.

## How to redeploy

There are two copies, the same setup as Victoria:

- **Editing copy:** `C:\Users\hensl\OneDrive\Desktop\Portland Travel App`. Edit here.
- **Deploy copy:** `C:\Users\hensl\repos\portland-2026`. A git clone of the GitHub repo.

1. Edit `index.html` (and anything else) in the editing copy.
2. **Bump `CACHE_NAME`** in `sw.js`.
3. Add a line to the version history in `docs/KNOWN-ISSUES.md`.
4. Check it:
   ```bash
   node --check sw.js
   # index.html's script is inline: extract it, then check it
   node -e "const h=require('fs').readFileSync('index.html','utf8');require('fs').writeFileSync(require('os').tmpdir()+'/pdx-app.js',h.split('<script>')[1].split('</script>')[0])"
   node --check "%TEMP%\pdx-app.js"
   python -m http.server 8000   # open http://localhost:8000/ with DevTools phone view (~390 px wide)
   ```
5. Copy to the deploy copy, commit, push (Command Prompt):
   ```cmd
   robocopy "C:\Users\hensl\OneDrive\Desktop\Portland Travel App" "C:\Users\hensl\repos\portland-2026" /E /XD .git
   cd C:\Users\hensl\repos\portland-2026
   git add -A
   git status
   git commit -m "Short description of the change"
   git push
   ```
   If `git push` asks for a password, run `gh auth token` and paste its output.
6. Wait 30–60 s, open the live URL, and hard-reload (Ctrl+Shift+R). The footer should say **`App version: vN ✓`** with the new number.
7. On the phones: fully close the app and reopen it. If the footer says `Installed: vX · Latest: vY`, close and reopen once more.

### First-time setup (already done Oct 13, 2026)

```cmd
gh repo create 1davidhensley/portland-2026 --public --description "Portland OR trip PWA - Nov 2026"
gh api repos/1davidhensley/portland-2026/pages -X POST -f "source[branch]=main" -f "source[path]=/"
```

## Installing on the phones

- **iPhone (Safari):** open the live URL → Share → *Add to Home Screen*.
- **Android (Chrome):** open the live URL → ⋮ menu → *Install app* / *Add to Home screen*.
- Open it once while online so everything is cached for offline use.

## Troubleshooting

**A phone still shows the old version.** Open https://1davidhensley.github.io/portland-2026/sw.js. If `CACHE_NAME` shows the new number, the deploy worked: fully close and reopen the app. If it shows the old number, Pages is still rebuilding; wait 2 minutes. If the number never changed, you forgot to bump it.
