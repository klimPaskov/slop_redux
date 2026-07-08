# Ireland focus tree spec part 21, flavour event acceptance handoffs

## Purpose

This file turns the flavour event layer into implementation acceptance rules. It exists because ordinary events can become filler when they lack hard hooks. Ireland must avoid that failure.

## Implementation acceptance

A final implementation must provide one of these outcomes for every row in `matrices/ireland_focus_tree_flavour_event_catalogue_matrix.md`:

| Disposition | Meaning | Required evidence |
| --- | --- | --- |
| implemented as unique event | the row has its own final event id | event id, localisation keys, trigger, effects, AI behavior, cleanup |
| implemented as dynamic variant | the row is a variant of a shared event | final event id, variant trigger, variant text keys, variant effects, variant cleanup |
| implemented through decision or mission event | the row fires from a decision or mission result | decision or mission id, event id, success and failure behavior |
| queued with reason | the row is deliberately left for a later tranche | reason, impacted route, no false completion claim |
| rejected with reason | the row was merged out or cut | reason, replacement coverage, effect loss assessment |

A row cannot be counted as implemented because a generic event exists with similar mood. It needs the historical anchor, route condition, and gameplay effect from the matrix.

## Required implementation table

The coding agent must create a final table with these columns:

| Working flavour handle | Final id or dynamic event | Trigger source | Effect package | AI behavior | Asset or sprite | Localisation keys | Cleanup | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Event code ownership

Recommended file grouping:

| File group | Contents |
| --- | --- |
| `ireland_flavour_civic_events` | constitution, councils, civil service, parish halls, public meetings |
| `ireland_flavour_media_culture_events` | radio, press, schools, language, folklore, public information |
| `ireland_flavour_emergency_homefront_events` | rationing, turf, fuel, civil defence, Red Cross, LDF |
| `ireland_flavour_ports_industry_events` | coast, merchant marine, ports, Ardnacrusha, sugar beet, transport |
| `ireland_flavour_border_events` | border markets, local safeguards, policing, schools, rail, integration |
| `ireland_flavour_route_events` | party offices, movement pressure, legal opposition, Labour, Blueshirt, IRA |
| `ireland_flavour_hidden_late_events` | hidden diagnostic events, compact texture, postwar memory, demobilisation |

The implementation can choose final filenames to match existing repository style, but it must preserve readable separation.

## Trigger ownership

Flavour events should fire from exact surfaces:

- focus completion hooks for route and industry flavour
- decision result hooks for local outcomes, supply responses, foreign contact, and customs actions
- mission success, mission failure, and mission timeout hooks for state tasks
- BOP band movement for authority conflicts
- targeted state events for Northern and local economy rows
- curated Ireland country pulses for calm domestic flavour, with cooldowns and active caps

Do not use whole world daily scans. Use Ireland scoped logic, mission hooks, focus hooks, and decision hooks.

## Localisation handoff

Every flavour event needs final player facing text written during implementation. This package provides direction only. Final text should be specific, concrete, and historically grounded. It should avoid generic lines about the government receiving reports, maps changing, committees convening, or officials issuing vague statements.

The final text should usually show a place, institution, material problem, public habit, or practical choice. It can mention schools, shop queues, fuel depots, harbour lights, parish halls, radio schedules, customs posts, county councils, barracks, creameries, rail tickets, or paperwork only when those details drive play.

The implementation must not paste working handles into localisation.

## Balance acceptance

Flavour events should be medium weight and localized. They should rarely decide an entire route alone. They should often accumulate through staged values, state mission outcomes, BOP movement, decision costs, or idea lifecycle.

A flavour event is too weak when the player can ignore it every time. A flavour event is too strong when it overrides route choices, focus rewards, major crises, or Northern settlement stages without prior setup.

## Asset acceptance

The asset prompt must include shared event image families for the flavour layer. Ordinary flavour events can reuse a shared report image family, icon, or category art when the image fits. Major public flavour outcomes can use report events. News events remain rare and public.

## Text and audio acceptance

The text and audio prompt must include research gates for culturally specific flavour, especially Irish language, folklore, political slogans, hymns, songs, proverbs, Church language, or diaspora press references. Unresearched wording remains blocked.

## Completion statement required

The final implementation report must include this statement with evidence:

`Flavour event coverage was implemented as required, with row level mapping, effects, AI behavior, assets, localisation, and cleanup recorded.`

If that cannot be said, the Ireland package is incomplete.
