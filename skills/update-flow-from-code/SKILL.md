---
name: update-flow-from-code
description: Update an existing Wavelength flow after the code changes. Use when the user asks to sync, refresh, or update a diagram so it matches the current code.
---

# Update a Wavelength flow from code

## When to use

- The code changed and the user wants the saved flow to match it.
- A README contains a Mermaid diagram from Wavelength that is now out of date.

## Instructions

1. Find the flow with search_flows or list_flows, then read it with get_flow.
2. Read the current code and compare it with the flow.
3. Make exact changes with add_nodes, update_nodes, remove_nodes, add_edges, update_edges, and remove_edges. Do not rebuild the whole flow.
4. Tell the user what changed: nodes added, removed, and renamed.
5. If the repo has a Mermaid copy of the flow, export it again with export_flow and replace the old block.
