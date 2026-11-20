---
name: works-with
description: Whether medical devices fit or work together, or what works with a device (fit by the numbers, and what each IFU says). Use when the person types /works-with or asks "can I use A with B", "what works with A".
argument-hint: <devices, or the question>
---

# Do these work together

The devices or question: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `00-works-together-overview`.
2. Call `find` for the ids of the devices named. Use ids, never guessed names, and say which device you took a close match for.
3. Call `connect`, then `run_sql` over the tables it built. Keep the rows on the server and take every count from a query result, never from your own tally.

Rules:
- Fit (the math), compatibility (what an IFU states) and label information are three different things: do not mix them.
- A "no" always comes with why: the figure, or the IFU's own words. "Could not calculate, no data" is not a failure.
- Answer the outcome first, then the reason.
- Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
