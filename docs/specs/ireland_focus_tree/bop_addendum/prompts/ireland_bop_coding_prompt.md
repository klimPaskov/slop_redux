# Ireland BOP coding prompt

Implement the Ireland Balance of Power addendum as a post implementation improvement to the already implemented canonical Ireland focus tree.

Use the files in this package as source design:

- `specs/ireland_bop_spec_part_1_design.md`
- `specs/ireland_bop_spec_part_2_modes_and_ranges.md`
- `specs/ireland_bop_spec_part_3_focus_decision_integration.md`
- `specs/ireland_bop_spec_part_4_ai_and_cleanup.md`
- `specs/ireland_bop_spec_part_5_acceptance_handoffs.md`
- `implementation/ireland_bop_file_surface_map.md`
- `implementation/ireland_bop_id_registry.md`
- all matrices in `matrices/`

Follow `AGENTS.md`, `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-feature-assets`, `hoi4-frame-animation`, `hoi4-text-audio-research`, `hoi4-subagents`, and `hoi4-improvement-loop`.

Before editing BOP script, inspect the local offline Paradox wiki pages and vanilla documentation for balance of power, effects, triggers, localisation, data structures, focus trees, decisions, AI, and scripted localisation. Inspect vanilla BOP examples and existing Slop Redux patterns.

Implement one Ireland BOP object with route specific active side pairs. Use the suggested id `IRE_state_authority_bop` unless the existing repository pattern requires a different id. Keep a mapping if renamed.

Do not create multiple simultaneous Ireland BOPs unless the UI is tested and the user approves. Do not replace Constitutional Authority, Emergency Preparedness, Partition Pressure, or Foreign Access Pressure. The BOP sits above Constitutional Authority and route internal struggles.

Implement these BOP modes:

- opening state
- historical emergency
- Commonwealth cooperation
- Labour republic
- Blueshirt corporate
- republican underground
- civic cultural
- Emergency Directorate

Wire BOP initialization to the opening constitutional trunk or the existing Constitutional Authority start. Wire route lock focuses to switch BOP modes and clean old route decisions. Use helper effects and triggers for mode switching, band checks, crisis gates, and cleanup.

Patch existing Ireland focuses, decisions, missions, ideas, AI, events where present, docs, and localisation so the BOP affects real gameplay. Major BOP decisions must use concrete costs and objectives, not repeated political power clicks. Use equipment, manpower, command power, army XP, civilian capacity, factory output, convoys, fuel, supplied divisions, local support, legitimacy, and deadlines where appropriate.

Implement route AI bands and recovery behavior from `matrices/ireland_bop_ai_matrix.md`. AI must avoid invalid actions, dead sponsors, closed routes, impossible Northern targets, and stale decisions after route change.

Write final localisation from direction only. Do not paste working labels. Do not invent quotes, slogans, mottos, lyric fragments, cultural remarks, or audio choices. Source any real symbols, real flags, real leader portraits, and real slogans through the proper asset or text research workflows.

Create or request assets from `prompts/ireland_bop_asset_prompt.md`. Wire sprite definitions only after final DDS files exist or after approved placeholders are registered according to repository rules.

Implement achievements from `prompts/ireland_bop_achievement_prompt.md` if the repository achievement system is active.

Near completion, spawn `hoi4_improvement_loop_planner` with `fork_context=false` using `prompts/ireland_bop_improvement_loop_prompt.md`. Resolve its addendum, closure handoff, or blocker before claiming completion.

Do not claim completion until the BOP works across every route, route decisions are gated cleanly, AI uses it safely, hidden paths read the planned bands, Northern settlement remains decision verified, assets and localisation are aligned, docs are updated, and validation scenarios in part 4 have been checked.
