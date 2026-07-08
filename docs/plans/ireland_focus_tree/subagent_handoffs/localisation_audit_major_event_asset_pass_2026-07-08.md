# Ireland Localisation Audit - Major Event and Asset Wiring Pass

Date: 2026-07-08
Agent: localisation subagent
Scope: `localisation/english/slop_redux_l_english.yml`; audit references across Ireland focus, decisions/missions, BOP, achievements, ideas, dynamic/opinion modifiers, scripted triggers/effects, and the three Ireland event files named by the parent.

## Summary

The localisation file keeps the required UTF-8 BOM, has no `:0` keys, and no duplicate or malformed localisation lines were found in the audited file. The first mechanical pass found seven concrete missing keys tied to the Ireland focus tree and tech bonus references. A narrower follow-up also found one missing opinion-modifier display key used by a scripted effect. Those were patched locally. A follow-up scan of the scoped Ireland files found no remaining missing localisation references from the audited surfaces.

The larger unresolved issue is wording quality, not key coverage. Many Ireland strings still read like implementation notes or design/audit labels instead of player-facing game text. I did not rewrite that broad set because it crosses many focuses, events, achievements, and flavour records, and the parent explicitly limited this subagent to concrete local localisation fixes.

## Files Changed

- `localisation/english/slop_redux_l_english.yml`
- `docs/plans/ireland_focus_tree/subagent_handoffs/localisation_audit_major_event_asset_pass_2026-07-08.md`

## Changed Keys

Added missing keys:

- `slopx_ireland_focus_tree`
- `slopx_ireland_focus_tree_desc`
- `ireland_army_reform_bonus`
- `ireland_emergency_stores_bonus`
- `ireland_grid_and_power_bonus`
- `ireland_observation_bonus`
- `ireland_small_arms_bonus`
- `ireland_sovereignty_alarm_opinion`

Changed concrete wording issues:

- `irl_bunreacht_referendum`
- `irl_bunreacht_referendum_desc`
- `irl_gaeltacht_development_board`
- `irl_gaeltacht_development_board_desc`
- `slopx_ireland_flavour.broadcast_language_slot.desc`
- `slopx_ireland_flavour.gaeltacht_grant_queue.t`
- `slopx_ireland_flavour.gaeltacht_grant_queue.desc`
- `slopx_ireland_flavour.gaelic_league_local_split.t`
- `slopx_ireland_flavour.gaelic_league_local_split.desc`
- `slopx_ireland_flavour.oduffy_letter_arrives.t`
- `slopx_ireland_flavour.oduffy_letter_arrives.desc`
- `slopx_ireland_flavour.gaeltacht_guard_post_dispute.t`

## Display Before and After

Before:

- Ireland focus tree and five tech bonus references could render as raw localisation keys.
- `ireland_sovereignty_alarm_opinion` could render as a raw localisation key if the referenced modifier is added by the owning gameplay pass.
- A few visible strings used unverified or malformed Gaelic/cultural labels, including `Radio ireann`, `Bunreacht`, `Gaeltacht`, `Conradh na gaeilge`, and `Oduffy`.

After:

- The missing focus tree and tech bonus keys now have visible English labels.
- `ireland_sovereignty_alarm_opinion` now has a visible English label.
- The concrete unverified/malformed Gaelic/cultural labels were replaced with plain English wording where a small local patch was safe.
- `Oduffy` was corrected to `O'Duffy`.

## Missing Key List

Pre-patch missing keys:

- `slopx_ireland_focus_tree`
- `slopx_ireland_focus_tree_desc`
- `ireland_small_arms_bonus`
- `ireland_grid_and_power_bonus`
- `ireland_emergency_stores_bonus`
- `ireland_army_reform_bonus`
- `ireland_observation_bonus`
- `ireland_sovereignty_alarm_opinion`

Post-patch missing keys in the audited Ireland surfaces: none found.

## Duplicate Key List

No duplicate keys were found in `localisation/english/slop_redux_l_english.yml`.

## Scripted Localisation Issues

- No unresolved `$nested$` references were found in the localisation file after the patch.
- No broken scripted-localisation file reference was found in the audited localisation file.
- Existing variable/value display syntax used by Ireland ledgers and dynamic descriptions was left intact.

## Dynamic Text Opportunities

These were not patched because they need owning-system review or broader gameplay/UI context:

- Several decision and BOP requirement strings could be clearer if they used shared dynamic values for duration, state, mandate, or alignment thresholds.
- Some flavour records refer to specific states by prose or static phrasing. If the owning gameplay pass already has state targets available, dynamic state names would be safer than static descriptions.
- Some availability and blocked-requirement text for Ireland route gates would read better with custom tooltips attached to the scripted triggers instead of player-facing generic trigger output.
- Several focus and event descriptions refer to route state with implementation labels such as `capstone`, `route lock`, or `gate`; dynamic route names would make these read less like design notes.
- `common/scripted_effects/ireland_flavour_effects.txt` uses `ireland_sovereignty_alarm_opinion`, but `common/opinion_modifiers/ireland_focus_tree_opinion_modifiers.txt` does not define that modifier. I added the localisation key only; the missing modifier definition is an owning-gameplay follow-up.

## Cross-Surface Mismatch Notes

