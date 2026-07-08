/goal Implement the Ireland focus tree package to its fullest extent. Also add the required BOP, major event suite, and comprehensive flavour event layer, then verify the whole Ireland package against this source package.

Read `docs/specs/ireland_focus_tree/README.md`, `ireland_focus_tree_planning_state.md`, all files under `specs/`, all files under `matrices/`, and all prompts. Prioritize parts 10, 12, 13, 19, 20, and 21.

Follow `AGENTS.md`, `hoi4-events`, `hoi4-feature-planning`, `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-feature-assets`, `hoi4-frame-animation`, `hoi4-text-audio-research`, `hoi4-improvement-loop`, and `hoi4-subagents`.

Events are required. Implement constitutional, Treaty Ports, Emergency neutrality, political route, Northern settlement, foreign reaction, industry, military, BOP crisis, hidden path, late game, and flavour event families. Use country, hidden, state, report, and news events. Every major route needs early, middle, late, and failure or overreach events.

Flavour events are mandatory. Implement the flavour catalogue as final events or dynamic variants with row level mapping. They must be historically grounded and must affect mechanics, decisions, missions, BOP, AI, state support, idea stages, route pressure, foreign access, achievements, or cleanup. Do not implement empty flavour popups.

Implement one Ireland BOP object, recommended id `IRE_state_authority_bop`, with route specific active side pairs. The BOP improves the implemented mechanics. It does not replace Constitutional Authority, Emergency Preparedness, Partition Pressure, or Foreign Access Pressure. BOP must affect route access, decisions, missions, hidden reveals, Northern legitimacy, foreign pressure, AI, events, achievements, and flavour consequences.

Preserve historical neutrality, Fine Gael legal opposition, Labour democratic socialism, Blueshirt corporatism, IRA underground, industry, military, diplomacy, Northern settlement, unified Ireland, and all hidden paths.

Do not use fallback trees, reduced event sets, BOP stubs, generic localisation, tiny reward filler, political power stores, repeated free divisions, empty flavour popups, or claim ladder Northern design. Real leaders, flags, symbols, and historical photos need sourced assets. Generated art is for fictional, symbolic, alternate, UI, and icon work. Treat unresearched quotes, slogans, cultural remarks, allusions, and audio as blockers.

Before completion, run `hoi4_improvement_loop_planner` with `fork_context=false` when available and resolve its output. Provide route, major event, flavour event, BOP, decision, mission, asset, localisation, AI, achievement, and cleanup coverage tables. Do not claim completion until the implemented files satisfy the full package.
