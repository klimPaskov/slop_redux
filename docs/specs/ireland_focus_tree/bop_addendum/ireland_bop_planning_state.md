# Ireland BOP planning state

Feature slug: `ireland_focus_tree`

Retained source label: `ireland_focus_tree_bop`

Parent feature slug: `ireland_focus_tree`

Feature name: Ireland Balance of Power addendum for the comprehensive national focus tree

Canonical package status: BOP is folded into `docs/specs/ireland_focus_tree/`.

Planning status: retained source-history package. Use the canonical top-level package for implementation.

## Source of truth

This subtree is not a separate addendum package for implementation. Its accepted facts have been copied into the canonical Ireland BOP spec, matrices, and implementation handoffs. Keep it only as audit trail and source history inside `docs/specs/ireland_focus_tree/`.

## Core ruling

The BOP is the visible internal authority struggle. It should sit above Constitutional Authority and route specific internal factions. Emergency Preparedness, Partition Pressure, and Foreign Access Pressure keep their own decision and mission systems.

Use one Ireland BOP object with route specific active side pairs. Do not create several simultaneous BOP objects for Ireland unless a later implementation test proves the UI handles that cleanly.

## Improvement loop status

The Ireland focus tree closure `hoi4_improvement_loop_planner` pass was run with `fork_context=false` on 2026-07-08. Current closure work is tracked in `docs/plans/ireland_focus_tree/improvement_loop_closure_readiness_2026-07-08.md` and its parent resolution notes.
