# Claude Code Environment Variables

Hidden environment variables that control Claude Code behavior.

> **Note:** These are undocumented variables discovered through code analysis. They may change between versions.

---

## Model Overrides

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_SUBAGENT_MODEL` | Override the model used for subagents/Task tool |
| `ANTHROPIC_MODEL` | Override the default model |
| `ANTHROPIC_DEFAULT_SONNET_MODEL` | Override Sonnet model version |
| `ANTHROPIC_DEFAULT_OPUS_MODEL` | Override Opus model version |
| `ANTHROPIC_DEFAULT_HAIKU_MODEL` | Override Haiku model version |
| `ANTHROPIC_SMALL_FAST_MODEL` | Override the "small fast" model (used for prefetch, etc.) |

**Example:**
```bash
CLAUDE_CODE_SUBAGENT_MODEL=claude-sonnet-4-20250514 claude
ANTHROPIC_SMALL_FAST_MODEL=claude-haiku-4-5-20251001 claude
```

---

## API Beta Features

Use `ANTHROPIC_BETAS` to enable experimental API features (comma-separated):

```bash
ANTHROPIC_BETAS=tool-examples-2025-10-29,web-search-2025-03-05 claude
```

### Available Betas

| Beta | Description |
|------|-------------|
| `interleaved-thinking-2025-05-14` | Interleaved thinking blocks |
| `context-1m-2025-08-07` | 1M token context window (Sonnet) |
| `context-management-2025-06-27` | Automatic context management |
| `structured-outputs-2025-12-15` | Structured/typed outputs |
| `web-search-2025-03-05` | Web search capability |
| `tool-examples-2025-10-29` | Tool usage examples in prompts |
| `advanced-tool-use-2025-11-20` | Advanced tool use features |
| `tool-search-tool-2025-10-19` | Tool search functionality |
| `effort-2025-11-24` | Effort/thinking level controls |
| `prompt-caching-scope-2026-01-05` | Enhanced prompt caching |
| `fine-grained-tool-streaming-2025-05-14` | Streaming for tool use |

---

## Security

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_DISABLE_COMMAND_INJECTION_CHECK` | Disable command injection security checks in bash |
| `CLAUDE_CODE_ADDITIONAL_PROTECTION` | Enable additional security protections |

---

## Prompt Caching

| Variable | Description |
|----------|-------------|
| `DISABLE_PROMPT_CACHING` | Disable all prompt caching |
| `DISABLE_PROMPT_CACHING_OPUS` | Disable caching for Opus model only |
| `DISABLE_PROMPT_CACHING_SONNET` | Disable caching for Sonnet model only |
| `DISABLE_PROMPT_CACHING_HAIKU` | Disable caching for Haiku model only |

---

## Compaction & Memory

| Variable | Description |
|----------|-------------|
| `DISABLE_AUTO_COMPACT` | Disable automatic context compaction |
| `DISABLE_COMPACT` | Disable compaction entirely |
| `DISABLE_MICROCOMPACT` | Disable micro-compaction |
| `ENABLE_CLAUDE_CODE_SM_COMPACT` | Enable session memory compaction |
| `DISABLE_CLAUDE_CODE_SM_COMPACT` | Disable session memory compaction |
| `CLAUDE_AUTOCOMPACT_PCT_OVERRIDE` | Override auto-compact threshold percentage |

---

## Thinking & Effort

| Variable | Description |
|----------|-------------|
| `DISABLE_INTERLEAVED_THINKING` | Disable interleaved thinking blocks |
| `DISABLE_EFFORT` | Disable effort/thinking level controls |

---

