# CLAUDE.md — limen-cli (admin CLI)

> **Project**: limen-cli — component of [Limen](https://github.com/getlimen/limen)
> **Role**: Optional admin CLI for Limen. **Not in v1 — scheduled for v1.1+.**

**For full project context, read [`limen/docs/HANDOFF.md`](https://github.com/getlimen/limen/blob/main/docs/HANDOFF.md).**

## Status

**Stub only.** This repo exists to reserve the name and pattern. No meaningful code until v1.1 work starts.

## Planned functionality (v1.1+)

- `limen login` — exchange an admin API token (from UI) for a local session
- `limen node list` / `node add` / `node remove`
- `limen service deploy <name>` / `service list`
- `limen route add <hostname>` / `route list`
- `limen backup create` / `backup restore`
- `limen logs <service> [--follow]`

## Tech Stack (planned)

- .NET 10 / NativeAOT
- `System.CommandLine` for CLI parsing
- Single binary per platform

## Why defer

The Angular UI is the primary admin surface for v1. A CLI is a user-convenience layer that should wait until the core platform is stable.

## Conventions

Same as `limen`: English-only, Apache 2.0, conventional commits, **no AI attribution in commits**.
