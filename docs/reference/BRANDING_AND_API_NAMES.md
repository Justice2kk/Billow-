# Nidomo identity and current API names

**Nidomo** is the current platform name, following **Cielori** and originally **BillowOS**. The mascot is **Nimo** (formerly **Billo**); older demo-user/package vocabulary used **billock**, now **nidomi**.

## Clean-break technical identity

Nidomo deliberately reset its runtime identity and persistent platform namespaces rather than migrating old Billow OS user data. The **current** names creators should use are:

| Area | Current Nidomo contract |
| --- | --- |
| Platform and ecosystem | **Nidomo OS**, **Nidomo Web**, **Nidomo Store**, **Nidomo Creator** |
| Site/Browser addresses | `nidomo://` |
| SDK import namespace | `@nidomo/*` (for example `@nidomo/app`, `@nidomo/files`) |
| First-party package/service identities | `org.nidomo.*` |
| Creator project manifest | `nidomo.project.json` |
| Local workspace state | `.nidomo/` |
| Nidomo HTML form bindings | `data-nidomo-service`, `data-nidomo-action` |
| Mascot | **Nimo** |
| Demo-user/package vocabulary | **nidomi** |

The former `billow://`, `@billow/*`, `org.billow.*`, `billow.project.json` and `.billow/` identifiers are **not** the current creator contract. Do not begin new projects using them; do not assume an old URI, installed package, workspace or saved data can be reopened under the new identity.

This decision does **not** imply that old Roblox DataStores were physically deleted. The new runtime uses isolated storage namespaces instead, so abandoned pre-Nidomo data is not part of the current user environment.

### Development and availability

The public documentation describes supported concepts and currently defined contracts, **not** a claim that every feature is generally released in Roblox. Some code paths or sample projects may be limited, experimental or only internally tested. Check the [compatibility index](../compatibility/FEATURES.md) for each feature's actual documented status.

The history of Cielori and BillowOS remains in the [changelog](../../CHANGELOG.md); those names are historical context, not alternate active SDKs.

[← Public repository](../../README.md) · [Compatibility checklist](../compatibility/CHECKLIST.md)
