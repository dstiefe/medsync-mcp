---
name: documents
description: Give the documents we hold for a device: its IFU, 510(k) and website links. Use when the person types /documents or asks for the IFU or 510(k) of a device.
argument-hint: <device> [and <device> ...]
---

# Documents for a device

The devices: $ARGUMENTS

Call `find` of the MedSync devices connector with each name. For every device found, show its `documents_line` exactly as the tool gave it, one line per device.

- Never write or guess a link. A device with no line has no documents held: say so.
- A close match is a guess: say which device you took it for.
- Add nothing else unless the person asks.
