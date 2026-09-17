# conductor-plugin-index

A public plugin index for [conductor](https://github.com/OTZro/conductor)'s Marketplace.

## Use it

```
CONDUCTOR_MARKETPLACE_INDEX_URLS=OTZro/conductor-plugin-index
```

Restart conductor; the listed plugins appear under Marketplace → Browse. You can also
install any plugin directly by pasting its repo into the "owner/repo or git URL" field —
an index is only a convenience list.

## Submit a plugin

Open a PR adding an entry to `index.json`:

```json
{
  "name": "your-plugin",
  "repo": "owner/your-plugin-repo",
  "description": "One line on what it does.",
  "tags": ["ui"]
}
```

`name` must match the `name` in your repo's root `conductor-plugin.json`, and versions are
git tags (`vX.Y.Z`). See `docs/marketplace/` in the conductor repo for the plugin layout.

Listing here is not an endorsement or a security review — installing a plugin runs its code.
