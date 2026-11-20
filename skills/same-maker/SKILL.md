---
name: same-maker
description: List a manufacturer's devices, grouped by category. Use when the person types /same-maker or asks "what does Balt make", "which devices are from X".
argument-hint: <manufacturer>
---

# A maker's devices

The manufacturer: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `schema-products-items` and `pattern-get-item-details`.
2. Write one Cypher with `run_cypher` for the products of that manufacturer, saving the rows with `save_as`. Then group by category with `run_sql`.
3. Show a table: category, device, number of sizes held.

Rules:
- Only devices we hold are listed. Say what you searched and take every count from a query result.
- If the manufacturer is not found, say so and give the closest names the tool returned.
- Whenever you name a device, put its documents under it, one line per device, exactly as a tool gave it (`documents_line`). Never write or guess a link.
