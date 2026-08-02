# toolkit.marketplace

A personal Claude Code plugin marketplace for consulting work. This repo acts as a plugin registry — Claude Code can point to it to discover and install agents built for client engagements.

## Adding this marketplace to Claude Code

```
/plugin marketplace add https://dev.azure.com/puterbaughcw/consulting/_git/toolkit.marketplace
```

Once added, Claude Code will be able to resolve plugins listed in `.claude-plugin/marketplace.json`.

## Installing plugins

After adding the marketplace, install individual plugins by name:

```
/plugin install architecture-lead
```

## Available plugins

| Plugin | Description |
|--------|-------------|
| `architecture-lead` | Principal-level architecture consulting persona: leads discovery sessions, generates design options with trade-off analysis, and produces client-ready decision briefs. |

## Adding a new plugin

1. Build the plugin in its own repo with a `.claude-plugin/plugin.json` manifest.
2. Add an entry to `.claude-plugin/marketplace.json` in this repo pointing at that repo's URL.
3. Commit and push — the marketplace entry is live immediately.
