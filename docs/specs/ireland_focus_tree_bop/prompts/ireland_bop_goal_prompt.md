# Goal prompt for Ireland BOP addendum

Implement `ireland_focus_tree_bop` as a post implementation improvement to the already implemented canonical Ireland focus tree. Use this package as the source design. Main files are `specs/ireland_bop_spec_part_1_design.md` through `specs/ireland_bop_spec_part_5_acceptance_handoffs.md`, `implementation/ireland_bop_file_surface_map.md`, `implementation/ireland_bop_id_registry.md`, and all matrices.

Follow `AGENTS.md`, `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-feature-assets`, `hoi4-frame-animation`, `hoi4-text-audio-research`, `hoi4-improvement-loop`, and `hoi4-subagents`.

Add one Ireland BOP object with route specific active side pairs. Do not create several simultaneous BOPs unless tested and approved. Do not replace Constitutional Authority, Emergency Preparedness, Partition Pressure, or Foreign Access Pressure. The BOP is the visible internal authority layer above those systems.

Implement BOP modes for opening state, historical emergency, Commonwealth cooperation, Labour republic, Blueshirt corporate, republican underground, civic cultural, and Emergency Directorate. Wire initialization, route mode switches, range effects, helper effects, helper triggers, constants, dynamic localisation, decisions, missions, focus hooks, AI behavior, hidden path gates, crisis recovery, and cleanup.

Use concrete decision and mission costs. Avoid political power stores, repeated tiny modifiers, generic equipment, free unit loops, and passive checklist missions. Northern settlement may read BOP legitimacy, but final settlement and integration remain decision verified through state control or agreement checks.

Create or request all BOP assets from `prompts/ireland_bop_asset_prompt.md`. Use sourced assets for real symbols and generated art only for fictional or symbolic material. Use frame animation rules for any animated warning sprite. Do not invent quotes, slogans, cultural remarks, lyric fragments, or audio choices. Final localisation must be written from direction, not copied from working labels.

Implement BOP achievements from `prompts/ireland_bop_achievement_prompt.md` if achievements are active.

Near completion, spawn `hoi4_improvement_loop_planner` with `fork_context=false` using `prompts/ireland_bop_improvement_loop_prompt.md`. Resolve its addendum, closure handoff, or blocker before claiming completion.

Keep iterating until the BOP works across all routes, AI uses it safely, decisions are curated and cleaned up, assets and localisation are aligned, docs are updated, and validation scenarios in part 4 pass. Do not claim completion while any planned BOP mode, route hook, AI behavior, hidden path gate, asset, achievement, cleanup rule, or validation is missing or simplified.
