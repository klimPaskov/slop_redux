# Ireland BOP planning state

Feature slug: `ireland_focus_tree_bop`

Parent feature slug: `ireland_focus_tree`

Feature name: Ireland Balance of Power addendum for the comprehensive national focus tree

Canonical package status: treated as already implemented by the user.

Planning status: complete design package, ready for implementation against the existing Ireland implementation.

## Source of truth

This package is a separate addendum. Its spec files should either be copied under `docs/specs/ireland_focus_tree_bop/` or merged into the existing Ireland spec folder under a clearly named BOP addendum file. Do not overwrite the canonical Ireland package. Do not remove the four existing mechanics.

## Core ruling

The BOP is the visible internal authority struggle. It should sit above Constitutional Authority and route specific internal factions. Emergency Preparedness, Partition Pressure, and Foreign Access Pressure keep their own decision and mission systems.

Use one Ireland BOP object with route specific active side pairs. Do not create several simultaneous BOP objects for Ireland unless a later implementation test proves the UI handles that cleanly.

## Mandatory open blocker

`hoi4_improvement_loop_planner` could not be spawned in this environment. The blocker is documented under `plans/ireland_bop_improvement_loop_blocker.md`.
