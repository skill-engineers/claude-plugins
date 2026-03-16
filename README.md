# Claude Plugins Marketplace

A monorepo of Claude Code plugins. Each sub-plugin lives under `plugins/` and is independently installable.

## Structure

```
.claude-plugin/
  plugin.json          # Root marketplace manifest (lists all sub-plugins)
plugins/
  content-writing/     # Content writing plugin (slide-outline skill)
    .claude-plugin/
      plugin.json
    skills/
      slide-outline/
        SKILL.md
        references/
```

## Plugins

| Plugin | Description |
|--------|-------------|
| [content-writing](./plugins/content-writing) | Slide outline planning skill for structuring compelling presentations |

## Adding a New Plugin

1. Create a new directory under `plugins/<plugin-name>/`
2. Add `.claude-plugin/plugin.json` with the plugin manifest
3. Add your components (`skills/`, `commands/`, `agents/`, `hooks/`)
4. Register the plugin in the root `.claude-plugin/plugin.json` under the `plugins` array
