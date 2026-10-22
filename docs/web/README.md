# Build for the Nidomo web

If you've made a website before, much of this will feel familiar.

**HTML** describes the page. **CSS** styles it. **Nidomo's Browser** displays it inside Roblox.

The difference is that Nidomo deliberately supports **a smaller, safer web profile**, plus its own `nidomo://` addresses and permission model.

## Start with a page, not a specification

[**Try the beginner walkthrough →**](../getting-started/BUILD_A_SITE.md)  
[**Quick compatibility checklist →**](../compatibility/CHECKLIST.md)  
[**Open the source example →**](../../examples/web/basic/)

## What you can work with

| Concept | Where to learn more |
| --- | --- |
| HTML content, links, buttons and images | [HTML profile](HTML.md) |
| CSS colors, typography, flex, spacing and responsive rules | [CSS profile](CSS.md) |
| JS/TS page behavior | [Feature-specific experimental coverage](../compatibility/FEATURES.md) |
| Nidomo addresses, navigation and routes | [`nidomo://` guide](../reference/URI_SCHEMES.md) |
| Exact supported vs. limited features | [Compatibility index](../compatibility/FEATURES.md) |

### Familiar isn't identical

A few intentional distinctions:

- No unrestricted access to Roblox Instances, services, remotes or DataStore.
- No arbitrary external networking from an untrusted page.
- No `innerHTML`-style dynamic raw-markup injection in the public page contract.
- No assumption that every browser DOM/CSS/JS feature works.
- Published sites are validated separately from their editable source.

**The important idea:** You can bring your HTML/CSS knowledge. Let the [compatibility guide](../compatibility/FEATURES.md) tell you exactly where Nidomo differs.

## What about JML and JSS?

Those are **legacy formats**. Existing historical content may still be readable, but new public authoring starts with **HTML and CSS**. See [JML](JML.md) and [JSS](JSS.md) only if you are dealing with an older project.

[← All documentation](../README.md)
