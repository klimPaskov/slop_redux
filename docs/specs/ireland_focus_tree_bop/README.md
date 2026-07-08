# Ireland Balance of Power addendum package

This is a separate post implementation addendum for the Slop Redux Ireland comprehensive focus tree.

The canonical Ireland focus tree package is treated as already implemented. This package does not rewrite that work. It adds a comprehensive Balance of Power layer that improves the existing implementation by making the internal political struggle visible, route aware, and connected to the already planned mechanics.

Working labels in this package are internal handles only. They are not final focus titles, decision names, event text, GUI labels, achievement titles, slogans, quotes, or audio choices.

## Design role

The BOP turns Constitutional Authority into a central game surface. It should make the player manage who holds practical authority in Ireland while Emergency Preparedness, Partition Pressure, and Foreign Access Pressure continue to exist as their own mechanics.

The BOP should never become a reward meter that only gives small bonuses. Its bands should unlock route tools, create crisis risks, alter decision costs, change AI behavior, shift available leaders or advisors, and affect Northern settlement and neutrality credibility.

## Package status

This package is implementation ready as a design handoff. It has no temporary continuation prompt.

The mandatory `hoi4_improvement_loop_planner` pass is recorded as a tooling blocker because this chat environment does not expose the project custom subagent spawning tool. The package includes a ready prompt for an environment that can spawn that subagent with `fork_context=false`.

## File structure

- `specs/` contains the canonical BOP addendum design.
- `matrices/` contains route, range, decision, AI, asset, and achievement tables.
- `implementation/` contains file surface and id registry handoffs.
- `prompts/` contains implementation, asset, decision, achievement, goal, and improvement loop prompts.
- `research/` contains source notes and bibliography.
- `reports/` contains readiness status.
- `plans/` contains the improvement loop blocker and prompt disposition.
