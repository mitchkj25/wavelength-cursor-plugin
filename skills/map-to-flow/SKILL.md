---
name: map-to-flow
description: Map a file, a function, a service, or a pipeline in this repo as a Wavelength process flow. Use when the user asks to diagram, map, chart, or document how code works.
---

# Map code to a Wavelength flow

## When to use

- The user asks to diagram, map, or chart a code path, a request flow, a job, or a pipeline.
- The user wants a flow diagram for onboarding, a design review, or a README.

## Instructions

1. Read the code that the user names. Follow calls into other files only as far as the user asks.
2. Build the graph yourself. Use one node for each step and one decision node for each branch (if, switch, try/catch, early return).
3. Use these node types: start, step, decision, system (external services and APIs), data (databases, queues, files), actor (people or teams), and end (one end node for each distinct return or outcome).
4. Give each decision exactly two or more labeled edges, for example Yes and No.
5. Put the function name or the file and line in each node note, so readers can find the code.
6. Call the Wavelength tool create_flow_from_graph with the nodes and edges. This saves the exact graph with no AI rewrite.
7. Tell the user the node and edge counts and give the link that the tool returns.
8. If the user wants the diagram in the repo, call export_flow with format "mermaid" and write the result in a mermaid code block. Do not commit unless the user asks.

## Rules

- Do not invent steps that are not in the code. If a branch is unclear, add a note on the node.
- Do not send secrets, keys, or customer data to Wavelength. Send only the flow.
