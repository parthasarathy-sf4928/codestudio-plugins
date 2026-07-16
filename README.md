# Agent Plugin Marketplace

Curated catalog of AI agent plugins for Code Studio's Engineering Workspace extension.

## Structure

```
plugins.json    — Plugin registry (fetched by the extension at runtime)
icons/          — Plugin icons (SVG)
```

## Plugin Entry Format

Each plugin in `plugins.json` has:

| Field           | Type     | Description                                         |
| --------------- | -------- | --------------------------------------------------- |
| `id`            | string   | Unique plugin identifier                            |
| `name`          | string   | Display name                                        |
| `description`   | string   | Short description                                   |
| `author`        | string   | Author name                                         |
| `version`       | string   | Semver version                                      |
| `icon`          | string   | Icon filename in `icons/`                           |
| `repository`    | string   | GitHub repo URL                                     |
| `keywords`      | string[] | Tags for search and recommendations                 |
| `category`      | string   | `"syncfusion"` \| `"community"` \| `"official"`     |
| `featured`      | boolean  | Show in featured section                            |
| `skillCount`    | number   | Number of skills in the pack                        |
| `installSource` | object   | Install info: `{ type: "git", repo: "owner/repo" }` |

## Adding a Plugin

1. Add an entry to `plugins.json`
2. Add an icon to `icons/` (SVG preferred, 32×32)
3. Commit and push — the extension fetches this file at runtime

## Used By

- [Engineering Workspace](https://github.com/praveen-hari/agentic_engineer) — Code Studio extension for AI-assisted SDLC workflows
