---
name: indicated-for
description: List the devices whose label covers a clinical situation (an occlusion site, a time window, a population). Use when the person types /indicated-for or asks "which devices are indicated for M2 within 8 hours".
argument-hint: <the situation, for example M2 within 8 hours>
---

# Indicated for

The situation: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `02-label-information`.
2. Query the graph for the indications that match, with `run_cypher` (`pattern-get-item-indications` and `schema-indications-anatomy` show how), saving the rows with `save_as`, then `run_sql` over them.
3. List each device with the indication that covers the situation.

Rules:
- Test each indication on its own: everything asked (the site, the time, the population) must hold inside one indication.
- A site in a vessel covers the vessels under it. A condition the label does not state reads "no information provided". A condition not met is a warning, never a reason to drop the device.
- Say which kind of time each label counts from (symptom onset, last known well).
- Quote the IFU's own words for each indication.
- Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
