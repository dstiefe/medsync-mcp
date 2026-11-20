---
name: compare
description: Compare two or more medical devices side by side: sizes, what each IFU says it is used with, and the labels. Use when the person types /compare or asks "compare A with B", "A versus B", "how does A differ from B". No verdict.
argument-hint: <device> and <device> [and <device> ...]
---

# Compare devices

The devices to compare: $ARGUMENTS

Call the `compare` tool of the MedSync devices connector once, with each device named as the person wrote it (for example `["Raptor 71", "Zoom 71"]`).

The tool shows the person a card with three tabs (Sizes, Compatibility, Label) and each device's documents. **The card is the answer.** Do not repeat its tables and do not summarize them: write one short sentence saying what was compared.

- Only if the person says no card appears, show the three tables from the tool's result exactly as given, then the documents links.
- Do not say which device is better, safer or preferable.
- Do not check whether the devices work together: that is a different question (`/works-with`).
- If a name was not found, or is a category rather than a device, say so plainly, with the closest match the tool gives.
- If fewer than two devices were given, ask which devices to compare.
