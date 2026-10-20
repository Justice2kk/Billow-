# URI schemes

## `billow://`

`billow://` is the logical addressing scheme for Cielori web routes/resources:

```text
billow://<authority>/<path>?<query>#<fragment>
```

It borrows familiar URI structure but does **not** imply raw DNS/TCP/TLS/socket access. Cielori resolves authorities through its own route/deployment platform and applies origin/security policy.

## `res://`

`res://` identifies Cielori-managed resources where symbolic resource references are exposed. The platform resolves them through trusted resource policy before producing any host-specific locator. A Roblox asset ID is provider data, not a durable Cielori file identity.
