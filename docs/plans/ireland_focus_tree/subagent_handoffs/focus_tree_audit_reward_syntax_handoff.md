# Ireland Focus Tree Audit Reward Syntax Handoff

Date: 2026-07-08

Subagent: mod focus tree subagent

## Scope

Audited the Ireland comprehensive national focus tree implementation for route logic, prerequisites, mutual exclusions, hidden path reveal/blocker behavior, focus rewards, Northern settlement/failure behavior, AI weights, and spec coverage.

## Patch

Changed `common/scripted_effects/slopx_ireland_effects.txt`.

Replaced unsupported military XP effect names in two Ireland reward helpers:

- `slopx_ireland_military_regular_effect`: `add_army_experience = 10` -> `army_experience = 10`
- `slopx_ireland_military_air_naval_effect`: `add_air_experience = 5` -> `air_experience = 5`
- `slopx_ireland_military_air_naval_effect`: `add_navy_experience = 5` -> `navy_experience = 5`

## Affected Focus Rewards

The fix preserves existing route behavior and makes the XP rewards apply for focuses that call these helpers:

- `irl_limited_air_and_naval_access`
- `irl_irish_brigade_lessons`
- `irl_army_establishment_review`
- `irl_officer_training_mission`
- `irl_regular_battalion_expansion`
- `irl_template_modernisation`
- `irl_air_corps_observation`
- `irl_baldonnel_training`
- `irl_air_warning_missions`
- `irl_naval_service_foundations`
- `irl_coastal_patrols`
- `irl_mines_and_convoy_warning`
- `irl_naval_neutrality_school`
- `irl_air_observation_ring`

## Validation

- Confirmed vanilla documentation and vanilla national focuses use `army_experience`, `air_experience`, and `navy_experience`.
- Re-ran a targeted grep on Ireland focus, effect, and decision files; no `add_army_experience`, `add_air_experience`, or `add_navy_experience` references remain.
- Parsed `common/national_focus/ireland_focus_tree.txt`: 238 focus blocks, no duplicate focus IDs, no missing icons, no missing `ai_will_do`, no unresolved prerequisite or mutual-exclusion focus references, no asymmetric mutual exclusions, and no duplicate focus coordinates.
- Compared focus IDs against `docs/specs/ireland_focus_tree/**/*.md`: 238 spec focus-like IDs match 238 implemented focus IDs, with no missing or extra IDs.
- Checked focus references from Ireland decisions, achievements, AI strategy, scripted triggers, and scripted effects; all referenced focus IDs resolve.

## Remaining Risks

No route blockers found after the helper syntax fix. Remaining review risk is balance tuning, not implementation coverage: route opener AI is factor-based at the focus level while route-specific behavior is primarily handled through `common/ai_strategy/ireland_focus_tree_ai_strategy.txt` after route flags are set.
