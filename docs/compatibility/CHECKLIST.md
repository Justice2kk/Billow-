# What works in Billow? ☑️

**The compatibility guide without the technical headache.** Wondering whether you can build something in BillowOS? Start here.

[**Making a website? ↓**](#websites-html) · [**Making an app? ↓**](#apps-and-programming) · [**Full technical list →**](FEATURES.md)

> **Reading the checklist**
>
> - **☑️ / `[x]`** — supported **within Billow's documented limits**. A check does *not* mean full browser compatibility.
> - **🧪** — experimental; the feature or public-facing behavior can change.
> - **☐ / `[ ]`** — not supported in the current profile. **Unchecked items are not a development to-do list.**
> - **🚫** — intentionally excluded for security or platform-design reasons.
> - **💠** — a Billow-specific feature rather than a standard browser API.
>
> This is a **curated overview** of the [public compatibility registry](../../compatibility/registry.json) (`billow-public-preview-2026-10`). The [full compatibility index](FEATURES.md) is the source for exact feature coverage, limitations and evidence. Internal tests do not mean every feature is already in a publicly playable release.

## Websites (HTML)

### ☑️ Things you can use

- [x] **Headings, paragraphs and basic text** — `h1`–`h6`, `p`, `span`, `strong`, `em` and similar elements.
- [x] **Page structure** — `main`, `header`, `nav`, `section`, `article`, `div`, etc.
- [x] **Lists** — `ul`, `ol` and `li`.
- [x] **Links** — `a`, as long as navigation is allowed by Billow.
- [x] **Images** — `img`, with approved resources plus valid `src` and `alt`.
- [x] **Buttons and text fields** — `button`, `label`, `textarea`, `input` (text/search only).
- [x] **Simple forms** — supported **only** through approved Billow service/action **POST** submissions.

### ☐ Not currently supported

- [ ] **Tables** — `<table>`.
- [ ] **Dropdown/select menus** — `<select>`.
- [ ] **Inline SVG or MathML** — `<svg>`, `<math>`.
- [ ] **HTML templates** — `<template>`.

🚫 **Arbitrary embedded websites (`iframe`)** are excluded on purpose.

[HTML guide →](../web/HTML.md) · [Every HTML feature →](FEATURES.md#html)

## Styling (CSS)

### ☑️ Things you can style

- [x] **Colors and typography** — color, font size, weight, line height and alignment.
- [x] **Spacing and shape** — margins, padding, gaps, borders and rounded corners.
- [x] **Flexible layouts** — supported flexbox properties, sizing and alignment.
- [x] **Images and layering** — bounded backgrounds, opacity, overflow and object fit.
- [x] **Common selectors** — element, class, ID, universal, descendant and child selectors.
- [x] **States** — `:hover`, `:focus`, `:disabled`, `:checked`, `:first-child` and `:last-child`.
- [x] **Basic responsive rules** — `@media` min/max-width queries in pixels.

### ☐ Not currently supported

- [ ] **CSS variables**, such as `--my-color`.
- [ ] **Nested CSS rules**.
- [ ] **Attribute selectors**, such as `[data-role="card"]`.
- [ ] **Pseudo-elements**, such as `::before` and `::after`.

**Heads-up:** Billow supports a *subset* of properties and values. For example, `px`, `%`, `vw` and `vh` exist only where the property accepts them. An ordinary CSS tutorial is a good starting point—not a guarantee.

[CSS guide →](../web/CSS.md) · [Every CSS feature →](FEATURES.md#css)

## Apps and programming

| Language | Status | What you should know |
| --- | --- | --- |
| **TypeScript** | 🧪 Public profile: experimental | Billow's **default** Creator-app language, with accepted internal workflows; public toolchain availability is a separate question. |
| **JavaScript** | 🧪 Public profile: experimental | Creator-app alternative, subject to the public runtime contract. |
| **Luau** | ☑️ Supported with limits | Supported inside Billow's controlled application runtime, **not** with unrestricted Roblox-engine access. |
| **JML, JSS and `.bts`** | ↩️ Legacy | Retained for compatibility/history. Start new sites in **HTML/CSS** and new TypeScript projects in `.ts`. |

### 🧪 Interactive websites

These kinds of page scripting exist but are **experimental** in the public compatibility profile:

- 🧪 Finding page elements (`getElementById`, `querySelector`).
- 🧪 Editing text, classes and attributes.
- 🧪 Listening to events.
- 🧪 Saving origin-scoped page data.
- 🧪 Same-origin requests and navigation.

These are controlled Billow **analogues**, not every browser DOM/JavaScript API.

[Start making an app →](../getting-started/BUILD_AN_APP.md) · [Language details →](FEATURES.md#language) · [Web APIs →](FEATURES.md#web-api)

## 💠 Billow-specific features

- 💠 **`billow://`** — Billow's own website addressing and routing, **not** ordinary Internet DNS.
- 💠 **Billow forms** — `data-billow-service` and `data-billow-action` for authorized POST actions.
- 💠 **App services** — `@billow/app`, `@billow/windows`, `@billow/files`, `@billow/storage`, `@billow/ipc`, `@billow/notifications`, `@billow/clipboard` and `@billow/logging`.

An API existing doesn't automatically grant your app permission to use it. Billow controls which resources and operations an app may access.

[Application API guide →](../applications/README.md) · [Billow-specific compatibility →](FEATURES.md#billow)

## 🚫 Not allowed by design

- 🚫 **`iframe`** with arbitrary embedded browsing contexts.
- 🚫 **`innerHTML`**-style unsafe raw-markup injection.
- 🚫 **Arbitrary cross-origin/external `fetch`** from untrusted pages.
- 🚫 **Direct Roblox Instances or services** from sandboxed public apps or pages.

These aren't just missing checkmarks. They are intentional platform boundaries.

## So… can I build that?

| I want to make… | Quick answer |
| --- | --- |
| A small personal website with images and links | ☑️ **Yes**, within the HTML/CSS profile. |
| A nice responsive page using flexbox | ☑️ **Yes**, with the supported values and width queries. |
| A form that submits data | ☑️ **With limits** — approved Billow service/action POST only. |
| A complex JavaScript-powered website | 🧪 **Maybe partly** — check each page API and available runtime. |
| A site that embeds another webpage | 🚫 **No** — arbitrary iframes are excluded. |
| A spreadsheet-like page using HTML tables | ☐ **Not with `table`** in this profile. |
| An application with its own window and storage | 💠 **Billow-native**, subject to Creator availability and granted permissions. |

**Want an exact answer?** Find the specific element, property or API in the [full feature index](FEATURES.md).

[← Compatibility hub](README.md) · [All docs](../README.md) · [Make a website →](../getting-started/BUILD_A_SITE.md)
