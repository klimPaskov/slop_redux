# Ireland country package audit - focus tree implementation

Subagent: country package audit
Date: 2026-07-08

## Scope

Audited Ireland country setup surfaces owned by this pass:

- `history/`
- `common/ideas/`
- `common/achievements/`
- `common/ai_strategy/`
- `common/bop/`
- `common/dynamic_modifiers/`
- `common/opinion_modifiers/`
- `gfx/flags/`
- `gfx/achievements/`
- `gfx/interface/ideas/`
- `gfx/interface/bop/`

Read-only integration references checked where needed: `common/national_focus/ireland_focus_tree.txt`, `common/decisions/ireland_bop_decisions.txt`, `common/scripted_effects/slopx_ireland_effects.txt`, `common/scripted_effects/ireland_bop_effects.txt`, `common/scripted_triggers/ireland_bop_triggers.txt`, `events/ireland_focus_tree_events.txt`, `interface/ireland_focus_tree.gfx`, `interface/ireland_focus_tree_bop.gfx`, and `localisation/english/slop_redux_l_english.yml`.

## Country Package Coverage Checklist

- Country playable setup: covered. `history/countries/IRE - Ireland.txt` keeps capital `113`, vanilla OOBs `IRE_1936` and `IRE_1939`, 3 research slots, starting convoys, democratic politics, and Ireland-specific starting ideas.
- Focus tree loading hook: covered. `common/national_focus/ireland_focus_tree.txt` defines `slopx_ireland_focus_tree` with `tag = IRE`; `history/countries/IRE - Ireland.txt` initializes mechanics through `slopx_ireland_initialize_mechanics`.
- Leaders and portraits: covered. Ireland recruits vanilla real Ireland character ids, including `IRE_Éamon_de_valera`; bytes match vanilla despite console mojibake in some PowerShell output. Real leader portrait sourcing remains inherited from vanilla.
- Ideas and dynamic modifiers: covered and patched. Starting ideas and ledger ideas resolve to existing idea sprites after the picture token fix. `slopx_ireland_mechanics_dynamic_modifier` resolves to `GFX_idea_ireland_mechanics`.
- Achievements and icons: covered. The 44 registered Ireland achievements all have complete root `gfx/achievements/<id>{,_grey,_not_eligible}.dds` triplets at `64x64`.
- AI strategy: covered. All AI strategy tags resolve in vanilla country tags. All `has_completed_focus = irl_*` references in `common/ai_strategy/ireland_focus_tree_ai_strategy.txt` resolve to current focus ids.
- Balance of power: covered. `IRE_state_authority_bop` exists once, the BOP decision category exists, BOP event ids `.19-.29` exist, and all 16 BOP side icons resolve to `72x88` DDS textures matching vanilla BOP side precedent.
- Opinion modifiers: covered. `ireland_guarded_channel_opinion`, `ireland_no_basing_principle_opinion`, and `ireland_atlantic_observer_opinion` are present and structurally local.
- Flags and cosmetic identity: covered. `IRE_ALL_ISLAND` cosmetic tag is set in `slopx_ireland_proclaim_all_island_settlement`, has localisation keys, and has normal/medium/small TGA flag variants with expected dimensions.

## File Surface Checklist

- `history/countries/IRE - Ireland.txt`: checked playable setup, leaders, ideas, initialization, 1939 focus completion, OOBs, politics, and technologies.
- `history/states/119-Northern Ireland.txt`: checked owner, cores, buildings, VPs, provinces, resources, and explicit delayed-Ireland-core comment.
- `common/ideas/ireland_focus_tree_ideas.txt`: patched `picture` values and checked allowed scopes/modifiers.
- `common/dynamic_modifiers/ireland_focus_tree_dynamic_modifiers.txt`: checked original-tag gating and icon reference.
- `common/achievements/ireland_focus_tree_achievements.txt`: checked registered ids and icon triplets.
- `common/ai_strategy/ireland_focus_tree_ai_strategy.txt`: checked tags and focus id references.
- `common/bop/ireland_balance_of_power.txt`: checked BOP id uniqueness, side ids, range ids, icons, decision category, and event references.
- `common/opinion_modifiers/ireland_focus_tree_opinion_modifiers.txt`: checked modifier ids and values.
- `gfx/flags/**/IRE_ALL_ISLAND*.tga`: checked existence, dimensions, 32-bit depth, and non-top-origin headers.
- `gfx/achievements/ireland*.dds`: checked root achievement triplets and `64x64` dimensions.
- `gfx/interface/ideas/idea_ireland*.dds` and `gfx/interface/ideas/ireland_focus_tree_bop/idea_ire_bop_state_authority.dds`: checked existence and `64x64` dimensions.
- `gfx/interface/bop/ireland_focus_tree_bop/*.dds`: checked existence and `72x88` dimensions against vanilla BOP side icons.

