# CLAUDE.md — limen-cli (admin CLI)

> **Project**: limen-cli — component of [Limen](https://github.com/getlimen/limen)
> **Role**: Optional admin CLI for Limen. **Not in v1 — scheduled for v1.1+.**

**For full project context, read [`limen/docs/HANDOFF.md`](https://github.com/getlimen/limen/blob/main/docs/HANDOFF.md) and [`limen/docs/CONVENTIONS.md`](https://github.com/getlimen/limen/blob/main/docs/CONVENTIONS.md).**

## Workflow rules (enforced, apply to every repo in `getlimen`)

- **Never work on `main`.** Create issue (labeled) → branch `<type>/<issue>_<PascalCaseName>` → PR (labeled) with `Closes #<issue>` → squash-merge + delete branch.
- **Use CLI generators whenever one exists.** `dotnet new`, `gh issue create`, `gh pr create`, etc. If you don't know the command, search online before hand-writing boilerplate.
- **No AI / Claude attribution** in commits or PRs.

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
