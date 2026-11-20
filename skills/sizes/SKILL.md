---
name: sizes
description: The sizes and specifications of medical devices (inner and outer diameter, length), or which devices have a size above or below a value. Use when the person types /sizes or asks for a device's dimensions.
argument-hint: <devices, or the size question>
---

# Sizes and specifications

The request: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `schema-measurements` and `pattern-get-item-measurements`.
2. Call `find` for the ids of the devices named.
3. Show a table: inner diameter, outer diameter and the one insertable length, per size, as the IFU states them (inches and cm; convert nothing). A missing figure reads "no data".
4. For a question across a category or a maker, query the graph, keep the rows on the server with `save_as`, and show the rows that answer it.

Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
