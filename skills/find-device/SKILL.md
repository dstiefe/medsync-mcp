---
name: find-device
description: Find a medical device by name in the MedSync graph, with the closest matches if the spelling differs, and its documents. Use when the person types /find-device or asks "do you have X", "is X in the data".
argument-hint: <device name>
---

# Find a device

The name: $ARGUMENTS

Call `find` of the MedSync devices connector with the name as the person wrote it.

- Show what was found: the device's name, its maker and category if the result gives them, and its documents line exactly as the tool gave it (`documents_line`).
- A close match is a guess: say which device you took it for, and list the other matches the tool returned.
- If nothing matches, say so plainly and give the closest names the tool returned. Never invent a device or a link.
- A name that is a category ("aspiration catheters") is not a device: say so and offer `/what-works-with` or `/by-size` instead.
