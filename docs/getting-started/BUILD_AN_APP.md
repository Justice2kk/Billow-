# Make something with Billow applications

A website is one way to create. An **application** is another: an installed Billow program that can use windows, files, app-owned storage and other permitted services.

You shouldn't need to become a Roblox engine programmer just to understand the app model.

## Pick a language

| Language | Why you might choose it |
| --- | --- |
| **TypeScript** | The default Billow Creator authoring language. |
| **JavaScript** | Familiar if you already build for the web. |
| **Luau** | Familiar if you already create Roblox experiences. |

The core project has accepted internal Check / Build / Run flows and a Creator → Store application lifecycle. That does **not** mean a public external SDK or general-purpose command-line tool is available for download here.

## What an app can work with

Instead of grabbing arbitrary Roblox engine objects, apps use **Billow-owned APIs**:

| I want my app to… | Look at |
| --- | --- |
| Know how it was launched | [`@billow/app`](../applications/README.md) |
| Show a window | [`@billow/windows`](../applications/README.md) |
| Open an allowed file | [`@billow/files`](../applications/README.md) |
| Save its own settings/data | [`@billow/storage`](../applications/README.md) |
| Talk to a permitted service | [`@billow/ipc`](../applications/README.md) |

The exact API shape, granted capabilities and runtime availability depend on the accepted Billow application contract.

## A sensible first app

Start small: one window, a readable interface, and one action that gives honest feedback. Then add persistent state or file access only when necessary.

Inside a supported Creator/Loom environment, the workflow is conceptually:

**Create project → write source → Check → Build → Run → test → publish when eligible.**

We intentionally aren't inventing an `npm install` command or project manifest for public users here. Those instructions will belong in this guide when there is a documented, distributable public toolchain.

## A couple of important boundaries

- A manifest asking for permission does **not** automatically grant it.
- App and file handles are not Roblox Instances.
- Publishing an app is not equivalent to bypassing the Store's validation and trust rules.
- Standard TypeScript or JavaScript knowledge helps, but the runtime is **not Node.js or a browser tab**.

[Application API guide →](../applications/README.md) · [Compatibility reference →](../compatibility/FEATURES.md)

[← Back to getting started](OVERVIEW.md)
