---
type: Changed
pr: 5240
---
**OpenCode installs no longer ship Claude-only references that change behavior** — the installer now rewrites `.claude/skills/` locators to `.opencode/skills/`, `./.claude/` tree refs to `./.opencode/`, `@`-anchored `.claude/gsd-core/` includes to the opencode tree, and `--claude --local/--global` launcher hints to the invoking `--opencode` flag (scope preserved), across commands, skills, agents, and the `gsd-core/` tree including `.compact.md` variants; the post-install leak scan covers exactly this owned set. The multi-runtime fallback chain (`${_GSD_RUNTIME_ROOT}/.claude`, `.codex/gsd-core`, `${CLAUDE_CONFIG_DIR:-…}` defaults, `CLAUDE_ENV_FILE`) is byte-identical, including a fallback-default mangling the old `$HOME/.claude` rule caused. (#4779)
<!-- docs-exempt: install-time path/hint correction only; no English docs describe the converted output or leak-scan text (verified: no matches in docs/ outside zh-CN mirrors), so there is no docs surface to update. -->
