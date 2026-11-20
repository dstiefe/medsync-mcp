---
name: label
description: What a device's label (IFU) says: an indication, an occlusion site, a time window, or a patient case. Use when the person types /label or asks "is X indicated for ...", "what does the IFU say about ...".
argument-hint: <the label question>
---

# What does the label say

The question: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `02-label-information`.
2. Call `find` for the ids of the devices named.
3. If devices must also work together, find those first (`connect`), then check their labels with `run_sql`.

Rules:
- Test each indication on its own: everything asked must hold inside one indication.
- A condition that is not met is a warning, never a reason to drop a device. A label that does not state it reads "no information provided".
- Say which kind of time each label counts from (symptom onset, last known well).
- Quote the IFU's own words, and list what else the indication states.
- Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
