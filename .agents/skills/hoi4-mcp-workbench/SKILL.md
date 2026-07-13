---
name: hoi4-mcp-workbench
description: Use the installed HOI4 MCP server from coding-agent workflows to analyze event chains and to inspect, render, create, clean, and validate national focus trees, scripted GUIs, and maps in an external mod workspace.
---

# HOI4 MCP Workbench

Use the MCP server alongside repository skills, `AGENTS.md`, and bounded
subagents. It operates on the configured mod workspace while the agent keeps
ownership of design, source review, and final validation.

## Setup once per machine

1. Install Node.js 22 or 24.
2. Install the package:

   ```powershell
   npm install --global hoi4-agent-tools@1.2.0
   ```

3. Configure the game and mod parent roots:

   ```powershell
   hoi4-agent-tools-setup --init `
     --mod-root "C:\Users\<you>\OneDrive\Documents\Paradox Interactive\Hearts of Iron IV\mod" `
     --game-root "C:\Program Files (x86)\Steam\steamapps\common\Hearts of Iron IV"
   hoi4-agent-tools-setup --print-client-config
   ```

4. Add the printed client entry to the coding agent and reload it.
5. Call `hoi4.mods` and use the returned workspace ID. Do not guess it from a
   path or reuse a cached ID from another setup.

## Tool routing

- Focus trees: `hoi4.focus_inspect`, `hoi4.focus_render`, then
  `hoi4.focus_rewrite`. Use `layoutMode: "compact"` for cleanup or pass a
  complete plan for a new tree. Set `reviewScale: 0.25` when a very large tree
  exceeds the default review budget.
- Event chains: call `hoi4.event_inspect` with `scan` or `roots`, then narrow
  with `trace`, `explain_path`, `state_flow`, or `impact`. Record the returned
  revision, edit normal mod source, then pass that revision to
  `hoi4.event_compare` as `before`. Finish with `hoi4.event_inspect` in `lint`
  mode and a targeted `hoi4.event_render`. Event tools are read-only.
  Comparison covers the workspace graph and does not take a chain selector.
- Scripted GUI: `hoi4.gui_inspect`, `hoi4.gui_render`, and
  `hoi4.gui_rewrite`. Provide the complete scenario, states, and resolutions
  needed for deterministic review.
- Maps: `hoi4.map_inspect`, `hoi4.map_render`, and `hoi4.map_rewrite`. Inspect
  province geometry and connected state, region, adjacency, supply, and railway
  data before a declarative rewrite.

## Context rules

- Let the coding agent decide when MCP helps. Do not add a separate workflow
  gate.
- Use narrow selectors, directions, depth, and node limits for event work.
- Read the compact response first. Open linked JSON or render artifacts only
  when the task needs evidence not present in the summary.
- Keep `AGENTS.md`, system skills, planning, assets, and subagent routing active.
  MCP is one tool in that workflow.
- Review the repository diff and run task-specific validation after writes.
- If MCP is unavailable, report the exact setup or tool error instead of
  claiming an MCP result.
