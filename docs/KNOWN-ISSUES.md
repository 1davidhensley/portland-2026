# Portland 2026 Trip App — Known Issues

## Open

### 15. Old Saturday 3:00 PM Guardian Games slot may still be booked
- **Status:** Open (settle before Fri Nov 13)
- **Details:** The One Piece evaluation was rebooked for Fri Nov 13 4:15–4:45 PM. The original Sat Nov 14 3:00–3:30 PM appointment (under Paula's name) has no cancel link in its invite. The store's Nov 11 email still lists it. Shown in Resources → Still open with the store's phone number.
- **Fix when done:** remove the row from Still open.

### 16. Friday evening is tight after the 5:00 evaluation
- **Status:** Open (David to confirm the plan)
- **Details:** The fourth evaluation runs 5:00–5:30 PM and Dolly Olive is at 6:30 with a 10-minute grace period. v10 assumes: leave the store about 5:40, quick check-in about 5:55, walk at 6:15. These times are estimates, not bookings. The store suggested bringing all four lists at 12:30, which may free the late slots, but that isn't guaranteed. Shown in Resources → Still open.

### 5. Saturday driver not decided
- **Status:** Open
- **Details:** No driver or car service is booked for the wine day. The v3–v5 hired-driver plan was dropped in v6. Shown as a TBD on the 9:30 AM stop, in the wine-day note, and in Resources → Still open.
- **Fix when decided:** delete the `tbd`, update the Saturday `note`, and remove the row from Still open. Don't put a booking number or price in the app.

### 13. Saturday lunch and dinner not booked
- **Status:** Open
- **Details:** Lunch (~1:45 PM, planned for Washington Square mall by the LEGO Store) and dinner are both unbooked. Bacchus Bar, Ruse Brewing, Mox and the LEGO Store are listed under Resources → Ideas.

### 14. Hotel wine hour time unknown
- **Status:** Open (ask at the desk)
- **Details:** The Kimpton hosts a daily wine hour; the booking email doesn't give a time.

### 4. What does the property credit cover?
- **Status:** Open (ask at check-in Fri)
- **Details:** The credit applies once per stay and can't go on the room rate, taxes, fees or tips. Whether it covers valet isn't confirmed. Shown as a checklist item on the Friday 5:15 PM check-in stop.

### 6. Site is public
- **Status:** By design
- **Details:** GitHub Pages sites are public. The app has no confirmation numbers, prices, card details, or email addresses. Dollar amounts for the hotel credit and the Guardian Games store credit are left out on purpose. Keep it that way.

## Resolved

### Which list goes in which Guardian Games slot (was #9)
- **Fixed in v8 (2026-11-10):** All three evaluations are on Fri Nov 13: 12:30–1:30 PM Paula's main list (under David's name), 2:00–3:00 PM the list approved Nov 9 (under Paula's name), 4:15–4:45 PM David's One Piece list (under David's name). The Sat 5:30 PM slot was a duplicate of the Nov 9 list and was cancelled. See open item 15 for the old Sat 3:00 slot.

### Friday 2:30 PM arrival vs 4:00 PM check-in (was #10)
- **Closed in v8 (2026-11-10):** Check-in is now about 5:15 PM, after Guardian Games.

### Friday dinner logistics (was #11)
- **Closed in v8 (2026-11-10):** The car goes to hotel valet at check-in; walk to Dolly Olive at 6:15 (0.4 mi).

### In-N-Out Vancouver and Columbia Sports Cards details unverified (were #12 and #7)
- **Closed in v8 (2026-11-10):** Both stops, and ORB, were dropped from Friday and moved to Resources → Ideas, with their "not verified" notes kept.

### Guardian Games trade-in appointments not booked (was #8)
- **Fixed in v6 (2026-11-09):** The October approvals were cancelled when the trip moved a week. The lists were resubmitted and approved Nov 7 (1 hr + 30 min) and Nov 9 (1 hr), and appointments are booked for Fri Nov 13 and Sat Nov 14. Four slots are booked; see open item 9 for which list goes where.

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
| v6 | 2026-11-09 | Trip moved to **Fri Nov 13 – Sun Nov 15**; hotel changed to the **Kimpton Hotel Vintage** (422 SW Broadway). Friday rebuilt from Paula's Nov 9 email: leave ~8:00, Columbia 11:00, In-N-Out Vancouver 12:00, ORB 1:00, hotel ~2:30, Guardian Games evaluation 5:00–6:00, Dolly Olive 6:30. Saturday: wineries, back to the hotel, Guardian Games evaluations at 3:00, 4:00 and 5:30; hired driver, LEGO Store and Ruse dropped (LEGO and Ruse moved to Ideas). Sunday: Powell's optional, late check-out to 4 PM. New "Still open" and Guardian Games panels in Resources; packing list rewritten. Day notes are now data (`note`), and resource groups can be `open`. |
| v7 | 2026-11-09 | Portland theming and fun: hero art (Mt. Hood, fir treeline), the **Rose City Card Set** (12 fact cards in 4 packs: one open now, one per trip day, plus a hidden secret rare), a "Cards" nav pill, and celebrations for a finished packing list, the Anacréon pickup and a full set. No itinerary changes. Card facts were checked on Nov 9 against Wikipedia, the Oregon Encyclopedia, the Portland Water Bureau, Oregon Wine Board and local news (KOIN, KPTV, KATU); the Powell's, In-N-Out and Mt. Hood cards are from general knowledge and weren't re-checked. |
| v8 | 2026-11-10 | From David's Nov 10 plan and the updated Calendly invites: **all three Guardian Games evaluations moved to Friday** (12:30, 2:00, 4:15). Friday rebuilt: drive straight to Guardian Games on I-5 (arrive 12:15), evaluations, spend the credit, check in ~5:15, walk to Dolly Olive at 6:15. Columbia Sports Cards, In-N-Out and ORB dropped from Friday and moved to Ideas. Saturday afternoon is free (Guardian Games stops removed). Still open, the Guardian Games panel and the trade-in packing list rewritten (three stacks, duplicate-card check). Three card-set cards reworded because they named the old I-205 route: the bridge card is now the I-5 Interstate Bridge. |
| v9 | 2026-11-10 | Saturday afternoon filled with Paula's earlier requests: **LEGO Store Washington Square** at 1:45 (with lunch at the mall, not booked) and **ORB Sports Cards** in Oregon City at 3:30, back at the hotel about 5:00. Both removed from Ideas. Columbia Sports Cards and In-N-Out stay in Ideas (Vancouver, WA is the wrong direction on Saturday; noted as Sunday drive-home options). Drive times are routing estimates without traffic. |
| v10 | 2026-11-11 | From the Nov 11 trade-in approval, the new Calendly invite and the store's Nov 11 reply: **fourth Guardian Games evaluation added, Fri 5:00–5:30 PM** (Pokémon list approved Nov 11, under David's name). Spend-the-credit moved to 5:30, check-in to about 5:55 (quick), walk to Dolly Olive still 6:15. Added the store's advice to bring all four stacks at 12:30. Still open gains a "Friday evening is tight" row; the Sat 3:00 row notes the store still lists it. Packing: fourth stack, "all four lists". |

## Lessons carried over from london-2026 / victoria-2026
- **Stale PWA cache:** bump `CACHE_NAME` on every content change. The footer version tag shows stale installs.
- **Truncated day cards:** keep `max-height: 50000px` on expanded day content.
- **`window.travelData` undefined:** use `typeof travelData`.
- **The SW must not cache live data:** Open-Meteo and `sw.js` are network-only.
