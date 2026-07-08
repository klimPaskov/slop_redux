# Slop Redux Ireland Focus Tree

## Overview

The Ireland tree is implemented as `slopx_ireland_focus_tree` in `common/national_focus/ireland_focus_tree.txt`. It uses the vanilla IRE tag and keeps the vanilla Irish character roster, including de Valera, O'Duffy, Larkin, Norton, Sean Lemass, Douglas Hyde, and the existing vanilla portraits.

The tree has 238 implemented focuses. It covers the opening constitutional trunk, five public political routes, industry and supply, military and Emergency defence, diplomacy and foreign access, the Northern settlement lane, late-game capstones, and revealable hidden paths.

## National Mechanics

The four visible pressure systems are initialized in `slopx_ireland_initialize_mechanics` and kept current through `slopx_ireland_update_mechanics_modifier`.

- Constitutional Authority: tracks Dail legitimacy, public order, reconciliation, emergency reach, and underground pressure.
- Emergency Preparedness: tracks stores, reserves, coastwatching, port defence, G2, and invasion response work.
- Partition Pressure: tracks unionist alarm, nationalist organisation, British response, and settlement preparation.
- Foreign Access Pressure: tracks port access, sponsor dependency, observers, couriers, and no-basing enforcement.

The values are shown through Ireland ledger ideas and the `slopx_ireland_mechanics_dynamic_modifier`. Decisions and focuses adjust the same variables, then force a dynamic modifier update.

## Route Families

- Historical sovereign neutrality: constitutional consolidation, Treaty Port recovery, neutrality credibility, Emergency oversight, and postwar legal claims.
- Fine Gael constitutional opposition: legal government, Blueshirt split, Commonwealth channels, guarded defence cooperation, and democratic Northern settlement.
- Democratic Labour: union mandate, rural cooperatives, worker industry, anti-fascist defence, and cross-border Labour organisation.
- Blueshirt corporatism: National Guard revival, optional O'Duffy return, corporate chambers, anti-communist front, and dangerous Northern escalation.
- IRA underground crisis: S-Plan cells, safehouses, border columns, German courier risk, Plan Kathleen exposure, and dependency cleanup.

## Hidden Paths

Hidden content is revealed through focus gates, decisions, and pressure thresholds rather than being visible from game start.

- Civic cultural restoration: revealed by democratic authority and low foreign access pressure. It stays a civic republican restoration and avoids crown restoration content.
- Emergency directorate: revealed by high Emergency Preparedness and weak civilian authority. It can restore civilian rule or harden into a permanent security state.
- Atlantic neutral compact: revealed through no-basing principles, neutral conference preparation, and low foreign access pressure. It is a conference and compact framework, not a formable country.
- Common platform Northern settlement: revealed through observer-backed and legitimacy-based settlement preparation.
- Corrupted restoration failure: triggered by attempting cultural restoration while foreign access pressure is in crisis.
- Compromised republican network: represented by IRA courier exposure and a G2 cleanup decision.
- Cross-border Labour Council: represented by Labour Northern network focuses and a route-crisis decision.
- Constitutional backchannel: represented by Commonwealth channel and guarded association focuses without granting bases automatically.
- Corporate chambers without O'Duffy: possible because O'Duffy's return is optional before corporate chambers.
- Republican reconciliation backchannel: represented by an amnesty/backchannel crisis decision.
- Neutral aftershock recovery: represented by a postwar recovery mission after Emergency lessons or neutrality conference work.
- Northern emergency protectorate: represented by a pre-settlement emergency protectorate decision when Ireland controls Northern Ireland, Britain is under wartime pressure, and a prepared settlement exists.

The improvement-loop follow-up added multi-step decision chains for the overlays that were initially only flags or single missions. These chains live in `ireland_foreign_access_category`, `ireland_partition_settlement_category`, `ireland_route_crisis_category`, and `ireland_post_settlement_integration_category`.

## Northern Settlement

The Northern route does not grant reunification from a focus alone. Focuses prepare legitimacy, observers, safeguards, and state-control conditions. `proclaim_all_island_settlement_decision` verifies that Ireland controls state `119`, has prepared the settlement, has a Northern agreement path, and has low enough Partition Pressure before setting the all-island provisional identity.

Integration then proceeds through staged decisions for policing, service continuity, Belfast industry, unionist safeguards, and failure review. These missions re-check control and pressure when they complete; if the conditions collapse, the settlement can fail. The state `119` core and reconciliation achievement hooks are added only when the integration stage reaches completion with safeguards intact.

## Assets

The asset wiring package lives under `docs/assets/ireland_focus_tree/` and game assets live under:

- `gfx/interface/goals/` for focus family icons.
- `gfx/interface/ideas/` for national spirits and the dynamic modifier icon.
- `gfx/interface/decisions/` and `gfx/interface/decisions/categories/` for decisions and categories.
- `gfx/achievements/` for achievement colour, grey, and not-eligible icons.
- `gfx/interface/animated/` for Emergency, Foreign Access, Northern Settlement, Hidden Reveal, and Atlantic Compact animated seal framesheets and static fallbacks.
- `gfx/flags/`, `gfx/flags/medium/`, and `gfx/flags/small/` for the vanilla-sourced `IRE_ALL_ISLAND` tricolour cosmetic tag.

The wiring file is `interface/ireland_focus_tree.gfx`. Final art must follow `hoi4-feature-assets` and `hoi4-frame-animation`; simple-shape or diagram placeholders are not accepted as final artwork.

## Future Plans

- Add event windows for major route transitions, if the design later wants narrative presentation beyond focus and decision text.
- Add a scripted GUI board for Emergency Preparedness if the broader mod adopts scripted GUI presentation patterns.
- Add researched audio or sourced quote packages only after the text and audio research workflow approves exact material.
