# Ireland Static Balance And Route Validation

Date: 2026-07-08

## Scope

This is a static implementation validation pass for the canonical Ireland package. It checks route surfaces, costs, AI locks, Northern settlement verification, BOP integration, achievement hooks, and cleanup paths from the files in this workspace. It is not a live HOI4 campaign run.

## Files Checked

- `common/national_focus/ireland_focus_tree.txt`
- `common/decisions/ireland_focus_tree_decisions.txt`
- `common/decisions/ireland_bop_decisions.txt`
- `common/bop/ireland_balance_of_power.txt`
- `common/scripted_effects/slopx_ireland_effects.txt`
- `common/scripted_effects/ireland_bop_effects.txt`
- `common/scripted_triggers/slopx_ireland_triggers.txt`
- `common/scripted_triggers/ireland_bop_triggers.txt`
- `events/ireland_focus_tree_events.txt`
- `events/ireland_focus_tree_major_events.txt`
- `events/ireland_flavour_events.txt`
- `common/ai_strategy/ireland_focus_tree_ai_strategy.txt`
- `common/achievements/ireland_focus_tree_achievements.txt`

## Route Coverage Evidence

- Historical sovereign neutrality has authority, Emergency readiness, Treaty Ports, coastwatch, foreign access, and postwar neutrality focus surfaces, with BOP modes for opening state and historical Emergency.
- Fine Gael constitutional opposition is distinct from Blueshirt corporatism through separate focus locks, BOP modes, liaison/backchannel decisions, constitutional concession testing, and non-basing safeguards.
- Labour democratic cooperation and Labour radical pressure are separated by route flags, BOP modes, cross-border council proof, worker-defence legality checks, and foreign dependency blockers.
- Blueshirt corporatism has separate O'Duffy and chamber-state outcomes, sponsor containment, guard discipline, chamber BOP mode, and no hidden path that turns the Atlantic compact into a formable country.
- IRA underground content has compromised network, courier exposure, safehouse audit, arms surrender, border-cell stand-down, reconciliation backchannel, and Army Council timeout pressure.
- Hidden civic restoration, Emergency directorate, Atlantic neutral compact, common-platform Northern settlement, corrupted restoration failure, cross-border Labour Council, constitutional backchannel, republican reconciliation, neutral aftershock recovery, and Northern emergency protectorate have reveal/prep flags plus focus, decision, mission, or achievement surfaces.
- The Atlantic compact remains implemented as a diplomatic conference or faction compact; no country tag or formable country path is used.

## Northern Settlement Checks

- All-island settlement uses `slopx_ireland_has_verified_northern_settlement`, observer/preparation flags, regional province control helpers, and staged post-settlement missions.
- `IRE_ALL_ISLAND` is reached through `slopx_ireland_complete_all_island_settlement` only after verified settlement conditions, not from a raw claim ladder.
- Post-settlement integration requires policing, service continuity, Belfast industry, and unionist safeguards before completion.
- The Northern emergency protectorate has temporary administration, observer corridor, policing board, and exit-settlement missions with failure pressure.

## Balance Notes

- Route missions use command power, fuel, equipment, factories, state targets, BOP position, and pressure variables rather than defaulting to political power, repeated flat stability, free divisions, or generic equipment rewards.
- Routine BOP decisions are cooldown pressure levers; closure-proof BOP actions use selectable missions.
- Hidden path AI is route-aware and blocks high-risk hidden consolidation under incompatible crisis, sponsor, or radical-route conditions.
- Cleanup effects clear route-crisis flags, invalidate sponsor paths, resolve protectorate exits, or set explicit failed/recovered flags instead of leaving hidden states ambiguous.

## Validation Limit

No live campaign, hands-off observer game, or executable HOI4 load run was performed from this Codex workspace. This note is static proof for code review and route coverage; live balance remains a manual playtest task outside the workspace.
