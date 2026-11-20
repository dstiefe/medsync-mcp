---
name: what-works-with
description: List the devices of a kind that work with a given device, with the reason each works or does not. Use when the person types /what-works-with or asks "which sheaths work with the Raptor 71", "what can I use with X".
argument-hint: <device> [kind of device wanted]
---

# What works with a device

The request: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `00-works-together-overview`.
2. Call `find` for the device. If the person named a kind (sheaths, microcatheters), pass that as a second name so `connect` treats it as a group.
3. Call `connect`, then `run_sql` over the tables it built to list the devices that work, grouped by product with their sizes.

Rules:
- Fit is the math on the sizes; compatibility is what an IFU states. A pair works only if both agree, or the IFU's statement is met when there is no math. Say which.
- For each device that does not work, say why in one line: the figure, or the IFU's own words.
- Take every count from a query result, never from your own tally.
- Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
