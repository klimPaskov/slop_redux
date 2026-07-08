# Ireland focus tree canonical audit handoff, 2026-07-08

Scope: `common/national_focus/ireland_focus_tree.txt` against the canonical top-level package in `docs/specs/ireland_focus_tree/`, excluding the stale `bop_addendum` subtree per current user constraint that BOP is already part of the canonical package.

Skills and references applied: `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-events`, `hoi4-feature-assets`, `hoi4-improvement-loop`, `hoi4-subagents`; AGENTS.md; offline wiki pages for data structures, triggers, effects, modifiers, localisation, scopes, on actions, events, decisions, ideas, AI, national focuses, BOP, and graphical assets; vanilla documentation for effects, triggers, modifiers, and script concepts.

## Patch summary

Changed files:

| File | Change |
| --- | --- |
| `common/national_focus/ireland_focus_tree.txt` | Added `allow_branch` reveal gates for `irl_hidden_cultural_reveal_gate` and `irl_atlantic_compact_gate`; added BOP cleanup mode switch to `irl_restore_civilian_rule`. |
| `docs/plans/ireland_focus_tree/subagent_handoffs/focus_tree_canonical_audit_2026-07-08.md` | This audit handoff. |

Changed focus IDs:

| Focus ID | Before | After |
| --- | --- | --- |
| `irl_hidden_cultural_reveal_gate` | Publicly visible once its parent path was visible, only disabled by `available = { slopx_ireland_can_reveal_civic_hidden_path = yes }`. | Hidden by `allow_branch = { slopx_ireland_can_reveal_civic_hidden_path = yes }` until the public reveal conditions are met. |
| `irl_atlantic_compact_gate` | Publicly visible once its parent path was visible, only disabled by `available = { slopx_ireland_can_reveal_atlantic_hidden_path = yes }`. | Hidden by `allow_branch = { slopx_ireland_can_reveal_atlantic_hidden_path = yes }` until the public reveal conditions are met. |
| `irl_restore_civilian_rule` | Set restoration flags and authority, but left Ireland in Emergency Directorate BOP mode. | Calls `ire_bop_set_mode_historical_emergency = yes` before the authority reward, closing the directorate BOP mode after civilian restoration. |

Localisation keys changed: none. Icon IDs changed: none.

## Route coverage table