## Missing Or Stale Country Package Surfaces

- Stale or queued achievement icon triplets exist without matching registered achievements in `common/achievements/ireland_focus_tree_achievements.txt`:
  - `ireland_focus_tree_balanced_authority`
  - `ireland_focus_tree_cabinet_over_emergency`
  - `ireland_focus_tree_events_of_the_island`
  - `ireland_focus_tree_flavour_coastwatch_without_scandal`
  - `ireland_focus_tree_flavour_merchant_marine_memory`
  - `ireland_focus_tree_flavour_safeguards_without_coercion`
  - `ireland_focus_tree_flavour_schools_without_corruption`
  - `ireland_focus_tree_flavour_winter_fuel_limited_powers`
  - `ireland_focus_tree_no_one_commands_the_council`
- These ids are documented in `docs/assets/ireland_focus_tree_bop/manifest.md` and `docs/specs/ireland_focus_tree/prompts/ireland_focus_tree_achievement_prompt.md`, so they look like planned or superseded achievement assets rather than missing files. They should be registered, explicitly queued, or removed from final asset manifests by the parent.

Parent resolution: all nine ids listed above were registered in `common/achievements/ireland_focus_tree_achievements.txt`, localised in `localisation/english/slop_redux_l_english.yml`, and verified against completed, grey, and not-eligible DDS triplets under `gfx/achievements/`.

## Map And State Setup Issues

- No blocking map setup issue found in owned surfaces.
- `history/states/119-Northern Ireland.txt` intentionally removes the vanilla Ireland core from state 119 and keeps `ENG`/`NIR` cores only. This matches the file comment: Ireland receives the core through the all-island integration chain.
- State 119 has owner `ENG`; no explicit controller is set, so controller follows owner at start.
- Vanilla Ireland states `113`, `134`, and `135` remain Ireland-owned/core through vanilla state history.

## Politics, Leader, Portrait, Flag, Advisor, And Party Issues

- No broken leader or advisor ids found. Ireland history recruits real vanilla Ireland characters from `common/characters/IRE.txt`.
- `IRE_Éamon_de_valera` displays as mojibake in some shell output, but the mod file bytes match vanilla UTF-8 bytes.
- No generated portrait use was found in the owned country setup surface.
- `IRE_ALL_ISLAND` flag files exist in normal, medium, and small sizes, using the base tricolour identity documented in the asset handoff.
- Party identity changes are driven by `slopx_ireland_set_*_identity` scripted effects outside this subagent's edit scope. No owned-surface party patch was needed.

## Focus, Decision, Idea, And Asset Issues

- Patched a concrete idea sprite bug: HOI4 idea `picture = foo` resolves to `GFX_idea_foo`; the file previously used `picture = GFX_idea_...`, which would resolve to missing `GFX_idea_GFX_idea_...` sprites.
- `common/national_focus/ireland_focus_tree.txt` loads for `tag = IRE`. This covers playable Ireland. If the parent expects civil-war or released copies with `original_tag = IRE` to receive the bespoke tree, the focus-tree owner should review the loading block; this audit did not edit focus files.
- BOP `decision_category = ireland_state_authority_bop_category` resolves in `common/decisions/ireland_bop_decisions.txt`.
- BOP event references `slopx_ireland_focus.19` through `.29` resolve in `events/ireland_focus_tree_events.txt`.
- Dynamic modifier and idea icons resolve through interface sprites and texture files.

## Starting Military, Technology, Industry, Supply, And Production Issues

- No owned-surface blocker found.
- `history/countries/IRE - Ireland.txt` uses vanilla `IRE_1936` and `IRE_1939` OOBs; both exist in the vanilla install.
- Starting technologies, convoys, and 1939 tech/doctrine additions are present.
- This audit did not rebalance division count, stockpiles, production lines, or live supply performance; it only checked country package references and map coherence in the owned surfaces.

## AI And Playability Issues

- No broken AI tag or focus-id references found after full focus-id parsing.
- AI strategies cover Ireland route flags, British reactions, German/Italian/Soviet/US/Spanish reactions, Northern Ireland reactions, and BOP recovery/pressure behavior.
- `NIR` is a valid vanilla tag and has vanilla character/history support, so the Northern Ireland AI strategies are not invalid tag references.
- Playability risk remains design-level: AI strategy weights were checked for reference integrity, not for campaign balance.

## Changed Files

- `common/ideas/ireland_focus_tree_ideas.txt`
- `docs/plans/ireland_focus_tree/subagent_handoffs/country_package_audit_2026-07-08.md`

