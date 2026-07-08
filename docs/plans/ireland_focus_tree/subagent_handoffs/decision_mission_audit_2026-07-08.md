# Ireland decision and mission audit handoff, 2026-07-08

## Scope

Audited Ireland decision and mission implementation against the canonical package in `docs/specs/ireland_focus_tree/`, with emphasis on:

- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_5_decisions_missions.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_12_balance_of_power.md`
- `docs/specs/ireland_focus_tree/bop_addendum/specs/ireland_bop_spec_part_1_design.md`
- `docs/specs/ireland_focus_tree/bop_addendum/specs/ireland_bop_spec_part_2_modes_and_ranges.md`
- `docs/specs/ireland_focus_tree/bop_addendum/specs/ireland_bop_spec_part_3_focus_decision_integration.md`
- `docs/specs/ireland_focus_tree/bop_addendum/specs/ireland_bop_spec_part_4_ai_and_cleanup.md`
- `docs/specs/ireland_focus_tree/matrices/ireland_focus_tree_decision_mission_matrix.md`
- `docs/specs/ireland_focus_tree/matrices/ireland_focus_tree_hidden_path_decision_matrix.md`
- `docs/specs/ireland_focus_tree/matrices/ireland_focus_tree_bop_decision_matrix.md`

Owned files inspected:

- `common/decisions/ireland_focus_tree_decisions.txt`
- `common/decisions/ireland_bop_decisions.txt`
- `common/decisions/ireland_flavour_decisions.txt`

Reference files inspected for trigger and cleanup context:

- `common/scripted_triggers/slopx_ireland_triggers.txt`
- `common/scripted_effects/slopx_ireland_effects.txt`
- `common/scripted_effects/ireland_bop_effects.txt`
- `common/achievements/ireland_focus_tree_achievements.txt`
- `common/ai_strategy/ireland_focus_tree_ai_strategy.txt`
- `interface/ireland_focus_tree.gfx`
- `interface/ireland_focus_tree_bop.gfx`

## Files changed

- `common/decisions/ireland_bop_decisions.txt`
- `docs/plans/ireland_focus_tree/subagent_handoffs/decision_mission_audit_2026-07-08.md`

## Changed ids

- `ire_bop_public_confidence_drive`
- `ire_bop_veterans_reconciliation_board`

## Patch behavior

Before:

- `ire_bop_public_confidence_drive` was visible in any active BOP mode because it had no `visible` mode filter. It only called the opening-mode constitutional side shift, so use outside opening mode could spend command power without moving the active BOP pair.
- `ire_bop_veterans_reconciliation_board` was also unfiltered by BOP mode. It could appear outside the opening or republican modes, and republican-mode use did not move the civilian republican front side.

After:

- `ire_bop_public_confidence_drive` is visible only in opening, historical emergency, and Commonwealth cooperation modes. Its effect now calls the matching legal-side helpers for those modes: constitutional government, civilian cabinet, and independent parliamentary review.
- `ire_bop_veterans_reconciliation_board` is visible only in opening and republican underground modes. It now calls both the opening constitutional helper and the republican front helper, with only the active mode's helper taking effect.

This is bounded to BOP decision validity and does not change focus trees, events, localisation, assets, interface, or achievement definitions.

## Issue list

### High severity

1. Most Ireland "missions" are click and wait decisions, not objective missions.
   - Evidence: `common/decisions/ireland_focus_tree_decisions.txt` defines `@ireland_mission_short = 35`, `@ireland_mission_medium = 60`, `@ireland_mission_long = 90`, and then uses `days_remove` broadly across authority, emergency, port, economy, foreign, partition, crisis, and integration decisions.
   - Spec conflict: the canonical decision and mission spec expects 90 to 365 day objectives that require state control, supplied divisions, port guarding, observer conditions, local support, or construction work.
   - Risk: the category behaves more like a short timed store than a mission layer. This affects visible mechanic presentation, player action requirements, and failure pressure.

2. Northern settlement and integration are implemented against a single broad state.
   - Evidence: `slopx_ireland_controls_northern_ireland` and `slopx_ireland_can_integrate_north` use `controls_state = 119`, and post-settlement work adds effects to state `119`.
   - Spec conflict: the canonical package calls for Belfast, Derry, border counties, observer plebiscites, service continuity, and staged integration targets.
   - Risk: the settlement can collapse into one state check and staged click chain instead of a Northern objective system. This weakens the "not a claim ladder" requirement.

3. BOP decision layer is present, but most BOP families are still clickable cooldown decisions.
   - Evidence: `common/decisions/ireland_bop_decisions.txt` includes required families such as `ire_bop_public_confidence_drive`, `ire_bop_coast_security_transfer`, `ire_bop_congress_mandate`, `ire_bop_guard_discipline_case`, and `ire_bop_army_council_mandate`, but most use `days_re_enable` and instant `complete_effect`.
   - Spec conflict: BOP missions should use concrete objectives and timers where the matrix says timed mission.
   - Risk: BOP is visible and action-linked, but the implementation underuses state objectives, supplied divisions, local support, and failure events.

### Medium severity

4. Hidden path reveal logic exists but coverage is uneven.
   - Evidence: reveal helpers exist for civic, directorate, Atlantic, and common platform routes in `slopx_ireland_effects.txt`. Decision hooks exist for common platform, directorate, Labour, corporate, republican, aftershock, and protectorate content.
   - Gap: several accepted hidden overlays from part 10 are represented by one or two short decisions, not full reveal ladders with testing missions, failure states, and cleanup. Examples include neutral aftershock recovery, constitutional backchannel, corporate chambers, and republican reconciliation.

5. Post-settlement integration has stages and failure review, but no active regional mission pool.
   - Evidence: `ireland_policing_transition_stage`, `ireland_service_continuity_stage`, `ireland_belfast_industry_stage`, and `ireland_unionist_safeguards_stage` form a chain gated by `ireland_integration_mission_active`.
   - Gap: stages do not verify multiple Northern target regions, observer conditions, or local administration beyond `controls_state = 119` and pressure thresholds.

6. AI behavior exists but is shallow in several decision families.
   - Evidence: many decisions use flat `ai_will_do = { base = 4 }`, `base = 5`, `base = 6`, or `base = 7`.
   - Gap: spec asks AI to consider route validity, foreign dependency, war pressure, equipment, state targets, and crisis bands. Some decisions do this, but many route and hidden overlay decisions do not.

### Low severity

7. Decision icon references are wired, but asset quality was not audited.
   - Evidence: all `icon = GFX_decision...` references in the Ireland decision files have matching `GFX_decision...` definitions under `interface/`.
   - Out of scope: final DDS quality, source manifests, and placeholder status were not inspected beyond reference existence.

8. Achievement hooks exist, but decision-side hooks are uneven.
   - Evidence: decision files set several route flags, such as `ireland_achievement_plan_kathleen_exposed_ready`, `ireland_achievement_common_platform_ready`, `ireland_achievement_workers_cross_the_border_ready`, and `ireland_achievement_amnesty_before_uprising_ready`.
   - Gap: BOP achievements mostly use live BOP conditions rather than decision-side "ready" hooks, which is valid but makes decision contribution less explicit.

## Decision category lifecycle notes

- `ireland_constitutional_authority_category`, line 43, appears after `ireland_mechanics_initialized`. It has early authority tools and an active flag, but mission durations are short and completion usually happens from timer expiry.
- `ireland_emergency_preparedness_category`, line 183, unlocks from `irl_emergency_skeleton`. It has active mission gating, but preparedness is mostly increased by wait timers and equipment costs rather than state defence objectives.
- `ireland_ports_and_coast_category`, line 323, opens from `irl_treaty_ports_question`. It changes port readiness and construction, but broad states make Cobh and Berehaven both Munster-level outcomes.
- `ireland_economic_recovery_category`, line 414, opens from `irl_first_industry_survey`. It has project staging and an active project flag, but project durations include 35, 60, and 90 day timers where the spec expected larger regional projects.
- `ireland_foreign_access_category`, line 538, opens from `irl_foreign_access_audit`. Sponsor invalidity is partly checked for Britain and faction state, but broad sponsor cleanup still appears to live outside the decision file.
- `ireland_partition_settlement_category`, line 786, opens from `irl_border_file_reopened`. It supports common platform and all-island proclamation, but most peaceful settlement work is click and wait.
- `ireland_route_crisis_category`, line 959, opens whenever an Ireland route is locked. It contains hidden overlay tasks and crisis tasks, with a shared `ireland_route_crisis_active` cleanup helper.
- `ireland_post_settlement_integration_category`, line 1427, appears after settlement or protectorate availability. It has staged integration and failure handling, but still uses one Northern state target.
- `ireland_state_authority_bop_category`, line 29 of `ireland_bop_decisions.txt`, is visible when the BOP exists. It has BOP mode-specific decisions and two true timed missions, but most BOP rows are cooldown decisions.

## Mission quality notes

| Mission or family | Owner | Category | Region | Requirement | Duration | Success | Failure | Duplicate risk |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `ireland_hold_dail_confidence_mission` | IRE | constitutional authority | country level | command power and no active authority mission | 35 days | authority gain | none, timer success only | medium, similar click and wait authority pattern |
| `ireland_emergency_stockpile_mission` | IRE | emergency preparedness | country level | infantry equipment, support equipment, trains | 60 days | store readiness and preparedness | none, timer success only | medium |
| `ireland_coastwatch_posts_mission` | IRE | emergency preparedness | coastal concept, no state target | support equipment and command power | 35 days | coastwatch readiness | none, timer success only | medium |
| `ireland_secure_cobh_approaches` | IRE | ports and coast | Munster state | fuel and support equipment | 60 days | coastal fort, AA, port readiness | none, timer success only | low, named port but broad state |
| `ireland_border_survey_mission` | IRE | partition settlement | Northern border concept | command power and no active Northern mission | 35 days | settlement preparation | none, timer success only | medium |
| `ireland_common_platform_table_mission` | IRE | partition settlement | Northern concept | low partition pressure | 90 days | hidden common platform focus effect | none, timer success only | medium |
| `ire_bop_civilian_rule_timetable_mission` | IRE | BOP authority | country level | authority, preparedness, stable BOP band | 180 days | civilian restoration flag and BOP shift | permanent security state | low, this is a stronger mission |
| `ire_bop_northern_legitimacy_hearing_mission` | IRE | BOP authority | Northern Ireland state | settlement prepared, low pressure, legitimacy, controls state 119 | 150 days | common platform reveal and BOP shift | settlement failed | low, but single-state target |
| `ireland_policing_transition_stage` | IRE | post-settlement integration | Northern Ireland state | can integrate north, command power, support equipment | 120 days | integration stage advances | settlement failure helper if invalid | medium, stage chain pattern |
| `ireland_protectorate_policing_board` | IRE | post-settlement integration | Northern Ireland state | support equipment, command power, active protectorate, controls state 119 | 120 days | protectorate policing ready | settlement failure helper | low |

## Cost and requirement clarity notes

- Costs are concrete in many places: command power, infantry equipment, support equipment, trains, fuel, manpower, and XP appear across the owned decision files.
- The main cost clarity gap is not resource variety. The gap is that many requirements do not express objective work. For example, port, border, coastwatch, and integration work often spends resources and waits without checking supplied divisions, built infrastructure, controlled named localities, or observer conditions.
- Mission durations are below the decision skill's recommended bands. `@ireland_mission_short = 35`, `@ireland_mission_medium = 60`, and `@ireland_mission_long = 90` make many non-emergency missions too short for the canonical objective layer.

## AI validity and route-lock notes

- The patch narrows two BOP decisions to their valid active modes and ensures all visible modes get a matching BOP shift.
- BOP AI strategy files include pressure recovery and route alarms, but many individual decision `ai_will_do` blocks remain flat or lightly modified.
- Sponsor and target validity is partial. Britain-linked decisions often check `country_exists = ENG`. Other sponsor families from the spec are mostly absent or abstracted, so invalid sponsor cleanup is not fully represented in the decision layer.
- Northern protectorate start checks route safety and British war state through `slopx_ireland_can_start_northern_protectorate`, but it still assumes state `119` as the full Northern surface.

## Localisation and tooltip gaps

- This audit did not edit localisation by user scope.
- Decision effects generally call `custom_effect_tooltip`, which is good for hiding raw effects.
- Risk remains that mission requirements are too generic because the script does not expose named target groups beyond state highlights. Localisation may name Cobh, Berehaven, Belfast, Derry, or border counties, but the script often enforces only state ids `119`, `113`, `134`, or `135`.

## Cleanup and exploit risk notes

- Category-level active flags reduce simultaneous spam: `ireland_authority_mission_active`, `ireland_emergency_mission_active`, `ireland_industry_mission_active`, `ireland_foreign_mission_active`, `ireland_northern_mission_active`, `ireland_route_crisis_active`, and `ireland_integration_mission_active`.
- `slopx_ireland_cleanup_crisis_flags` clears major crisis route flags and calls BOP cleanup.
- Integration failure helper exists and clears the integration active flag.
- Exploit risk remains where fire-once click and wait decisions grant readiness, authority, buildings, settlement progress, or achievement flags without objective success checks. The worst risks are post-settlement stage farming through passive timers, broad state-only integration, and hidden route tasks that can resolve by waiting.

## Concrete recommended fixes

1. Convert the most important `days_remove` pseudo-missions into `activation` plus `days_mission_timeout` missions with objective `available` checks and failure `timeout_effect`.
   - Start with `ireland_border_survey_mission`, `ireland_common_platform_table_mission`, `ireland_policing_transition_stage`, and `ireland_service_continuity_stage`.

2. Add regional scripted triggers for Northern objectives.
   - File recommendation: `common/scripted_triggers/slopx_ireland_triggers.txt`
   - Needed identifiers: `slopx_ireland_controls_belfast_area`, `slopx_ireland_controls_derry_area`, `slopx_ireland_has_border_security_objective`, or equivalent state or province group helpers.

3. Make the Northern settlement decision prove more than state `119`.
   - File recommendation: `common/decisions/ireland_focus_tree_decisions.txt`
   - Identifier: `proclaim_all_island_settlement_decision`
   - It should require settlement legitimacy, low pressure, agreement, and at least one completed peaceful or protectorate objective chain.

4. Add real failure paths to short route and hidden overlay decisions.
   - File recommendation: `common/decisions/ireland_focus_tree_decisions.txt`
   - Candidate ids: `ireland_common_platform_unionist_alarm_containment`, `ireland_courier_exposure_stage`, `ireland_arms_surrender_channel`, `ireland_neutral_aftershock_recovery_mission`.

5. Expand BOP missionization.
   - File recommendation: `common/decisions/ireland_bop_decisions.txt`
   - Candidate ids: `ire_bop_coast_security_transfer`, `ire_bop_worker_production_truce`, `ire_bop_guard_discipline_case`, `ire_bop_safehouses_under_political_control` if added later.

6. Add stronger AI weighting to hidden and crisis decisions.
   - Use route flags, BOP pressure dominance, foreign access crisis, war state, equipment stockpile, and partition pressure instead of flat base weights.

7. Keep icon wiring as-is unless asset audit reports quality problems.
   - Asset reference check found matching `GFX_decision...` definitions for all decision icon references in the owned Ireland decision files.

## Meaningful validation

- Checked vanilla decision documentation for `allowed`, `visible`, `available`, targeted decision, and mission behavior.
- Checked offline wiki Decision modding, Triggers, Effects, Scopes, Localisation, Modifiers, On actions, Event modding, Idea modding, AI modding, Data structures, and National focus modding pages before gameplay inspection.
- Verified patched BOP helper references exist in `common/scripted_effects/ireland_bop_effects.txt`.
- Verified `common/decisions/ireland_bop_decisions.txt` brace balance after patch: balance `0`, minimum nesting did not go negative.
- Ran `git diff --check -- common/decisions/ireland_bop_decisions.txt`, no whitespace errors reported.
- Confirmed all `icon = GFX_decision...` references in the three Ireland decision files have matching `GFX_decision...` sprite definitions under `interface/`.

## Skipped validation

- Did not run the game or inspect runtime logs.
- Did not edit or validate localisation content because the user explicitly limited ownership to Ireland decision files and this handoff.
- Did not patch focus tree, events, achievements, assets, interface, scripted effects, scripted triggers, or AI strategy files. Findings against those surfaces are reported only.
- Normal `git diff` does not show the decision patch because `common/decisions/` is currently untracked in this worktree.

## Remaining risks

- The implementation is not yet fully canonical against the decision and mission spec because most mission families still lack active objectives, partial success, and failure outcomes.
- Northern settlement is not yet a robust staged settlement system. It is mainly a single-state gate plus staged integration chain.
- Hidden paths are present, but several overlays need deeper reveal missions, route disqualifiers, failure effects, and cleanup before they meet the hidden path ruling.
- BOP is canonical and present, but its decision layer needs more objective missions and more route-aware AI before it fully satisfies the BOP addendum.
- Achievement hooks exist, but the decision layer does not consistently document which decision or mission earns each hook.