| Route family | Canonical expectation | Implementation status | Evidence |
| --- | --- | --- | --- |
| Opening constitutional trunk | Free State audit, civil war wounds, ports/economic war, emergency skeleton, route lock. | Covered. | `irl_audit_free_state` through `irl_support_lanes_open`, `common/national_focus/ireland_focus_tree.txt:17-266`. |
| Historical sovereign neutrality | Constitution, ports return, strict neutrality, Emergency cabinet, Plan W, postwar legal claim. | Covered. | `irl_bunreacht_referendum` through `irl_de_valera_settlement_capstone`, `common/national_focus/ireland_focus_tree.txt:278-542`. |
| Constitutional opposition/Commonwealth | Legal opposition, guarded cooperation, treaty review, boundary bargain, democratic settlement. | Covered. | `irl_rebuild_opposition_benches` through `irl_democratic_all_island_settlement`, `common/national_focus/ireland_focus_tree.txt:559-598`. |
| Labour/social republic | Dail Labour, unions, welfare, worker defence, anti-fascist route, all-island congress. | Covered. | `irl_labour_in_dail` through `irl_international_anti_fascist_capstone`, `common/national_focus/ireland_focus_tree.txt:598-638`. |
| Blueshirt corporatist | O'Duffy/Guard, corporate chambers, anti-communist diplomacy, Ulster hard route. | Covered. | `irl_national_guard_revival` through `irl_corporate_militarized_capstone`, `common/national_focus/ireland_focus_tree.txt:638-677`. |
| IRA underground | Army Council, cells, German courier, Plan Kathleen, Northern uprising, revolutionary republic. | Covered. | `irl_army_council_speaks` through `irl_army_council_state_capstone`, `common/national_focus/ireland_focus_tree.txt:678-717`. |
| Industry/economy support | Native manufactures, rural/ports recovery, turf, rationing, route economy variants. | Covered. | `irl_tariff_scars_audit` through `irl_trade_balanced_capstone`, `common/national_focus/ireland_focus_tree.txt:718-740`. |
| Military/Emergency defence | Army establishment, LDF/LSF, coastwatching, port commands, Air Corps, G2, invasion plan. | Covered. | `irl_army_establishment_review` through `irl_invasion_response_plan`, `common/national_focus/ireland_focus_tree.txt:741-765`. |
| Diplomacy/neutrality | League, London/Washington/Vatican, pressure tracks, sponsor balancing, neutrality capstone. | Covered. | `irl_league_voice` through `irl_neutrality_capstone`, `common/national_focus/ireland_focus_tree.txt:766-786`. |
| Northern settlement | Observer/legal/economic/military tracks, settlement office, integration, no direct claim ladder. | Covered in focus file; decision verification exists outside owned file. | `irl_border_survey` through `irl_all_island_administration`, `common/national_focus/ireland_focus_tree.txt:787-812`; `slopx_ireland_prepare_all_island_settlement` focus hooks; `proclaim_all_island_settlement_decision`, `common/decisions/ireland_focus_tree_decisions.txt:937`. |
| Late route capstones | Postwar conference, emergency lessons, route late payoffs, second-stage guardrails. | Covered, with some reward repetition. | `irl_postwar_neutrality_conference` through `irl_route_mastery_achievements_gate`, `common/national_focus/ireland_focus_tree.txt:814-833`. |
| Hidden civic/common platform | Reveal ladder, civic route, common platform settlement support. | Partly covered; reveal gate patched. Decision loop depth remains a non-focus risk. | `irl_hidden_cultural_reveal_gate` through `irl_civic_restoration_capstone`, `common/national_focus/ireland_focus_tree.txt:826-842`. |
| Hidden Emergency Directorate | Crisis reveal, G2/LDF/order/directorate, restore or entrench fork. | Covered; cleanup patched for restoration BOP mode. | `irl_emergency_directorate_warning` through `irl_permanent_security_state`, `common/national_focus/ireland_focus_tree.txt:844-850`. |
| Hidden Atlantic compact | Gate, shipping observers, arbitration, no-basing, member rules, compact capstone. | Covered; reveal gate patched. | `irl_atlantic_compact_gate`, `irl_hidden_neutral_conference_gate` through `irl_atlantic_compact_capstone`, `common/national_focus/ireland_focus_tree.txt:829` and `852-857`. |
| Mandatory route-specific hidden overlays from part 10 | Compromised republican network, cross-border Labour Council, constitutional backchannel, corporate chambers without O'Duffy, republican reconciliation, neutral aftershock, Northern emergency protectorate. | Simplified or mostly external to focus tree; not represented as full focus overlay families in the 238 focus IDs. | Spec requires these at `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:396` and `:464`; focus file has flags/hooks such as `ireland_constitutional_backchannel_open`, `ireland_cross_border_labour_council_visible`, and decision/effect references, but no full overlay focus groups. |

## High-priority findings

1. Fixed: hidden reveal gate exposure. `irl_hidden_cultural_reveal_gate` and `irl_atlantic_compact_gate` were visible before earned because they used `available` only. Added `allow_branch` predicates at `common/national_focus/ireland_focus_tree.txt:826` and `:829`.

2. Fixed: missing BOP cleanup on directorate recovery. `irl_restore_civilian_rule` now calls `ire_bop_set_mode_historical_emergency = yes` at `common/national_focus/ireland_focus_tree.txt:849`.

3. Remaining: hidden AI weights are still too broad for the spec. The spec says AI must not choose hidden paths because they are visible by accident and should have explicit validity checks (`docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:341`). Focus-level AI on hidden focuses is still flat: civic route factors around 3, directorate factors 1-3, Atlantic factors 4. `common/ai_strategy/ireland_focus_tree_ai_strategy.txt` has route strategies, but the focus file itself does not enforce rare historical/democratic/crisis-only selection.

