# Portland 2026 Trip App — Known Issues

## Open

### 9. Extra Saturday Guardian Games slot (5:30–6:30 PM)
- **Status:** Open (decide before Sat Nov 14)
- **Details:** Four Calendly appointments are on the calendar for three approved lists: Fri Nov 13 5:00–6:00 PM (1 hr, under Paula's name, booked Nov 9), Sat Nov 14 3:00–3:30 PM (30 min, under Paula's name), Sat 4:00–5:00 PM (1 hr, under David's name) and Sat 5:30–6:30 PM (1 hr, under David's name, booked Nov 9 an hour before the Friday one). Paula's Nov 9 email puts the new trade-in on Friday 5–6, so the Saturday 5:30 slot looks like a leftover. The app shows it as an optional stop with a "decide before Saturday" box.
- **Fix when known:** if it was cancelled, delete the 5:30 PM stop and the "Extra Saturday slot" row in Resources → Still open. If it's real, say which list it's for.

### 10. Friday 2:30 PM arrival vs 4:00 PM check-in
- **Status:** Open (ask at the desk Fri)
- **Details:** Paula's Nov 9 email has check-in "around 2:30 pm" (she wrote "Ritz"; the booking is the Kimpton Hotel Vintage, rebooked Oct 28). Kimpton check-in is 4:00 PM; early check-in is a card perk only if a room is ready.

### 11. Friday dinner logistics
- **Status:** Open
- **Details:** The Guardian Games appointment ends at 6:00 PM (SE Taylor St) and Dolly Olive is at 6:30 PM downtown with a 10-minute grace period. Where the car goes (hotel valet then a 0.4 mi walk, or parking near the restaurant) isn't decided. Shown as a TBD on the 6:00 PM stop.

### 12. In-N-Out Vancouver details unverified
- **Status:** Open (low risk)
- **Details:** Paula asked for lunch at In-N-Out in Vancouver, WA at 12:00. The address (13511 SE 3rd Way) comes from news reports of the April 2026 opening, not from In-N-Out's own site. Shown with a confirm box.

### 5. Saturday driver not decided
- **Status:** Open
- **Details:** No driver or car service is booked for the wine day. The v3–v5 hired-driver plan was dropped in v6. Shown as a TBD on the 9:30 AM stop, in the wine-day note, and in Resources → Still open.
- **Fix when decided:** delete the `tbd`, update the Saturday `note`, and remove the row from Still open. Don't put a booking number or price in the app.

### 13. Saturday lunch and dinner not booked
- **Status:** Open
- **Details:** Lunch (~2:00 PM, back at the hotel) and dinner are both open. Bacchus Bar, Ruse Brewing, Mox and the LEGO Store are listed under Resources → Ideas.

### 14. Hotel wine hour time unknown
- **Status:** Open (ask at the desk)
- **Details:** The Kimpton hosts a daily wine hour; the booking email doesn't give a time.

### 4. What does the property credit cover?
- **Status:** Open (ask at check-in Fri)
- **Details:** The credit applies once per stay and can't go on the room rate, taxes, fees or tips. Whether it covers valet isn't confirmed. Shown as a checklist item on the Friday 2:30 PM stop.

### 7. Columbia Sports Cards hours unverified
- **Status:** Open (matters more since v6)
- **Details:** Card-shop directories that the store hasn't claimed list 10 am–7 pm weekdays (another says 10–5). The visit is now at 11:00 AM, an hour after the unverified opening, so the stop has a "call before you leave" box.

### 6. Site is public
- **Status:** By design
- **Details:** GitHub Pages sites are public. The app has no confirmation numbers, prices, card details, or email addresses. Dollar amounts for the hotel credit and the Guardian Games store credit are left out on purpose. Keep it that way.

## Resolved

### Guardian Games trade-in appointments not booked (was #8)
- **Fixed in v6 (2026-11-09):** The October approvals were cancelled when the trip moved a week. The lists were resubmitted and approved Nov 7 (1 hr + 30 min) and Nov 9 (1 hr), and appointments are booked for Fri Nov 13 and Sat Nov 14. See open item 9 for the extra slot.

### Ruse Brewing hours unconfirmed (was #3)
- **Closed in v6 (2026-11-09):** Ruse is no longer the Saturday dinner plan; it moved to Resources → Ideas with a "call to check hours" note.

### Fable Hobby hours unconfirmed
- **Fixed in v4 (2026-10-14):** Fable Hobby was dropped. Paula asked for Guardian Games (345 SE Taylor St) in its place. The hours come from the store's site (Sat 10 am–10 pm).

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
| v4 | 2026-10-14 | Paula's email: Guardian Games (SE Taylor) replaces Fable Hobby on Saturday. Added the LEGO Store at Washington Square on the Saturday drive back (2:15 PM). Added Powell's City of Books on Sunday at 10 AM and removed it from Ideas. Dropped Stumptown Otaku, so Powell's runs until check-out. The Saturday hotel rest moved to 4:30 PM. |
| v5 | 2026-10-25 | Guardian Games trade-in (30-min + 1-hr buylist evaluations, 3+ hrs): Saturday stop at 3:15 PM, no longer optional, with booking checklist and TBD. Driver drops off there. Cut the 4:30 hotel rest; Ruse moved to ~7:30. Friday backup plan added as a confirm box on Friday's 10:00 AM stop (Dolly Olive 6:30 unchanged). Trade-in cards added to Packing. |
| v6 | 2026-11-09 | Trip moved to **Fri Nov 13 – Sun Nov 15**; hotel changed to the **Kimpton Hotel Vintage** (422 SW Broadway). Friday rebuilt from Paula's Nov 9 email: leave ~8:00, Columbia 11:00, In-N-Out Vancouver 12:00, ORB 1:00, hotel ~2:30, Guardian Games evaluation 5:00–6:00, Dolly Olive 6:30. Saturday: wineries, back to the hotel, Guardian Games evaluations at 3:00 and 4:00; hired driver, LEGO Store and Ruse dropped (LEGO and Ruse moved to Ideas). Sunday: Powell's optional, late check-out to 4 PM. New "Still open" and Guardian Games panels in Resources; packing list rewritten. Day notes are now data (`note`), and resource groups can be `open`. |

## Lessons carried over from london-2026 / victoria-2026
- **Stale PWA cache:** bump `CACHE_NAME` on every content change. The footer version tag shows stale installs.
- **Truncated day cards:** keep `max-height: 50000px` on expanded day content.
- **`window.travelData` undefined:** use `typeof travelData`.
- **The SW must not cache live data:** Open-Meteo and `sw.js` are network-only.