The current Ireland localisation has a broad generated/implementation-wording debt. Representative keys and patterns:

- Focus descriptions such as `irl_account_for_economic_war_desc`, `irl_bog_mechanisation_trials_desc`, `irl_british_trade_reopening_desc`, `irl_self_sufficient_economy_capstone_desc`, and `irl_trade_balanced_capstone_desc` include phrases like `reward is tied`, `loose stockpiles`, or `capstone`.
- Defence and army focus descriptions such as `irl_air_corps_observation_desc`, `irl_air_observation_ring_desc`, `irl_army_establishment_review_desc`, `irl_baldonnel_training_desc`, `irl_local_defence_force_desc`, and `irl_template_modernisation_desc` use `free formations` wording.
- Several focus or decision labels include design/audit terms, including `irl_audit_free_state`, `irl_foreign_access_audit`, `irl_tariff_scars_audit`, `ireland_safehouse_audit`, `irl_atlantic_compact_gate`, `irl_political_route_lock`, and `irl_social_republic_route_lock`.
- Achievement descriptions such as `ireland_focus_tree_atlantic_compact_DESC`, `ireland_focus_tree_ballot_to_belfast_DESC`, `ireland_focus_tree_blueshirt_brittle_victory_DESC`, `ireland_focus_tree_constitutional_neutrality_mastery_DESC`, and `ireland_focus_tree_labour_without_dependency_DESC` still use phrasing like `not a formable country`, `not a bare claim chain`, or `capstone`.
- Flavour and focus event text under `slopx_ireland_flavour.*` and `slopx_ireland_focus.*` contains player-visible implementation wording such as `live Ireland mechanics`, `Open a local task`, `practical file`, `route record`, `mechanics`, and hidden-path audit language.

## File Encoding Concerns

- `localisation/english/slop_redux_l_english.yml` starts with a UTF-8 BOM after the patch.
- No `:0` keys were found.
- No malformed localisation lines were found by the scoped parser.
- Git warned that LF line endings in `localisation/english/slop_redux_l_english.yml` may be replaced by CRLF when Git touches the file. That is a line-ending hygiene concern, but the file still validates as UTF-8 BOM.

## Recommended Fixes

Recommended parent follow-up in `localisation/english/slop_redux_l_english.yml`:

- Rewrite implementation-history and design-label phrases in Ireland focus descriptions so they describe world state and player choices, not mechanics or audit history.
- Replace `capstone`, `route lock`, `gate`, `audit`, `free formations`, `loose stockpiles`, and `reward is tied` in player-facing strings with in-world alternatives.
- Review hidden-route and secret-path strings to make sure they do not reveal secret route content before it is intended.
- Review all cultural, Gaelic, slogan, quote, and public-audio references against the text/audio research package before restoring any Irish-language names or historically specific allusions.
- Move recurring blocked-requirement and state/control phrasing into custom tooltips or scripted localisation only after the owning gameplay files expose stable values/scopes.

## Validation Evidence

Scoped validation after the patch checked:

- UTF-8 BOM presence: yes
- Localisation lines: 2,238
- Parsed keys: 2,233
- Malformed localisation lines: 0
- `:0` localisation keys: 0
- Duplicate localisation keys: 0
- Missing referenced keys in audited Ireland surfaces: 0
- Unresolved nested `$...$` references: 0

Audited reference surfaces:

- `common/national_focus/ireland_focus_tree.txt`
- `common/decisions/ireland_focus_tree_decisions.txt`
- `common/decisions/ireland_bop_decisions.txt`
- `common/decisions/ireland_flavour_decisions.txt`
- `common/bop/ireland_balance_of_power.txt`
- `common/achievements/ireland_focus_tree_achievements.txt`
- `common/ideas/ireland_focus_tree_ideas.txt`
- `common/dynamic_modifiers/ireland_focus_tree_dynamic_modifiers.txt`
- `common/opinion_modifiers/ireland_focus_tree_opinion_modifiers.txt`
- `events/ireland_focus_tree_events.txt`
- `events/ireland_focus_tree_major_events.txt`
- `events/ireland_flavour_events.txt`
- `common/scripted_triggers/slopx_ireland_triggers.txt`
- `common/scripted_triggers/ireland_bop_triggers.txt`
- `common/scripted_triggers/ireland_flavour_triggers.txt`
- `common/scripted_effects/slopx_ireland_effects.txt`
- `common/scripted_effects/ireland_bop_effects.txt`
- `common/scripted_effects/ireland_major_event_effects.txt`
- `common/scripted_effects/ireland_flavour_effects.txt`

## Skipped Validation

- No in-game UI pass was run.
- No web research or new source verification was performed.
- No gameplay, event, focus, decision, interface, asset, or scripted GUI files were edited.
- No broad rewrite was attempted for all implementation-like prose because that would exceed the local patch scope.

## Unresolved Wording Decisions

- Whether to restore exact Irish-language terms such as `Dail`/`Dáil`, `Bunreacht`, `Gaeltacht`, or organisation names depends on a verified text/audio research package.
- Whether hidden-route audit text should remain player-visible needs route-design owner review.
- Whether achievement descriptions should use mechanical shorthand or fully in-world requirements needs parent style direction.
- Several generated flavour records likely need a prose pass rather than isolated key edits.
