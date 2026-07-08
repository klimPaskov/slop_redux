# Ireland focus tree improvement loop planner prompt

Spawn `hoi4_improvement_loop_planner` with `fork_context=false`.

Feature slug: `ireland_focus_tree`
Feature name: Ireland comprehensive national focus tree
Current package status: canonical implementation ready source spec package complete except for the mandatory project subagent pass.

## Read first

Read `AGENTS.md`, `hoi4-improvement-loop`, `hoi4-feature-planning`, `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-feature-assets`, `hoi4-frame-animation`, `hoi4-text-audio-research`, and `hoi4-subagents`.

Read these package files:

- `README.md`
- `ireland_focus_tree_planning_state.md`
- all files under `specs/`, including `specs/ireland_focus_tree_spec_part_10_hidden_paths.md`
- all files under `matrices/`, including the hidden path matrices
- all files under `research/`
- all files under `prompts/`
- `plans/ireland_focus_tree_improvement_loop_blocker.md`
- `reports/ireland_focus_tree_implementation_readiness_report.md`

## Question to answer

Determine whether the Ireland focus tree package needs an expansion addendum, an anti bloat cut, or a closure handoff.

## Design constraints to preserve

- Keep player facing localisation as direction only. Do not write final focus titles, descriptions, decision text, event prose, achievement titles, slogans, quotes, cultural remarks, or audio choices.
- Use working labels only as internal handles.
- Avoid em dash and semicolons in prose.
- Real leaders, real flags, and attested symbols require sourced asset work.
- Historical neutrality must remain active through ports, coast watching, G2, Emergency defence, supply, and diplomacy.
- Fine Gael constitutional opposition must remain separate from the Blueshirt corporatist route.
- Labour must remain a democratic socialist route with radical pressure as an option, not only a Soviet branch.
- IRA German contact and Plan Kathleen style material must remain risky and unstable.
- Northern settlement must not become a claim ladder. It must use international reactions, British and unionist pressure, state objectives, and integration work.
- Unified Ireland is the main formable or identity change.
- The Atlantic compact remains a conference or limited faction concept, not a formable country.
- Hidden paths are required planned content. You may trim, merge, or refine weak hidden routes only if the final package still contains planned hidden paths with comparable depth and a recorded disposition.
- The four current internal mechanics are Constitutional Authority, Emergency Preparedness, Partition Pressure, and Foreign Access Pressure.
- The current UI decision is decision category headers and spirit tooltips, with the Emergency Preparedness board as the only scripted GUI candidate.

## Hidden path review requirement

Review part 10 and the hidden path matrices. Check whether civic cultural restoration has enough gameplay and avoids high kingship fantasy, whether Emergency directorate is distinct from Blueshirts and IRA, whether Atlantic compact remains diplomatic, whether common platform settlement avoids a free Northern handover, and whether corrupted restoration failure prevents exploit and fantasy route abuse.

Also inspect the route specific hidden overlays: constitutional backchannel, Labour independent front, corporate chambers without O'Duffy, republican reconciliation backchannel, compromised republican network, cross border Labour Council, neutral aftershock recovery, and Northern emergency protectorate.

## Output requested

Write one of these under `docs/plans/ireland_focus_tree/` or the equivalent planning package path:

1. Expansion addendum if a real design gap remains.
2. Anti bloat cut if any planned branch, asset, mechanic, route, prompt, or hidden content weakens the design.
3. Closure handoff if the design is deep, connected, and ready for implementation after normal cleanup.

Your handoff must list design problem or closure reason, files inspected, additions, cuts, or closure tasks, research basis, affected specs, matrices, prompts, assets, decisions, focus routes, AI, country package surfaces, open questions, whether any prior addendum remains unresolved, and whether the result should be promoted into `docs/specs/ireland_focus_tree/`.
