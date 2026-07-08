# Ireland focus tree event implementation prompt

Feature slug: `ireland_focus_tree`

Implement the required Ireland event layer. Major events and flavour events are canonical content.

Read:

- `specs/ireland_focus_tree_spec_part_13_event_suite.md`
- `specs/ireland_focus_tree_spec_part_19_flavour_event_layer.md`
- `specs/ireland_focus_tree_spec_part_20_flavour_event_catalogue.md`
- `specs/ireland_focus_tree_spec_part_21_flavour_event_acceptance.md`
- `matrices/ireland_focus_tree_event_suite_matrix.md`
- `matrices/ireland_focus_tree_event_focus_decision_matrix.md`
- `matrices/ireland_focus_tree_event_ai_matrix.md`
- `matrices/ireland_focus_tree_event_trigger_cleanup_matrix.md`
- `matrices/ireland_focus_tree_event_asset_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_catalogue_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_effect_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_historical_anchor_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_ai_cleanup_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_asset_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_source_matrix.md`

Follow `AGENTS.md`, `hoi4-events`, `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-feature-assets`, `hoi4-frame-animation`, `hoi4-text-audio-research`, and `hoi4-subagents`.

Implement major event families for constitutional state building, Treaty Ports, Emergency neutrality, political route milestones, Northern settlement, foreign reactions, industry and supply, military defence, BOP crises, hidden path reveals, and late game unified Ireland.

Implement the full flavour event layer. It must cover rationing, household burden, turf, wheat, shipping, Coast Watching Service, LDF drill, Red Cross relief, censorship, G2, language administration, local politics, border markets, school and policing settlement, foreign legation pressure, diaspora relief, and postwar aftershocks. Use country events, state events, hidden events, report events, and rare news events as mapped.

Use weighted pools, route filters, mechanic thresholds, cooldowns, and active caps so the campaign feels rich without popup spam.

Every major route needs early, middle, late, and failure or overreach events. Every BOP extreme band needs crisis or recovery event handling. Every Northern settlement path needs local, British, unionist, observer, integration, and failure events. Every flavour event family needs gameplay effects beyond prose.

Events must change play. They should move canonical mechanics, change BOP, unlock or close decisions, start or resolve missions, alter AI strategy, create foreign responses, change idea lifecycle, create state integration work, set achievement memory, or perform cleanup. Do not fill event chains with tiny stability, political power, war support, generic equipment, or empty flavour text.

Do not write final event titles, descriptions, options, news text, report text, quotes, slogans, cultural remarks, Irish language phrases, or audio cues from working labels. Working labels are internal handles. Use text and audio research for source dependent wording.

Create final event ids, namespaces, localisation keys, event pictures, news or report image references, AI chances, trigger tooltips, decision hooks, focus hooks, mission success and failure hooks, and cleanup helpers.

Record final event coverage tables that map every working label from the major event suite and every flavour handle from the flavour matrix to a final event id, merged dynamic event, queued row with reason, or rejected row with reason. A rejection is valid only when another implemented event preserves the historical anchor, trigger, mechanical payload, AI behavior, asset need, and cleanup role.