4. Remaining: the corrupted restoration failure path is represented by `irl_cultural_corruption_guardrail` and `slopx_ireland_trigger_corrupted_restoration_failure`, but AI is not disabled at focus level (`ai_will_do = { factor = 3 }` at `common/national_focus/ireland_focus_tree.txt:827`). The spec says corrupted restoration failure AI access is disabled (`docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:29`).

5. Remaining: mandatory hidden overlays are not full focus overlays. Part 10 expands hidden content beyond the five primary paths; implementation mostly exposes flags, decisions, or helper hooks instead of focus groups. This is broader than a small subagent patch and needs parent design triage.

## Missing or simplified content list

| Area | Finding | Reference |
| --- | --- | --- |
| Hidden overlay depth | Route-specific hidden overlays listed in Part 10 are not full focus branches. | `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:396`, `:464`, `:687`. |
| Civic hidden loop | Civic route focuses mostly call shared helpers; the spec expects staged decisions/missions for civil service, Gaeltacht routes, schools, contacts, minority guarantees, and diaspora links. | Focuses at `common/national_focus/ireland_focus_tree.txt:835-842`; decision-loop spec at `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:102`. |
| Atlantic compact loop | Focus sequence exists, but the focus file itself cannot prove member goals, observer validation, compact collapse, or no-formable cleanup. | `common/national_focus/ireland_focus_tree.txt:852-857`; spec at `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:215`. |
| Reward variety | Several route stretches use repeated shared rewards (`slopx_ireland_hidden_civic_focus_effect`, `slopx_ireland_hidden_atlantic_focus_effect`, route focus effects). This is functional but less expressive than the spec's focus-specific rewards and mission hooks. | `common/national_focus/ireland_focus_tree.txt:835-842`, `:852-857`. |
| Cleanup hooks | BOP cleanup for directorate recovery was patched. Other cleanup promises for hidden overlays, obsolete decisions, and failure missions depend on decisions/effects outside owned files and were not changed. | Patched `common/national_focus/ireland_focus_tree.txt:849`; broader cleanup spec at `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:33-43`. |

## Icon coverage table

| Check | Result | Evidence |
| --- | --- | --- |
| Focus icon IDs used by tree | 21 unique `GFX_goal_ireland_*` icons. | Parsed from `common/national_focus/ireland_focus_tree.txt`. |
| Sprite definitions | 21/21 defined. | `interface/ireland_focus_tree.gfx:399-521`. |
| DDS files | 21/21 referenced files exist under `gfx/interface/goals/`. | Scripted existence check against `.gfx` texturefile paths. |
| Hidden icons | `GFX_goal_ireland_hidden_civic`, `GFX_goal_ireland_hidden_directorate`, `GFX_goal_ireland_hidden_atlantic`, and `GFX_goal_ireland_hidden_common` are defined and used. | `interface/ireland_focus_tree.gfx:435-455`; focus uses at `common/national_focus/ireland_focus_tree.txt:826-857`. |
| Asset quality | Asset handoffs/manifest indicate generated symbolic assets and explicitly reject simple-shape fallback in several batches. | `docs/assets/ireland_focus_tree/focus_icon_handoff.md`; `docs/assets/ireland_focus_tree/manifest.md`; source-quality notes such as `docs/assets/ireland_focus_tree/achievement_source_repair_batch_2c_handoff.md`. |

No icon files or interface files were edited.

## Localisation and reward mismatch list

| Check | Result |
| --- | --- |
| Focus name keys | 238/238 present in `localisation/english/slop_redux_l_english.yml`. |
| Focus description keys | 238/238 present in `localisation/english/slop_redux_l_english.yml`. |
| Localisation edits | None made, per ownership constraint. |
| Reward helper existence | 53 called `slopx_ireland_*`/`ire_bop_*` helpers from focus file resolve in `common/scripted_effects/` or `common/scripted_triggers/`. |
| Supported direct effects | Direct focus effects checked against the consulted effects documentation; no unsupported direct effect was found in the focus file during this audit. |
| Northern settlement reward match | Focus rewards prepare or advance settlement and unlock flags; they do not directly create a claim ladder. Decision-verified settlement exists via `proclaim_all_island_settlement_decision`. |

