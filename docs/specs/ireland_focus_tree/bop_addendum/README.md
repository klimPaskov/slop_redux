# Ireland Balance of Power retained source package

This directory is retained canonical source history for the Slop Redux Ireland Balance of Power material.

The BOP design has been folded into `docs/specs/ireland_focus_tree/` through `specs/ireland_focus_tree_spec_part_12_balance_of_power.md`, the copied `ireland_focus_tree_bop_*` matrices, and the canonical implementation maps. Do not treat this subtree as a separate feature package or implement it independently. It remains here so the accepted design history, research notes, prompts, and matrices can be audited without restoring the deleted standalone BOP package.

Working labels in this package are internal handles only. They are not final focus titles, decision names, event text, GUI labels, achievement titles, slogans, quotes, or audio choices.

## Design role

The BOP turns Constitutional Authority into a central game surface. It should make the player manage who holds practical authority in Ireland while Emergency Preparedness, Partition Pressure, and Foreign Access Pressure continue to exist as their own mechanics.

The BOP should never become a reward meter that only gives small bonuses. Its bands should unlock route tools, create crisis risks, alter decision costs, change AI behavior, shift available leaders or advisors, and affect Northern settlement and neutrality credibility.

## Package status

This package is retained as supporting source material. The active implementation package is `docs/specs/ireland_focus_tree/`.

The Ireland focus tree closure `hoi4_improvement_loop_planner` pass was run with `fork_context=false` on 2026-07-08; the active closure handoff is `docs/plans/ireland_focus_tree/improvement_loop_closure_readiness_2026-07-08.md`.

## File structure

- `specs/` contains the retained BOP addendum design now folded into the canonical Ireland package.
- `matrices/` contains route, range, decision, AI, asset, and achievement tables.
- `implementation/` contains file surface and id registry handoffs.
- `prompts/` contains implementation, asset, decision, achievement, goal, and improvement loop prompts.
- `research/` contains source notes and bibliography.
- `reports/` contains readiness status.
- `plans/` contains the improvement loop blocker and prompt disposition.
