# Vessel Registry

The public registry of Vessel cargos. Fetched by the Vessel desktop app to populate the Marketplace.

## Registry Format

`registry.json` is a JSON array of entries. Each entry:

```json
{
  "id": "my-cargo",
  "name": "My Cargo",
  "author": "yourname",
  "description": "A short description shown in the Marketplace",
  "category": "productivity",
  "repo": "github.com/yourname/my-cargo",
  "latestVersion": "1.0.0",
  "downloadUrl": "https://github.com/yourname/my-cargo/releases/download/1.0.0/my-cargo.zip"
}
```

| Field | Description |
|-------|-------------|
| `id` | Unique identifier matching the `id` in the cargo's `manifest.json`. Lowercase letters, numbers, hyphens only. |
| `name` | Display name shown in the Marketplace. |
| `author` | Author or organization name. |
| `description` | One-sentence description shown in the Marketplace card. |
| `category` | Freeform category label (e.g. `productivity`, `development`, `utilities`). |
| `repo` | Source repository (display only, e.g. `github.com/yourname/my-cargo`). |
| `latestVersion` | Current version as semver (e.g. `1.0.0`). Used to detect updates. |
| `downloadUrl` | Direct HTTPS URL to the cargo `.zip` file. |

## Adding a Cargo

1. Fork this repo
2. Add your entry to `registry.json`
3. Open a PR — ensure your `downloadUrl` is publicly accessible