Potential mismatch retained: some focus names promise specific institutional content but reward through broad helper effects. This is a depth/variety issue rather than a missing-key issue.

## BOP, identity, and Northern settlement findings

| Area | Status |
| --- | --- |
| BOP route entry modes | Route entries call BOP mode helpers: historical, Commonwealth, Labour, Blueshirt, IRA at `common/national_focus/ireland_focus_tree.txt:296`, `:577`, `:616`, `:656`, `:696`. |
| Hidden BOP modes | Civic and directorate reveals call `ire_bop_set_mode_civic_cultural` and `ire_bop_set_mode_emergency_directorate` in `common/scripted_effects/slopx_ireland_effects.txt:418-437`. |
| Directorate recovery | Patched in focus file: `irl_restore_civilian_rule` now returns to historical emergency BOP mode. |
| Focus-prepared identity changes | Route identities are set by helper effects, while all-island identity is decision-verified. `slopx_ireland_complete_all_island_settlement` sets `set_cosmetic_tag = IRE_ALL_ISLAND` only after `slopx_ireland_can_proclaim_all_island_settlement`. |
| Northern settlement not a claim ladder | Focus file has no direct `add_state_claim` or `create_wargoal` in Northern settlement route. The all-island result is gated through `proclaim_all_island_settlement_decision` and `slopx_ireland_complete_all_island_settlement`. |

## AI behavior gaps

| Gap | Impact | Reference |
| --- | --- | --- |
| Hidden focus AI weights are flat and nonzero. | AI can pursue hidden content too readily once gates are met, instead of very rare or crisis-only behavior. | `common/national_focus/ireland_focus_tree.txt:826-857`; spec AI rule at `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:327-341`. |
| Corrupted restoration AI not disabled at focus level. | Violates hidden path AI table for trap/failure branch. | `common/national_focus/ireland_focus_tree.txt:827`; spec at `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_10_hidden_paths.md:29`. |
| Route-aware AI exists mostly as strategy, not focus selection. | Country strategy reacts to route flags, but focus selection still uses simple factors through most route stretches. | `common/ai_strategy/ireland_focus_tree_ai_strategy.txt:8-58`, `:387-390`; focus AI factors throughout `common/national_focus/ireland_focus_tree.txt`. |

## Validation evidence

- Parsed canonical top-level spec IDs from `docs/specs/ireland_focus_tree/`: 238 unique `irl_*` IDs.
- Parsed `common/national_focus/ireland_focus_tree.txt`: 238 focus blocks, 238 unique IDs, zero duplicates, zero missing spec IDs, zero extra implementation IDs.
- Prerequisite/mutual-exclusion reference scan: zero references to missing focus IDs.
- Post-patch reveal checks: `irl_hidden_cultural_reveal_gate` and `irl_atlantic_compact_gate` both have `allow_branch`; `irl_restore_civilian_rule` has `ire_bop_set_mode_historical_emergency`.
- Icon scan: 21 focus icon IDs used, 21 definitions found, 21 referenced DDS files exist.
- Localisation scan: zero missing focus name keys and zero missing focus description keys.
- Helper scan: all 53 called focus helper tokens are defined in scripted effects/triggers.

Skipped meaningful validation:

- No game load was run from this subagent pass.
- No edits or validation fixes were made in localisation, assets, decisions, events, interface, or AI strategy files due the user ownership constraint.
- Asset quality was checked through existing manifests/handoffs and file presence, not by re-rendering or visually inspecting every DDS.

## Remaining route risks

- Hidden route implementation is present but still thinner than the Part 10 hidden-path design, especially route-specific overlays and mission loops.
- AI route rarity and failure-branch avoidance need a focused AI/focus-weight pass.
- Several late/hidden rewards rely on broad helper effects; parent should decide whether more focus-specific rewards are required before declaring the Ireland tree complete.
- The `bop_addendum` subtree still exists under `docs/specs/ireland_focus_tree/` even though the current user constraint says the separate BOP package was deleted. I ignored it for canonical ID parity, but parent documentation cleanup may need to remove or mark it superseded.
