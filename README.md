# Wavelength for Cursor

Map code paths, services, and pipelines from your repo as editable process flow diagrams in [Wavelength](https://wavelengthflow.com). Keep the diagram current as the code changes, and export it as Mermaid for your docs.

## What is included

- **MCP server**: the hosted Wavelength server at `https://wavelengthflow.com/api/mcp`. Sign-in uses OAuth with your Wavelength account.
- **Skill `map-to-flow`**: maps a file, a function, or a service as a flow with one node per step and one decision per branch.
- **Skill `update-flow-from-code`**: changes an existing flow to match the current code with exact graph edits.
- **Rule `wavelength`**: tells the agent when to use each Wavelength tool.

## Set up

1. Install the plugin from the Cursor Marketplace.
2. Open **Customize**, then **MCPs**. Turn on **wavelength** and click **Authenticate**.
3. Sign in with your Wavelength account and approve access. A free account works.

## Try it

- "Map src/checkout.js as a Wavelength flow."
- "Show my Wavelength flow Order checkout."
- "The retry logic changed. Update the Order checkout flow to match the code."
- "Export the flow as Mermaid and add it to README.md."

## Privacy and security

Wavelength does not read your code. Cursor reads the code on your machine and sends only the flow (node and edge text) to Wavelength. Each tool acts only as the signed-in user. Turn on Read-only mode in Wavelength Settings, then AI connector, to block all writes.

- Privacy policy: https://wavelengthflow.com/privacy.html
- Security: https://wavelengthflow.com/security.html
- Support: support@wavelengthflow.com

## License

MIT
