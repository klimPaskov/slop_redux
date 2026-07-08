# Ireland Focus Tree Closure Readiness Handoff

Date: 2026-07-08

## Recommendation

Do not add another broad Ireland expansion layer. The package is mechanically deep enough: 238 focus IDs are implemented, `IRE_state_authority_bop` exists with route-specific modes, major and flavour event layers are present, hidden overlays have focus or mission surfaces, Northern settlement is focus-prepared and decision-verified, and the Atlantic compact remains a conference or faction concept rather than a formable country.

This was not a clean closure handoff when written. The finite hardening and verification work has since been resolved by the parent patches and final completion audit recorded below.

## Prior Addendum Status

The previous addendum at `docs/plans/ireland_focus_tree/improvement_loop_addendum.md` is resolved by `docs/plans/ireland_focus_tree/improvement_loop_resolution.md`. The resolution says the requested hidden overlay, AI, achievement, localisation, and asset follow-up work was implemented rather than queued or rejected.

This closure-readiness handoff is retained as the resolved improvement-loop audit trail for final review.

## Parent Resolution Status

Parent resolution work after this handoff:

- Route-proof closure actions were converted into selectable missions where they gate route safety, settlement legitimacy, hidden overlay completion, BOP recovery, or achievement proof. Routine BOP nudges and local timed project decisions remain ordinary decisions by design. See `docs/plans/ireland_focus_tree/decision_mission_closure_resolution_2026-07-08.md`.
- A final player-facing localisation prose pass removed the reported visible implementation labels from Ireland focus, decision, BOP, achievement, major-event, and flavour-event text without adding unverified slogans, quotes, Gaelic phrases, cultural allusions, or audio cues.
- Achievement asset documentation was reconciled to the current 53 registered Ireland achievements: 36 in the original Ireland lane and 17 in the BOP/event/flavour lane.
- The BOP addendum subtree under `docs/specs/ireland_focus_tree/bop_addendum/` is retained as canonical source history inside the Ireland package, not a separate feature package.
- Static balance and route validation evidence is recorded in `docs/plans/ireland_focus_tree/balance_validation_static_2026-07-08.md`. No live HOI4 campaign run was performed in this Codex workspace.

## Basis Read

Canonical package surfaces inspected:

- `docs/specs/ireland_focus_tree/README.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_5_decisions_missions.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_11_acceptance_handoffs.md`
- `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_12_balance_of_power.md`
- Ireland asset, animation, text/audio, localisation, focus, decision, and country-package handoffs under `docs/assets/ireland_focus_tree/` and `docs/plans/ireland_focus_tree/subagent_handoffs/`

Current implementation surfaces sampled:

- `common/national_focus/ireland_focus_tree.txt`
- `common/decisions/ireland_focus_tree_decisions.txt`
- `common/decisions/ireland_bop_decisions.txt`
- `common/bop/ireland_balance_of_power.txt`
- `common/scripted_triggers/slopx_ireland_triggers.txt`
- `common/scripted_effects/slopx_ireland_effects.txt`
- `common/scripted_effects/ireland_bop_effects.txt`
- `common/ai_strategy/ireland_focus_tree_ai_strategy.txt`
- `common/achievements/ireland_focus_tree_achievements.txt`
- `common/opinion_modifiers/ireland_focus_tree_opinion_modifiers.txt`
- `localisation/english/slop_redux_l_english.yml`
- `docs/assets/ireland_focus_tree/manifest.md`
- `docs/assets/ireland_focus_tree/animation_handoff.md`

## Resolved Closure Findings

### Resolved high: remaining pseudo-mission debt on closure-proof actions

The parent patch correctly converted the major Northern/protectorate stages and selected BOP route actions to true selectable missions. Remaining closure-proof actions still use short `days_remove` or cooldown patterns and should either be converted to objective missions or explicitly documented as accepted ordinary decisions.

Implementation targets:

- `common/decisions/ireland_focus_tree_decisions.txt`
  - `ireland_hold_dail_confidence_mission`
  - `ireland_veterans_reconciliation_mission`
  - `ireland_emergency_stockpile_mission`
  - `ireland_coastwatch_posts_mission`
  - `ireland_secure_cobh_approaches`
  - `ireland_secure_berehaven_gate`
  - `ireland_lough_swilly_watch_rotation`
  - `ireland_constitutional_concession_test_mission`
  - `ireland_neutral_aftershock_recovery_mission`
  - `ireland_republican_reconciliation_backchannel`
  - `ireland_legal_worker_defence_mandate`
  - `ireland_safehouse_audit`
  - `ireland_courier_exposure_stage`
  - `ireland_arms_surrender_channel`
  - `ireland_border_cells_stand_down`
  - `ireland_army_council_reconciliation_crisis`
