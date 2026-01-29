# Claude Code Feature Flags

Unofficial documentation of feature flags in [Claude Code](https://claude.ai/code) CLI.

> **⚠️ DISCLAIMER**
>
> This is **unofficial community documentation**. Not affiliated with or endorsed by Anthropic.
>
> - Feature flags can change or be removed without notice between versions
> - Enabling experimental flags may cause unexpected behavior
> - Some flags require specific plans or OAuth scopes
> - Use at your own risk

---

## How It Works

Claude Code uses feature flags to control access to new and experimental features. These are cached locally in `~/.claude.json` under `cachedGrowthBookFeatures`.

### Enabling Features

Edit `~/.claude.json` and modify the flag value:

```json
{
  "cachedGrowthBookFeatures": {
    "tengu_claudeai_mcp_connectors": true
  }
}
```

Restart Claude Code after making changes.

> **Note:** Anthropic may override local changes when syncing with their servers.

---

## Feature Flags Reference

### Integration Features

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_claudeai_mcp_connectors` | `false` | Claude.ai hosted MCP servers. Requires OAuth with `user:mcp_servers` scope |
| `tengu_chrome_auto_enable` | `false` | Auto-enable Chrome extension integration |

### Memory & Sessions

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_session_memory` | `false` | Persistent memory across sessions |
| `tengu_sm_compact` | `false` | Smart compaction with memory extraction |
| `tengu_coral_fern` | `false` | Access past sessions from current conversation |

### Planning & Workflow

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_plan_mode_interview_phase` | `false` | Interview/clarification phase before planning |
| `tengu_scratch` | `false` | Scratch/draft workspace feature |

### File Operations

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_marble_kite` | `false` | Skip "must read file before writing" validation |
| `tengu_file_write_optimization` | `false` | Shorter file write confirmation messages |

### API & Performance

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_streaming_tool_execution2` | `true` | Stream tool execution |
| `tengu_bash_haiku_prefetch` | `true` | Prefetch with Haiku for bash commands |
| `tengu_compact_cache_prefix` | `true` | Cache prefix optimization |
| `tengu_system_prompt_global_cache` | `false` | Global caching for system prompts |

### Extended Thinking

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_marble_anvil` | `true` | Keep all thinking blocks |
| `tengu_workout` | `false` | Effort/thinking level controls |

### Premium Features

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_brass_pebble` | `false` | Agent swarms - requires max/team plan with extra usage |

### UI & UX

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_code_diff_cli` | `true` | Diff view in CLI |
| `tengu_pr_status_cli` | `true` | PR status in footer |
| `tengu_permission_explainer` | `true` | Explain permission requests |
| `tengu_keybinding_customization_release` | `true` | Custom keybindings |
| `tengu_thinkback` | `false` | `/think-back` - Year in review animation |

### Search

| Flag | Default | Description |
|------|---------|-------------|
| `tengu_mcp_tool_search` | `true` | Search across MCP tools |

---

## Environment Variables That Disable Flags

Feature flags are automatically disabled if any of these are set:

```bash
DISABLE_TELEMETRY=1
CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC=1
CLAUDE_CODE_USE_BEDROCK=1
CLAUDE_CODE_USE_VERTEX=1
```

---

## Contributing

Found a new flag or figured out what one does? Open a PR!

---

## Version

Tested on Claude Code **v2.1.25** (January 2026)

---

## License

MIT
