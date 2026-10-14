# Portland 2026 Trip App — Known Issues

## Open

### 2. Fable Hobby hours unconfirmed
- **Status:** Open
- **Details:** Saturday 2:15 PM optional stop (4826 SW Scholls Ferry Rd). Shown with "⚠️ TBD: Hours unconfirmed".
- **Fix when known:** add the hours to `details` and delete `tbd`.

### 3. Ruse Brewing hours unconfirmed
- **Status:** Open
- **Details:** Saturday ~7:00 PM dinner at Ruse Brewing Crust Collective (1505 NW 21st Ave, (971) 888-5021). **No reservation on purpose**, so dinner can move earlier or later. Its website lists Sat 11:30 am–10 pm, but the site says it's being updated. Shown as a "Confirm before going" box.
- **Fix when known:** put the confirmed hours in `details` and delete `confirm`.

### 4. Does the property credit cover valet?
- **Status:** Open (ask at check-in Fri)
- **Details:** The plan is to use valet and put the hotel property credit toward it. The credit can't go on the room rate; valet isn't confirmed either way. Shown as a checklist item on the Friday 3:30 PM check-in stop and in Travel & Stay / Resources.
- **If it doesn't:** the credit can go toward Bellpine (20th floor) or the spa instead.

### 5. Saturday driver not booked
- **Status:** Open (book before Saturday)
- **Details:** Decided to hire a driver for the wine day (pickup ~9:35 AM at the hotel; Eminent Domaine → Anacréon → optional Fable Hobby → hotel). Shown as "⚠️ TBD: Driver not booked yet" on the 9:35 AM stop.
- **Fix when booked:** delete the `tbd`. Don't put the booking number or price in the app.

### 7. Columbia Sports Cards hours unverified
- **Status:** Open (low risk)
- **Details:** Card-shop directories that the store hasn't claimed list 10 am–7 pm weekdays (another says 10–5). Either way it should be open at the 1:00 PM visit.

### 6. Site is public
- **Status:** By design
- **Details:** GitHub Pages sites are public. The app has no confirmation numbers, prices, card details, or email addresses, and dollar amounts from the hotel perks and valet are left out on purpose. Keep it that way.

## Resolved

### Columbia Hobby & SportsCards address unconfirmed
- **Fixed in v3 (2026-10-14):** The store's website (columbiasportscard.com, "Visit us!") lists **15644 NE Fourth Plain Blvd, Vancouver, WA 98682** under the name Columbia Sports Cards & More. The 2707 NE 114th Ave address was dropped.

### Saturday dinner not decided
- **Fixed in v2 (2026-10-13):** Detroit-style pizza at Ruse Brewing Crust Collective in Slabtown. Bellpine and Mox were the earlier options; Mox moved to Resources → Ideas.

### Self-park garage not picked
- **Fixed in v2 (2026-10-13):** Using valet instead; the property credit is meant to cover it (see open item 4).

## Version history

| Version | Date | Change |
|---|---|---|
| v1 | 2026-10-13 | First release, built from the victoria-2026 template. Three days, Travel & Stay, Resources, Packing. |
| v2 | 2026-10-13 | Saturday dinner set to Ruse Brewing Crust Collective (Detroit-style pizza, Slabtown). Parking plan: valet, paid with the property credit. Mox moved to Ideas. |
| v3 | 2026-10-14 | Columbia address confirmed (15644 NE Fourth Plain Blvd). Saturday: hired driver instead of a designated driver (not booked yet). Ruse kept as a no-reservation, flexible-time dinner. |

## Lessons carried over from london-2026 / victoria-2026
- **Stale PWA cache:** bump `CACHE_NAME` on every content change. The footer version tag shows stale installs.
- **Truncated day cards:** keep `max-height: 50000px` on expanded day content.
- **`window.travelData` undefined:** use `typeof travelData`.
- **The SW must not cache live data:** Open-Meteo and `sw.js` are network-only.
