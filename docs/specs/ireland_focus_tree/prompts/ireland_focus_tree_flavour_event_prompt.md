# Ireland focus tree flavour event implementation prompt

Feature slug: `ireland_focus_tree`

Implement the mandatory flavour event layer from:

- `specs/ireland_focus_tree_spec_part_19_flavour_event_layer.md`
- `specs/ireland_focus_tree_spec_part_20_flavour_event_catalogue.md`
- `specs/ireland_focus_tree_spec_part_21_flavour_event_acceptance.md`
- `matrices/ireland_focus_tree_flavour_event_catalogue_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_effect_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_asset_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_ai_cleanup_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_historical_anchor_matrix.md`
- `matrices/ireland_focus_tree_flavour_event_source_matrix.md`

These events are required gameplay coverage for ordinary political, cultural, economic, social, civil defence, local, and postwar life in Ireland. The flavour matrix contains 169 working handles or merged dynamic equivalents.

Follow `AGENTS.md`, `hoi4-events`, `hoi4-focus-trees`, `hoi4-decisions-missions`, `hoi4-feature-assets`, `hoi4-frame-animation`, `hoi4-text-audio-research`, `hoi4-improvement-loop`, and `hoi4-subagents`.

Implement event families for civic calendar, presidency, Dáil scrutiny, courts, press, radio, language, schools, GAA, church, social relief, vocational training, sugar beet, creameries, turf, rationing, Ardnacrusha, rail, ports, shipping, ARP, blackout, coast posts, fisheries, internment, crashes, Donegal access, border markets, workplace politics, guard local order, IRA families, safehouses, diplomats, diaspora, Red Cross, and postwar memory.

Every flavour event must change play. It must move a mechanic value, move BOP, start or resolve a mission, alter a decision cost, change state local support, alter idea lifecycle, consume real resources, change foreign reaction memory, alter AI weights, or perform cleanup. Do not add empty popups.

Use country events, state events, hidden events, report events, and rare news events as mapped. Use family cooldowns and state caps so flavour events feel frequent across a campaign without flooding one month.

Do not write final titles, descriptions, options, newspaper headlines, radio lines, church wording, sports slogans, diaspora letters, quotes, or cultural remarks from working labels. Use text and audio research for source dependent wording. Working labels are internal handles only.

Update the final implementation report with a table mapping each working flavour event label to a final event id, merged event id, queued row with reason, or rejected row with reason. A rejection is valid only when another implemented event preserves the historical anchor, trigger, mechanical payload, AI behavior, asset need, and cleanup role.
