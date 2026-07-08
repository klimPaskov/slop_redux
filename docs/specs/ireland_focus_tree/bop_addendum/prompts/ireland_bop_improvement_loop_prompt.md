# Ireland BOP improvement loop prompt

Spawn `hoi4_improvement_loop_planner` with `fork_context=false`.

Feature slug: `ireland_focus_tree_bop`

Parent feature slug: `ireland_focus_tree`

Goal: review the post implementation Ireland Balance of Power addendum for depth, anti bloat, missing route integration, missing AI behavior, missing decision quality, hidden path coverage, asset needs, and implementation readiness.

Read these package files:

- `specs/ireland_bop_spec_part_1_design.md`
- `specs/ireland_bop_spec_part_2_modes_and_ranges.md`
- `specs/ireland_bop_spec_part_3_focus_decision_integration.md`
- `specs/ireland_bop_spec_part_4_ai_and_cleanup.md`
- `specs/ireland_bop_spec_part_5_acceptance_handoffs.md`
- `matrices/ireland_bop_mode_matrix.md`
- `matrices/ireland_bop_range_matrix.md`
- `matrices/ireland_bop_focus_integration_matrix.md`
- `matrices/ireland_bop_decision_matrix.md`
- `matrices/ireland_bop_ai_matrix.md`
- `matrices/ireland_bop_asset_matrix.md`
- `matrices/ireland_bop_achievement_matrix.md`
- `implementation/ireland_bop_file_surface_map.md`
- `implementation/ireland_bop_id_registry.md`
- `prompts/ireland_bop_coding_prompt.md`
- `research/ireland_bop_research_notes.md`

Also read the already implemented Ireland canonical package in the repository, especially the focus tree, decisions, ideas, AI, hidden path content, and docs. Treat the canonical package as implemented, then evaluate whether this BOP addendum improves it without duplicating or bloating it.

Questions to answer:

1. Should the addendum remain one BOP object with route specific active side pairs.
2. Does any route need a different BOP mode, a merged mode, or a removed mode.
3. Are any planned BOP decisions passive, too cheap, too abstract, or redundant with existing canonical decisions.
4. Are hidden paths gated clearly and safely by BOP bands.
5. Does the BOP preserve the distinction between Fine Gael legalism and Blueshirt corporatism.
6. Does Labour remain democratic socialist unless the player chooses stronger congress or foreign alignment pressure.
7. Does IRA foreign contact remain risky and unstable.
8. Does Emergency Directorate remain a crisis route and not an easy shortcut.
9. Does the BOP improve Northern settlement without replacing decision verified state control and integration.
10. Are AI rules strong enough to prevent invalid route choices and stale decisions.
11. Are assets and possible animation useful without clutter.
12. Does the addendum need an expansion addendum, a small correction list, or a closure handoff.

Return either a concrete addendum or a closure handoff. If an addendum is written, state exactly which package files should be patched or which items should be queued, rejected, or accepted.
