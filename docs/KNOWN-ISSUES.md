# Portland 2026 Trip App — Known Issues

## Open

### 1. Columbia Hobby & SportsCards address unconfirmed
- **Status:** Open
- **Details:** We have two addresses: **2707 NE 114th Ave Ste 3** or **15644 NE Fourth Plain Blvd**, both in Vancouver, WA. The app shows both as Maps buttons with a "Confirm before going" box. Call 360-635-4400 to check.
- **Fix when known:** in `index.html`, Friday 1:00 PM stop: replace `mapsLinks` with a single `mapsQuery`, delete `confirm`, and update the `exit` step in the 10:00 AM stop's `transportDir`.

### 2. Fable Hobby hours unconfirmed
- **Status:** Open
- **Details:** Saturday 2:15 PM optional stop (4826 SW Scholls Ferry Rd). Shown with "⚠️ TBD: Hours unconfirmed".
- **Fix when known:** add the hours to `details` and delete `tbd`.

### 3. Saturday dinner not decided
- **Status:** Open
- **Options:** **Bellpine** at the Ritz (20th floor, uses the property credit) or **Mox Boarding House** (1938 W Burnside St; restaurant + card shop; validates 90 min of parking). Shown side by side with "⚠️ TBD: Pick one".
- **Fix when decided:** replace `options` with the chosen place's `details` / `mapsQuery`, rename the stop, delete `tbd`.

### 4. Self-park garage not picked
- **Status:** Open
- **Details:** Ritz-Carlton valet has a daily fee; the self-park garage is TBD. Shown on the Friday 3:30 PM check-in stop and in Travel & Stay / Resources.

### 5. Saturday designated driver
- **Status:** Open (decide before Saturday)
- **Details:** Shown as a TBD on the 9:35 AM drive and in the wine-day note.

### 6. Site is public
- **Status:** By design
- **Details:** GitHub Pages sites are public. The app has no confirmation numbers, prices, card details, or email addresses, and dollar amounts from the hotel perks and valet are left out on purpose. Keep it that way.

## Version history

| Version | Date | Change |
|---|---|---|
| v1 | 2026-10-13 | First release, built from the victoria-2026 template. Three days, Travel & Stay, Resources, Packing. |

## Lessons carried over from london-2026 / victoria-2026
- **Stale PWA cache:** bump `CACHE_NAME` on every content change. The footer version tag shows stale installs.
- **Truncated day cards:** keep `max-height: 50000px` on expanded day content.
- **`window.travelData` undefined:** use `typeof travelData`.
- **The SW must not cache live data:** Open-Meteo and `sw.js` are network-only.