- `common/decisions/ireland_bop_decisions.txt`
  - review `ire_bop_public_confidence_drive`, `ire_bop_veterans_reconciliation_board`, `ire_bop_emergency_order_review`, `ire_bop_anti_basing_vote`, `ire_bop_defence_liaison_protocol`, `ire_bop_congress_mandate`, `ire_bop_cadre_mobilisation`, `ire_bop_civilian_front_conference`, `ire_bop_army_council_mandate`, `ire_bop_civic_institution_drive`, and `ire_bop_public_cultural_mobilisation` against the BOP decision matrix.

Resolution:

- Route-safety, settlement-legitimacy, BOP-recovery, hidden-overlay, and achievement-proof rows were converted into `selectable_mission = yes` with `days_mission_timeout`, objective checks, timeout effects, and route-aware AI where relevant.
- Routine repeatable pressure nudges remain ordinary decisions and are documented in `decision_mission_closure_resolution_2026-07-08.md`.

### Resolved high: localisation prose still contains implementation-facing wording

Missing keys are mostly fixed, and `ireland_sovereignty_alarm_opinion` is now defined. The remaining issue is player-facing prose quality.

Current examples in `localisation/english/slop_redux_l_english.yml`:

- `irl_atlantic_compact_gate` and `irl_atlantic_compact_gate_desc` still expose "Gate".
- `irl_audit_free_state` and `irl_tariff_scars_audit` still expose "audit/review" style implementation labels.
- `irl_army_council_state_capstone_desc`, `irl_atlantic_compact_capstone_desc`, and several route descriptions still use "capstone" or route-summary phrasing.
- `slopx_ireland_flavour.hidden_path_audit_day.*` still exposes hidden-path audit language to the player.

Resolution:

- A final prose pass removed the reported implementation labels from player-facing values.
- Hidden route text remains reveal-safe.
- No unverified Gaelic terms, quotes, slogans, cultural allusions, song fragments, or audio cues were added.

### Residual validation limit: no live campaign balance proof

No subagent handoff records a live campaign balance pass. This blocks completion, because the package spans focuses, BOP, decisions, events, AI strategy, hidden route reveals, achievements, and staged Northern settlement.

Static validation scenarios recorded:

- 1936 historical sovereign-neutral route through Emergency, ports, BOP stability, and postwar neutrality.
- Constitutional opposition through guarded cooperation, constitutional backchannel, and Northern settlement.
- Labour democratic/cooperative route through cross-border council and democratic return checks.
- Blueshirt corporatist route with and without O'Duffy, including chamber-state consolidation and sponsor containment.
- IRA route through compromised network, courier exposure, reconciliation, and Army Council pressure.
- Hidden civic restoration, Emergency directorate, Atlantic neutral compact, and neutral aftershock recovery.
- Common platform Northern settlement and Northern emergency protectorate, including regional province control, observer legitimacy, staged integration, and failed-settlement recovery.
- AI-only or hands-off checks for Britain, Northern Ireland, Germany, Italy, Spain, United States, Soviet Union, Vatican-mediated behavior, and sponsor invalidation cleanup.

Balance findings are recorded in `balance_validation_static_2026-07-08.md` against `common/national_focus/ireland_focus_tree.txt`, `common/decisions/ireland_focus_tree_decisions.txt`, `common/decisions/ireland_bop_decisions.txt`, `common/bop/ireland_balance_of_power.txt`, `events/ireland_focus_tree_events.txt`, `events/ireland_focus_tree_major_events.txt`, `events/ireland_flavour_events.txt`, and `common/ai_strategy/ireland_focus_tree_ai_strategy.txt`.

### Medium: achievement asset documentation is stale

The older country-package audit reported nine extra achievement DDS triplets. Current implementation has 53 registered Ireland achievements in `common/achievements/ireland_focus_tree_achievements.txt`, including the former BOP/flavour additions, and matching DDS triplets exist under `gfx/achievements/`.

Resolution:

- `docs/assets/ireland_focus_tree/achievement_icon_handoff.md` now records the current canonical count of 53 registered achievements and points to the 17-icon BOP/event/flavour lane.
- `docs/assets/ireland_focus_tree_bop/manifest.md` is retained as a resolved subpackage feeding the implemented parent achievement registry.