## Changed Identifiers

- No country tags, state ids, leaders, parties, focus tree ids, localisation keys, BOP ids, achievement ids, or formable ids changed.
- Idea picture token references changed:
  - `ireland_shadow_of_civil_war`: `GFX_idea_ireland_shadow_of_civil_war` -> `ireland_shadow_of_civil_war`
  - `ireland_economic_war_strain`: `GFX_idea_ireland_economic_war_strain` -> `ireland_economic_war_strain`
  - `ireland_treaty_ports_in_foreign_hands`: `GFX_idea_ireland_treaty_ports` -> `ireland_treaty_ports`
  - `ireland_small_army_long_coast`: `GFX_idea_ireland_small_army_long_coast` -> `ireland_small_army_long_coast`
  - `ireland_divided_island`: `GFX_idea_ireland_divided_island` -> `ireland_divided_island`
  - `ireland_trade_dependence`: `GFX_idea_ireland_trade_dependence` -> `ireland_trade_dependence`
  - `ireland_emergency_powers`: `GFX_idea_ireland_emergency_powers` -> `ireland_emergency_powers`
  - `ireland_constitutional_authority_ledger`: `GFX_idea_ireland_authority` -> `ireland_authority`
  - `ireland_partition_pressure_ledger`: `GFX_idea_ireland_partition_pressure` -> `ireland_partition_pressure`
  - `ireland_foreign_access_ledger`: `GFX_idea_ireland_foreign_access` -> `ireland_foreign_access`

## Before And After Behavior

- Before: Ireland ideas would ask the engine for `GFX_idea_GFX_idea_ireland_*` sprite names and could display missing idea icons despite valid sprite definitions existing.
- After: Ireland ideas ask for unprefixed picture tokens, resolving to existing `GFX_idea_ireland_*` sprites in `interface/ireland_focus_tree.gfx`.

## Validation Evidence

- Offline wiki and vanilla documentation were consulted for country setup, focuses, ideas, decisions, events, localisation, scopes, triggers, effects, modifiers, on actions, AI, and BOP behavior.
- Vanilla precedents checked:
  - `history/countries/IRE - Ireland.txt`
  - `common/characters/IRE.txt`
  - `common/country_tags/00_countries.txt`
  - `history/units/IRE_1936.txt`
  - `history/units/IRE_1939.txt`
  - vanilla BOP side icon dimensions from `gfx/interface/bop/*.dds`
- Mechanical checks run:
  - 44 registered Ireland achievements all have complete `normal`, `grey`, and `not_eligible` DDS triplets.
  - Registered achievement DDS files are `64x64`.
  - All idea `picture` tokens now resolve to defined `GFX_idea_*` sprites and existing DDS textures.
  - Ireland idea DDS textures checked at `64x64`.
  - All 16 BOP icon sprites referenced by `common/bop/ireland_balance_of_power.txt` resolve to interface sprites and existing `72x88` DDS textures, matching vanilla BOP side icon size.
  - `IRE_ALL_ISLAND` normal flags checked at `82x52`, medium at `41x26`, and small at `10x7`; all checked files are 32-bit TGA and not top-origin.
  - 1939 precompleted focuses in Ireland history all resolve to focus ids.
  - AI strategy `has_completed_focus = irl_*` references all resolve to focus ids.
  - AI strategy tags `ENG`, `GER`, `IRE`, `ITA`, `NIR`, `SOV`, `SPR`, and `USA` resolve in vanilla country tags.
  - `IRE_state_authority_bop` exists once in `common/bop`.
  - `ireland_state_authority_bop_category` exists in `common/decisions/ireland_bop_decisions.txt`.
  - BOP event ids `slopx_ireland_focus.19` through `.29` exist.

## Skipped Meaningful Validation

- No live game load or in-game UI inspection was run in this subagent pass.
- No art quality judgement was made from rendered contact sheets in this country-package audit. The audit checked asset existence, dimensions, and wiring only.
- No commit was created because the Ireland feature package is currently largely untracked/dirty from other worktree activity; committing the untracked idea file would include broader work not authored by this pass.

## Remaining Setup Or Identity Risks

- The 9 extra achievement icon triplets should be reconciled with achievement registration or explicitly marked as queued/superseded in the parent implementation.
- Focus-tree loading currently keys on `tag = IRE`; parent should confirm whether this is intentionally limited to playable Ireland rather than `original_tag = IRE` clones.
- Balance was not campaign-tested. AI weights, starting penalties, BOP swings, and 1939 progression need parent-level playability validation.
- Real leader and flag constraints are satisfied for owned country setup surfaces based on vanilla references and the existing asset handoff. This audit did not independently source-audit every symbolic generated icon.
