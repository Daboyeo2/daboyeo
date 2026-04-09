# Workspace Override: daboyeo

This file adds repository-specific rules on top of the global multi-agent defaults.
Global multi-agent defaults remain in effect unless this file narrows them.

## Repository Facts To Fill

- Primary source of truth paths
- Shared asset paths
- Do-not-touch or generated paths
- Error log path: `ERROR_LOG.md`
- Verification commands
- Manual approval zones
- Worker ownership mapping when Route B is used

## Repository Overrides

- Fill `WORKSPACE_CONTEXT.toml` first if you want project-aware generation instead of generic fallback rules
- Keep `STATE.md` updated with exact `route`, concrete `reason`, `writer_slot`, `contract_freeze`, and `write_sets` when Route B is active
- If multiple roles are used, append real participation to `MULTI_AGENT_LOG.md` before reporting that they ran
- Add repository-specific verification commands, hard triggers, approval zones, and worker ownership here
- Let this repository narrow Route A/B behavior further only when it truly needs stricter local rules

