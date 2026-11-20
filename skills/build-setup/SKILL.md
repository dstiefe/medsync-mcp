---
name: build-setup
description: Check a whole stack of devices used together, outer to inner, and show it as a card: what works, which pair fails and why. Use when the person types /build-setup or lists two or more devices or categories to use together.
argument-hint: <device>, <device>, <device> ...
---

# Build a setup

The devices: $ARGUMENTS

Use the MedSync devices connector:

1. Call `find` for every device or category named. Use ids, never guessed names, and say which device you took a close match for.
2. Call **`setup_card`** with all of them, each as `{"words": "<as the person said it>", "id": "<from find>"}`. Order does not matter: the card finds the order, outermost first. It works for any number of devices and for whole categories.

**The card is the answer.** It shows one column per thing, outer to inner, what works, what fails and why, and the documents. Write one or two short sentences: what was set up, and whether every combination works. Do not repeat the columns in a table, and do not call `connect` unless the person asks you to explain one pair or one setup in detail (then use `find`, `connect` and `run_sql`, with named devices or a small group).

Rules:
- A "no" always comes with why: the card gives the figure or the IFU's own words for each failing pair.
- "Could not calculate, no data" is not a failure.
- If the card does not appear, say so, and fall back to `connect` and `run_sql` with a small group.
- Take every count from a tool result, never from your own tally.
