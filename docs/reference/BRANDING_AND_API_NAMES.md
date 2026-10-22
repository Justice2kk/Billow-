# Nidomo's name and the existing API names

**Nidomo** is the current public-facing name of the platform, previously known as **Cielori** and originally **BillowOS**. **Nimo** is the mascot's current name (formerly **Billo**).

The product has a new identity, but a brand update does **not** automatically rename protocols, package imports, existing saved projects, or the underlying Roblox runtime. Creator code must continue to use the documented contracts until verified replacements exist.

| What you see | What to do right now |
| --- | --- |
| **Nidomo** | Current name of the platform, documentation and creator ecosystem. |
| **Nimo** | Current name of the mascot; older material may show Billo. |
| `billow://` | Use the existing documented URI scheme for now. Do **not** assume `nidomo://` has shipped. |
| `@billow/app`, `@billow/files`, etc. | Keep documented import specifiers until the runtime confirms compatible Nidomo equivalents. |
| `data-billow-service`, `data-billow-action` | Retain the accepted HTML form attributes until a supported migration is published. |
| `billow_extension`, registry field `billow`, `billow-public-preview-2026-10` | Existing compatibility schema/status/profile identifiers; **not** the current product name. |
| JML / JSS / `.bts` | Historical authoring formats. New web work should prefer HTML/CSS; new applications use the documented TypeScript-first path where available. |

**What has changed?** Public branding, community-facing language and names in guides and examples.

**What is not established by this repository?** That the executable runtime, API namespaces, URI schemes, saved files, asset identifiers or package IDs were all migrated concurrently. Do not rename technical identifiers in your own existing code simply because the project was rebranded.

For supported capabilities and their limitations, use the [public compatibility index](../compatibility/FEATURES.md) and [registry](../../compatibility/registry.json). A future API migration must be communicated with explicit compatibility and upgrade guidance.

[← Public repository](../../README.md) · [Compatibility checklist](../compatibility/CHECKLIST.md)
