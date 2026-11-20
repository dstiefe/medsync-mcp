---
name: by-size
description: Find devices across a category by a size above or below a value, such as aspiration catheters with an inner diameter of 0.071 inch or more. Use when the person types /by-size or asks which devices have a size above or below a value.
argument-hint: <kind of device and the size condition>
---

# Devices by size

The request: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `schema-measurements` and `pattern-get-item-measurements`.
2. Write one Cypher with `run_cypher` over the category's devices and their sizes, saving the rows with `save_as`. Then count and filter with `run_sql`.
3. Show a table: device, size, inner diameter, outer diameter, insertable length, as the IFU states them (inches and cm; convert nothing).

Rules:
- The length is the one insertable length. A missing figure reads "no data", never zero.
- Say what you searched ("every active aspiration catheter"), and take every count from a query result.
- Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
