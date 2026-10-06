---
type: Fixed
pr: 5242
---
**OpenCode v2 loader now accepts the GSD plugin alongside v1** — `.opencode/plugins/gsd-core.js` (and its byte-identical Kilo twin) exposes a non-enumerable `setup(ctx)` registering V2 equivalents of every V1 surface (tool/shell/session hooks, filtered event subscription, package-tree command/agent/skill transforms) while the V1 `server` map and its `Object.values` iteration stay exactly `[server]`. (#4916)
