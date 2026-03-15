# Deployment Profile

This is a sanitized profile of the OpenClaw environment the architecture was designed around.

## Runtime Shape

- OpenClaw gateway mode: local
- Primary model: local Ollama model
- Current primary model ref: `ollama-2/qwen2.5:7b`
- Agent shape: single main agent
- Heartbeat enabled: yes
- Heartbeat interval: `30m`

## Enabled Channels

- Telegram
- Discord

## Why This Matters

The architecture is intentionally optimized for a local-first OpenClaw deployment rather than a hosted frontier-model stack.

That means the design assumes:

- local LLM orchestration
- shorter, more structured worker prompts
- stronger dependence on deterministic tools and filesystem artifacts
- resumable per-issue runs instead of giant long-context sessions

## Design Implications

Because the target environment is local-first:

- workers should emit JSON, not long freeform prose
- evidence should be persisted to disk per issue run
- one worker should handle one issue at a time
- synthesis should happen after artifacts are written, not only in memory
- GitHub writes should stay manual or approval-gated until the system is proven reliable

## Excluded Details

This profile intentionally does not include:

- tokens
- secrets
- raw account identifiers
- personal paths beyond the general OpenClaw layout
- any direct credential material
