# Make your first Nidomo page

You already know the best part: if you've seen HTML and CSS before, you can start with familiar ideas.

Nidomo's Browser renders a **bounded HTML/CSS profile** inside Roblox. It isn't a full copy of the regular web, so build from the small, documented set first.

## 1. Look at the example

The ready-to-read starter has just two files:

- [`index.html`](../../examples/web/basic/index.html) — what the page says and how it is organized.
- [`styles.css`](../../examples/web/basic/styles.css) — the colors, spacing, typography and layout.

[**Open the example folder →**](../../examples/web/basic/)

No build tools or secret framework needed to understand the example.

## 2. Change something you can see

Try editing the `<h1>` text in `index.html`, or the background color in `styles.css`. It's deliberately ordinary HTML/CSS so that what you learn carries over.

Here's the simplest idea:

```html
<main>
  <h1>My corner of Nidomo</h1>
  <p>I'm making something of my own.</p>
</main>
```

```css
main {
  max-width: 640px;
  padding: 24px;
  background-color: #f5f6ff;
}
```

## 3. Move into Sites when you have access

In a running Nidomo build that exposes the accepted Sites workflow, the general journey is **create a site project → edit → preview → build → publish inside Nidomo → open it in the Browser**.

The core project has tested that internal journey for static HTML/CSS. The exact entry screens and release availability may differ; this public repository doesn't provide an external CLI, installable template or imaginary publishing manifest.

Importantly, a *preview* is not the same thing as an approved public deployment. Publication has additional validation and permission steps.

## 4. Check what transfers from the web

Start with familiar tags, classes, flex layouts, colors and links. Check before using advanced CSS selectors, browser APIs, `iframe`, raw SVG, arbitrary network requests or JavaScript page behaviors.

- [HTML support](../web/HTML.md)
- [CSS support](../web/CSS.md)
- [Feature-by-feature compatibility](../compatibility/FEATURES.md)
- [How `billow://` works](../reference/URI_SCHEMES.md)

**Tip:** If a feature doesn't work, it may be outside Nidomo's current profile—not necessarily an error in your HTML.

[← Back to getting started](OVERVIEW.md)
