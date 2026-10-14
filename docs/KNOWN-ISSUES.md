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

### 3. Ruse Brewing hours and reservations unconfirmed
- **Status:** Open
- **Details:** Saturday 7:00 PM dinner at Ruse Brewing Crust Collective (1505 NW 21st Ave, (971) 888-5021). Its website lists Sat 11:30 am–10 pm, but the site says it's being updated and doesn't mention reservations or parking. Shown as a "Confirm before going" box.
- **Fix when known:** put the confirmed hours / reservation in `details` and delete `confirm`.

### 4. Does the property credit cover valet?
- **Status:** Open (ask at check-in Fri)
- **Details:** The plan is to use valet and put the hotel property credit toward it. The credit can't go on the room rate; valet isn't confirmed either way. Shown as a checklist item on the Friday 3:30 PM check-in stop and in Travel & Stay / Resources.
- **If it doesn't:** the credit can go toward Bellpine (20th floor) or the spa instead.

### 5. Saturday designated driver
- **Status:** Open (decide before Saturday)
- **Details:** Shown as a TBD on the 9:35 AM drive and in the wine-day note.

### 6. Site is public
- **Status:** By design
- **Details:** GitHub Pages sites are public. The app has no confirmation numbers, prices, card details, or email addresses, and dollar amounts from the hotel perks and valet are left out on purpose. Keep it that way.

## Resolved

### Saturday dinner not decided
- **Fixed in v2 (2026-10-13):** Detroit-style pizza at Ruse Brewing Crust Collective in Slabtown. Bellpine and Mox were the earlier options; Mox moved to Resources → Ideas.

### Self-park garage not picked
- **Fixed in v2 (2026-10-13):** Using valet instead; the property credit is meant to cover it (see open item 4).

## Version history

| Version | Date | Change |
|---|---|---|
| v1 | 2026-10-13 | First release, built from the victoria-2026 template. Three days, Travel & Stay, Resources, Packing. |
| v2 | 2026-10-13 | Saturday dinner set to Ruse Brewing Crust Collective (Detroit-style pizza, Slabtown). Parking plan: valet, paid with the property credit. Mox moved to Ideas. |

## Lessons carried over from london-2026 / victoria-2026
- **Stale PWA cache:** bump `CACHE_NAME` on every content change. The footer version tag shows stale installs.
- **Truncated day cards:** keep `max-height: 50000px` on expanded day content.
- **`window.travelData` undefined:** use `typeof travelData`.
- **The SW must not cache live data:** Open-Meteo and `sw.js` are network-only.