## Performance

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_MAX_TOOL_USE_CONCURRENCY` | Max concurrent tool executions |
| `CLAUDE_CODE_PROFILE_STARTUP` | Profile startup performance |
| `CLAUDE_CODE_PERFETTO_TRACE` | Enable Perfetto tracing for debugging |

---

## Features

| Variable | Description |
|----------|-------------|
| `DISABLE_COST_WARNINGS` | Disable cost warning prompts |
| `DISABLE_FILE_CHECKPOINTING` | Disable file history/snapshots |
| `DISABLE_ATTACHMENTS` | Disable file attachments |
| `DISABLE_BACKGROUND_TASKS` | Disable background task execution |
| `DISABLE_OFFICIAL_MARKETPLACE_AUTOINSTALL` | Disable auto-install of official plugins |
| `DISABLE_PLUGIN_AUTOLOAD` | Disable automatic plugin loading |

---

## Commands

| Variable | Description |
|----------|-------------|
| `DISABLE_BUG_COMMAND` | Disable `/bug` command |
| `DISABLE_DOCTOR_COMMAND` | Disable `/doctor` command |
| `DISABLE_FEEDBACK_COMMAND` | Disable feedback command |
| `DISABLE_UPGRADE_COMMAND` | Disable `/upgrade` command |
| `DISABLE_LOGIN_COMMAND` | Disable `/login` command |
| `DISABLE_LOGOUT_COMMAND` | Disable `/logout` command |
| `DISABLE_EXTRA_USAGE_COMMAND` | Disable extra usage command |
| `DISABLE_INSTALL_GITHUB_APP_COMMAND` | Disable GitHub app install command |

---

## Updates

| Variable | Description |
|----------|-------------|
| `DISABLE_AUTOUPDATER` | Disable automatic updates |
| `DISABLE_AUTO_MIGRATE_TO_NATIVE` | Disable auto-migration to native install |
| `DISABLE_INSTALLATION_CHECKS` | Disable installation verification checks |

---

## UI & Display

| Variable | Description |
|----------|-------------|
| `DISABLE_TERMINAL_TITLE` | Disable terminal title updates |
| `DISABLE_FEEDBACK_SURVEY` | Disable feedback survey prompts |
| `CLAUDE_CODE_SYNTAX_HIGHLIGHT` | Control syntax highlighting |
| `CLAUDE_CODE_ACCESSIBILITY` | Enable accessibility features |

---

## Telemetry & Logging

| Variable | Description |
|----------|-------------|
| `DISABLE_TELEMETRY` | Disable all telemetry |
| `DISABLE_NONESSENTIAL_TRAFFIC` | Disable non-essential network requests |
| `DISABLE_ERROR_REPORTING` | Disable error reporting |
| `CLAUDE_DEBUG` | Enable debug logging |
| `CLAUDE_CODE_DEBUG_LOGS_DIR` | Custom directory for debug logs |

---

## Shell & Bash

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_SHELL` | Override default shell |
| `CLAUDE_CODE_SHELL_PREFIX` | Prefix for shell commands |
| `CLAUDE_BASH_MAINTAIN_PROJECT_WORKING_DIR` | Maintain project working directory |
| `CLAUDE_BASH_NO_LOGIN` | Don't use login shell |
| `CLAUDE_CODE_BASH_SANDBOX_SHOW_INDICATOR` | Show sandbox indicator |

---

## Paths & Config

| Variable | Description |
|----------|-------------|
| `CLAUDE_CONFIG_DIR` | Override config directory (default: `~/.claude`) |
| `CLAUDE_CODE_TMPDIR` | Override temp directory |
| `CLAUDE_TMPDIR` | Alternative temp directory override |
| `CLAUDE_ENV_FILE` | Custom environment file path |
| `CLAUDE_CODE_ADDITIONAL_DIRECTORIES_CLAUDE_MD` | Additional CLAUDE.md search paths |

---

## API & Auth

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_API_BASE_URL` | Override API base URL |
| `CLAUDE_CODE_OAUTH_TOKEN` | Provide OAuth token directly |
| `CLAUDE_CODE_OAUTH_CLIENT_ID` | Custom OAuth client ID |
| `CLAUDE_CODE_SESSION_ACCESS_TOKEN` | Session access token |
| `CLAUDE_CODE_SKIP_BEDROCK_AUTH` | Skip Bedrock authentication |
| `CLAUDE_CODE_SKIP_VERTEX_AUTH` | Skip Vertex authentication |
| `CLAUDE_CODE_SKIP_FOUNDRY_AUTH` | Skip Foundry authentication |

---

## Provider Selection

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_USE_BEDROCK` | Use AWS Bedrock |
| `CLAUDE_CODE_USE_VERTEX` | Use Google Vertex AI |
| `CLAUDE_CODE_USE_FOUNDRY` | Use Foundry |

---

## Remote & IDE

| Variable | Description |
|----------|-------------|
| `CLAUDE_CODE_REMOTE` | Enable remote mode |
| `CLAUDE_CODE_AUTO_CONNECT_IDE` | Auto-connect to IDE |
| `CLAUDE_CODE_SSE_PORT` | SSE server port |

---

## Debug Modes

| Variable | Description |
|----------|-------------|
| `CLAUDE_DEBUG` | Enable debug logging |
| `DEBUG` | Node.js debug output (e.g., `DEBUG=claude:*`) |
| `CLAUDE_REPL_MODE` | Enable REPL mode (changes available tools) |
| `CLAUDE_CODE_PROFILE_STARTUP` | Profile startup performance |
| `CLAUDE_CODE_PERFETTO_TRACE` | Enable Perfetto tracing |
| `CLAUDE_CODE_DEBUG_LOGS_DIR` | Custom directory for debug logs |
| `CLAUDE_CODE_DIAGNOSTICS_FILE` | Write diagnostics to file |

---

## Usage Examples

```bash
# Use Haiku for subagents to save costs
CLAUDE_CODE_SUBAGENT_MODEL=claude-haiku-4-5-20251001 claude

# Override default model
ANTHROPIC_MODEL=claude-opus-4-20250115 claude

# Enable API betas
ANTHROPIC_BETAS=web-search-2025-03-05,tool-examples-2025-10-29 claude

# Disable cost warnings
DISABLE_COST_WARNINGS=1 claude

# Debug mode with custom log directory
CLAUDE_DEBUG=1 CLAUDE_CODE_DEBUG_LOGS_DIR=/tmp/claude-logs claude

# Verbose debug output
DEBUG=claude:* claude

# Disable auto-compaction
DISABLE_AUTO_COMPACT=1 claude

# Profile startup time
CLAUDE_CODE_PROFILE_STARTUP=1 claude

# Skip the "must read before write" check
# (via feature flag in ~/.claude.json)
# "tengu_marble_kite": true
```
