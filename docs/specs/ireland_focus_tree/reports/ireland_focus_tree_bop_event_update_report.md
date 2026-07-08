# Ireland focus tree BOP and event canonical update report

## Correction made

The earlier canonical package treated events too weakly. That was a design error. Events are now required planned content across the full Ireland package.

The package now includes a mandatory event suite spec, event matrices, event prompt, event asset directions, event text and audio research gates, event achievement hooks, and updated coding and goal prompts.

## BOP integration

The separate BOP addendum is now folded into the canonical package. The full addendum remains under `bop_addendum/`, and canonical BOP files are also present under `specs/`, `matrices/`, and `implementation/`.

## Updated source files

- `specs/ireland_focus_tree_spec_part_12_balance_of_power.md`
- `specs/ireland_focus_tree_spec_part_13_event_suite.md`
- `prompts/ireland_focus_tree_event_prompt.md`
- BOP matrices copied into canonical `matrices/`
- event matrices added to canonical `matrices/`
- updated coding, goal, decision, asset, text and audio, achievement, and improvement loop prompts

## Acceptance change

Implementation is not complete without events. Every major route, hidden route, BOP mode, Northern settlement stage, major foreign reaction, formation outcome, and cleanup layer needs event coverage.

## Remaining process note

The mandatory project improvement loop subagent still cannot be run in this chat environment because no callable project custom subagent tool is exposed. The package keeps the prompt and blocker note visible.
