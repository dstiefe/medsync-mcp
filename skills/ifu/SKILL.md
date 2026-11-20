---
name: ifu
description: Quote what a device's IFU says in one section, such as warnings, directions for use or contraindications. Use when the person types /ifu or asks "what does the IFU say about ...".
argument-hint: <device> <topic, for example warnings>
---

# What the IFU says

The request: $ARGUMENTS

Use the MedSync devices connector:

1. Call `wiki_pages` and read `start-here`, then `schema-documents`, `schema-document-sections` and `pattern-get-item-details`.
2. Call `find` for the device, then `run_cypher` for the section that matches the topic.
3. Quote the section in the IFU's own words. Do not paraphrase a warning.

Rules:
- If the IFU has no such section, say "the IFU has no section on that". That is a fact of the label, not an error.
- Give the document the words came from, and its link as the tool gave it (`documents_line`). Never write or guess a link.
