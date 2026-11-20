---
name: what-works-with
description: List the devices of a kind that work with a given device, shown as a card with the reason each works or does not. Use when the person types /what-works-with or asks "which sheaths work with the Raptor 71", "what can I use with X".
argument-hint: <device> [kind of device wanted]
---

# What works with a device

The request: $ARGUMENTS

Use the MedSync devices connector:

1. Call `find` for the device, and for the kind the person named (sheaths, microcatheters). Use ids, never guessed names.
2. Call **`setup_card`** with the device and the kind, each as `{"words": "<as the person said it>", "id": "<from find>"}`.

**The card is the answer.** It shows the device and the devices of that kind grouped by maker, which work with it, which do not, and why. Write one or two short sentences. Do not repeat the card in a table, and do not call `connect` unless the person asks you to explain one pair in detail.

Rules:
- Fit is the math on the sizes; compatibility is what an IFU states. The card already applies both, with MedSync's own rules.
- For a device that does not work, the card gives the reason: the figure, or the IFU's own words.
- If the card does not appear, say so, and fall back to `connect` and `run_sql`.
