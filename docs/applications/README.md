# Applications in Nidomo

An application is a thing you can launch, use and close—just like the apps you're used to. In Nidomo, it can also be something **you build**.

The accepted Creator workflow supports **TypeScript first**, with **JavaScript and Luau** as alternatives. Loom provides an in-platform creator workbench. Public authoring/tool availability can differ from the internally tested implementation.

[**New to making apps? Start here →**](../getting-started/BUILD_AN_APP.md)

## Meet the Nidomo APIs

Nidomo applications use controlled platform APIs rather than reaching into Roblox's engine directly.

| API | What it's for |
| --- | --- |
| `@nidomo/app` | App identity, launch information and lifecycle |
| `@nidomo/windows` | Windows owned by your app |
| `@nidomo/files` | Access to files you're allowed to use |
| `@nidomo/storage` | Your app's stored data/settings |
| `@nidomo/ipc` | Communication with permitted services |
| `@nidomo/notifications` | Notifications where granted |
| `@nidomo/clipboard` | Permission-scoped clipboard use |
| `@nidomo/logging` | Application diagnostics |

### An important rule

Having an API available is not the same as having **permission**. Nidomo grants capabilities for specific operations and resources. A guessed file ID or process number isn't permission; neither is an app manifest that simply requests broad access.

An app's window is not the same thing as its process or package. Those are distinct parts of the platform so apps can be managed safely and predictably.

The [compatibility index](../compatibility/FEATURES.md) is the public reference for individual language and API support claims.

## What isn't this?

It's **not** an npm package catalog, Node.js runtime, direct Roblox plugin API, or permission to run arbitrary Luau code inside other users' sessions. Public SDK/packaging commands will be documented when they are actually available.

[Platform overview →](../architecture/SYSTEM_OVERVIEW.md) · [Beginner guide →](../getting-started/BUILD_AN_APP.md)

[← All documentation](../README.md)