Result:

- No extra achievement DDS triplet remains orphaned; the 36 original lane plus 17 BOP/event/flavour lane cover the 53 registered ids.

### Medium: documentation still carries a separate BOP addendum subtree

The current user and parent constraint says the canonical Ireland specs include BOP and there is no separate BOP spec package to use. The repo still contains `docs/specs/ireland_focus_tree/bop_addendum/`.

Resolution:

- `docs/specs/ireland_focus_tree/README.md`, `docs/specs/ireland_focus_tree/bop_addendum/README.md`, and `docs/specs/ireland_focus_tree/bop_addendum/ireland_bop_planning_state.md` now mark the subtree as retained canonical source history, not a separate implementation package.

## Non-Blocking Follow-Up

- Run final focus tree, decision/mission, localisation, country package, and feature completion audits after the blockers above are handled.
- Confirm `IRE_ALL_ISLAND` remains the only identity change tied to all-island settlement and that it still occurs only after `slopx_ireland_can_proclaim_all_island_settlement`.
- Keep the Atlantic compact as a conference/faction compact. Do not add an Atlantic formable country.
- Keep Northern settlement verified by focus preparation plus decisions/missions. Do not turn it into a claim ladder.

## Asset And Subagent Routing

Assets must follow `hoi4-feature-assets` and `hoi4-frame-animation`.

No final asset may be a simple-shape placeholder, geometric diagram, flat icon stand-in, transform-only animation, recolor-only animation, glow-only animation, or resized reuse of an unrelated lane. Final assets must be generated, sourced, or user-provided artwork, then processed into the correct HOI4 sizes and documented in a manifest.

Keep asset lanes separate:

- Focus icons: `hoi4_icon_artist`, final DDS in `gfx/interface/goals/`, sprite names such as `GFX_goal_ireland_*`.
- Idea and dynamic modifier icons: `hoi4_icon_artist`, final DDS in `gfx/interface/ideas/`, sprite names such as `GFX_idea_ireland_*`.
- Decision and decision category icons: `hoi4_icon_artist`, final DDS in `gfx/interface/decisions/` and `gfx/interface/decisions/categories/`, sprite names such as `GFX_decision_ireland_*`.
- Achievement icons: `hoi4_icon_artist`, final root DDS triplets in `gfx/achievements/<achievement_id>{,_grey,_not_eligible}.dds`; do not wire achievement icons through focus or decision sprites.
- Event and report art: `hoi4_generated_feature_art` for fictional/generated period-style art, or `hoi4_asset_source_researcher` if real historical photos, symbols, flags, offices, portraits, or documents are requested.
- Animated seals and animated UI pieces: asset subagent must use `hoi4-frame-animation`; require separate source frames, processed frames, static fallback, DDS framesheet, contact sheet, preview, manifest, and `.gfx`/`.gui` handoff. No transform-only or single-still animation is acceptable.

Asset subagents produce source files, processed PNGs, DDS outputs, contact sheets, manifests, and handoffs. The parent implementation agent owns `.gfx` wiring, gameplay references, localisation references, documentation alignment, and final validation.

## Text And Audio Routing

No unverified quotes, slogans, Gaelic phrases, cultural allusions, song or poem fragments, exact headlines, prayers, speeches, or audio cues should be added.

The existing text/audio gate handoff allows plain in-world prose and a small set of sourced institutional terms. Any new source-dependent text must go through `hoi4_quote_remark_researcher`. Any audio must go through `hoi4_audio_researcher` with exact use, duration, mood, license, source file, and final path.

## What Should Not Be Added

- No new ordinary political route.
- No church government route.
- No monarchy, high-kingship, occult, pan-Celtic, or fantasy cultural route.
- No Atlantic formable country.
- No new scripted GUI board unless the parent explicitly accepts a separate UI package after closure blockers are resolved.
- No new country tags for Northern actors unless a later accepted design proves a map-control reason.
- No new BOP mechanic. Use the existing `IRE_state_authority_bop`.

## Promotion Note

Keep this file in `docs/plans/ireland_focus_tree/` until resolved. It should not be promoted wholesale into `docs/specs/ireland_focus_tree/`, because it is a closure-readiness note rather than new source design.

If the parent accepts the blocker list as the final completion gate, promote only a concise final acceptance checklist into `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_11_acceptance_handoffs.md` or a compact closure report. The main canonical design does not need another expansion spec.
