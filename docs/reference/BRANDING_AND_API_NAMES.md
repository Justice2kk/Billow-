# Cielori's name and the existing API names

**Cielori** is the new public-facing name for the platform previously called **BillowOS**.

You'll still see the old name in a few technical identifiers. That doesn't mean this documentation is outdated: those identifiers are part of the current published compatibility vocabulary, and changing a name in Markdown does **not** change the underlying app/browser runtime.

| What you see | What to do right now |
| --- | --- |
| **Cielori** | The new platform and public-docs name. |
| `billow://` | Use it where the current routing contract requires it; don't assume `cielori://` works. |
| `@billow/app`, `@billow/files`, etc. | Keep the documented import names in code until a compatible runtime migration is announced. |
| `data-billow-service`, `data-billow-action` | Keep the current form attribute names for the same reason. |
| JML / JSS / `.bts` | Historical authoring formats. For new projects prefer HTML/CSS and TypeScript `.ts` where supported. |

**What's confirmed?** The project's name has changed. **What's not confirmed by this public repository?** That every API namespace, URI scheme, asset ID or installed package name has changed at the same time.

The [compatibility registry](../../compatibility/registry.json) and [full index](../compatibility/FEATURES.md) are the source for currently documented API names. Any future migrations should preserve clear compatibility guidance instead of silently breaking older projects.

[← Public repository](../../README.md) · [Compatibility checklist](../compatibility/CHECKLIST.md)
