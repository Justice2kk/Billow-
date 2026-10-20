# Help make Cielori easier to understand

You don't need to be a kernel engineer to improve these public docs. A clearer example, a confusing explanation fixed, or a broken link repaired can make the next creator's day much easier.

## Good contributions

- Explain a confusing concept in ordinary language.
- Make a beginner example easier to follow without adding unsupported features.
- Repair broken links, typos and unclear navigation.
- Report missing context or an incorrect support claim.
- Suggest documentation for a real, confirmed public capability.

Before sending a pull request, explain **who the change helps and why**. A little context beats a wall of jargon.

## If you're changing a compatibility claim

Cielori's compatibility pages aren't hand-maintained checklists.

1. Update [`compatibility/registry.json`](compatibility/registry.json), including the corresponding evidence reference.
2. Run `python tools/validate_public.py --write` to regenerate the feature page.
3. Run `python tools/validate_public.py --check`.
4. Keep limitations explicit. A familiar API name does not prove full standard behavior.

[Feature index](docs/compatibility/FEATURES.md) · [Documentation hub](docs/README.md)

## Boundaries worth respecting

This is the **public documentation and examples repository**. Don't paste private implementation files, security-sensitive details, hidden service paths, credentials or unreleased internal procedures here.

Please don't claim that Cielori implements all of HTML, CSS, JavaScript or Roblox's engine APIs. Tie support claims to observable behavior and public compatibility evidence.

The [license status](LICENSE) is currently limited; public visibility is not a blanket license grant for Cielori's private code.

Thanks for helping make a creative platform feel approachable.
