---
type: Fixed
pr: 5242
---
**OpenCode hook scripts now run on a real JS runtime instead of the host binary** — the adapter resolves `GSD_HOOK_RUNTIME` → `node`/`bun` on `PATH` → validated `process.execPath` (with a loud one-time warning as a last resort), so hooks actually execute under Bun/SEA/native hosts instead of silently allowing; a child that never booted (bad interpreter, bad cwd, missing binary) now throws naming the hook file instead of reading as allow. (#4849)
