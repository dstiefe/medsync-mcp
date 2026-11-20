---
name: build-setup
description: Check a whole stack of devices used together, slot by slot, and show which pair fails and why. Use when the person types /build-setup or lists three or more devices to use together.
argument-hint: <device>, <device>, <device> ...
---

# Build a setup

The devices: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, `00-works-together-overview` and `04-the-tables-and-sql`.
2. Call `find` for every device, then `connect` with all of them. Order does not matter: `connect` finds the slots.
3. Call `run_sql` over the tables it built. Show the setups that work, as a table: one row per setup, one column per slot, with the sizes.

Rules:
- If a pair fails, name the pair and give the reason: the figure that does not fit, or the IFU's own words. A "no" always comes with why.
- A slot that an IFU says is needed, but the person did not name, is said in the answer, with the IFU's words. Offer it as a next step; do not add it silently.
- "Could not calculate, no data" is not a failure: name the device and the missing value.
- Take every count from a query result, never from your own tally.
- Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
