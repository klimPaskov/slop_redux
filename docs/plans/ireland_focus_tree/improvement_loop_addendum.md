# Ireland Focus Tree Improvement Loop Addendum

Date: 2026-07-08

## Disposition

Write an improvement addendum, not a closure handoff.

The implemented Ireland focus tree is a large, route-complete tranche rather than a small fallback. It has 238 focuses, the four pressure mechanics, decision categories, hidden path focus groups for civic restoration, Emergency directorate, Atlantic compact, common platform settlement, generated UI assets, achievements, and documentation. It still does not meet closure quality because several accepted hidden overlays are represented as flags or single missions rather than complete revealable subpaths, the AI package is narrower than the canonical matrix, and player-facing localisation still contains placeholder-style descriptions and tooltips.

No prior addendum exists under `docs/plans/ireland_focus_tree/`. The earlier blocker note under `docs/specs/ireland_focus_tree/plans/ireland_focus_tree_improvement_loop_blocker.md` is process-only and is resolved by this pass. This addendum remains unresolved until the parent either implements it, folds it into the source specs, queues it with a reason, or rejects it with a reason.

## Files Inspected

- Canonical package: `docs/specs/ireland_focus_tree/README.md`, `ireland_focus_tree_planning_state.md`, all spec parts under `docs/specs/ireland_focus_tree/specs/`, all matrices under `docs/specs/ireland_focus_tree/matrices/`, prompt `docs/specs/ireland_focus_tree/prompts/ireland_focus_tree_improvement_loop_prompt.md`, research notes and bibliographies under `docs/specs/ireland_focus_tree/research/`, readiness report, and the prior blocker note.
- Implementation: `common/national_focus/ireland_focus_tree.txt`, `common/decisions/ireland_focus_tree_decisions.txt`, `common/scripted_effects/slopx_ireland_effects.txt`, `common/scripted_triggers/slopx_ireland_triggers.txt`, `common/ideas/ireland_focus_tree_ideas.txt`, `common/dynamic_modifiers/ireland_focus_tree_dynamic_modifiers.txt`, `common/ai_strategy/ireland_focus_tree_ai_strategy.txt`, `common/achievements/ireland_focus_tree_achievements.txt`, `interface/ireland_focus_tree.gfx`, `localisation/english/slop_redux_l_english.yml`, `docs/ireland_focus_tree.md`, and `docs/assets/ireland_focus_tree/manifest.md`.
- Additional setup evidence: `history/countries/IRE - Ireland.txt` initializes Ireland mechanics. `common/script_constants/ireland_focus_tree_constants.txt` holds Ireland tuning constants.

## Research Basis

The accepted design is grounded in the source package research:

- 1937 Constitution, presidency, language status, and Dail legitimacy anchor the constitutional trunk and civic cultural hidden path.
- 1938 Treaty Port settlement and Emergency defence records anchor the port, coastwatching, G2, LDF, and active neutrality mechanics.
- O'Duffy, Blueshirts, Spain, Italy, and Catholic corporatism anchor a route-locked radical right path separate from Fine Gael legal opposition.
- William Norton, trade union politics, cooperative economics, and anti-fascist volunteer memory anchor Labour as democratic socialism with radical pressure, not only Soviet alignment.
- IRA, S-Plan, Hermann Goertz, and Plan Kathleen material anchor German contact as exposure and dependency risk.
- Boundary Commission memory, Northern unionist reaction, local support, observer missions, safeguards, and integration stages anchor the Northern settlement as more than a claim ladder.
- Hidden civic restoration uses language, Gaelic League, Douglas Hyde, education, Gaeltacht, and presidency anchors. It must remain civic and constitutional, not crown or high-kingship fantasy.

## Route Families Checked

| Route family | Implementation evidence | Gap | Parent action |
| --- | --- | --- | --- |
| Opening state-building trunk | Implemented from `irl_audit_free_state` through `irl_support_lanes_open`; mechanics initialize from country history and scripted effects. | Opening is structurally present. Localisation is broad and repetitive. | Replace generic focus descriptions with route-specific player text that explains current state and choice consequences. |
| Historical sovereign neutrality | Implemented through constitution, presidency, Treaty Ports, Emergency oversight, G2, coastwatching, Plan W, strict neutrality, postwar legal claim, and de Valera capstone. | Route is deep enough mechanically. It needs final text polish and AI checks for active neutrality under changing war states. | Keep route. Add AI validation notes for when neutrality should delay Northern action or resist sponsor pressure. |
| Fine Gael constitutional opposition | Implemented with Cosgrave legal government, Blueshirt split, Commonwealth channel, guarded defence cooperation, treaty review, Allied association, Atlantic guarantee, and settlement. | Good separation from Blueshirts. Hidden constitutional backchannel is mostly represented by flags and achievement hooks, not a revealable overlay loop. | Add a small hidden backchannel package with 2 to 3 decisions or missions for document review, liaison caps, and concession testing. |
| Labour and social republic | Implemented through Norton, unions, cooperatives, welfare, anti-fascist volunteer liaison, worker defence, social republic, radical alignment choice, and cross-border networks. | Labour route exists and stays democratic-socialist by default. Hidden Labour independent front is underdeveloped beyond focuses and one cross-border council decision. | Add Labour hidden overlay missions for worker defence under law, anti-fascist service board, cooperative supply front, and democratic return check if radical pressure rises. |
| Blueshirt corporatist | Implemented with National Guard, optional O'Duffy return, corporate chambers, Catholic social order, union discipline, Spain and Rome/Burgos channels, anti-communist front, Dail pressure, corporate state, and Northern escalation. | Core route is present. Corporate chambers without O'Duffy is only an optional path flag and achievement condition. | Add a short institutional crisis package: Guard leader crisis, chamber-state consolidation, and sponsor containment. Do not create a separate Fine Gael fascist route. |
| IRA underground | Implemented with S-Plan cells, safehouses, border columns, absorption option, Army Council path, sabotage, German courier, Plan Kathleen, smuggling, British pressure, Ulster operation, dependency break, and capstone. | Core risk is present. Compromised republican network and republican reconciliation backchannel are mostly flags plus cleanup decisions. | Add exposure-stage missions and failure states: safehouse audit, courier exposure, arms surrender, border cells stand-down, and Army Council crisis if reconciliation fails. |
| Industry and supply | Implemented with tariff repair, native manufactures, small arms, Shannon power, sugar beet, turf, ports, docks, fisheries, rural works, rail, stores, rationing, and capstones. | Good route breadth. Some descriptions are generic and do not distinguish project outcomes. | Localisation pass only unless balance audit finds project reward problems. |
| Military and Emergency | Implemented with army review, training, LSF/LDF, coastwatching, radio posts, port commands, Air Corps, naval service, G2, internee camps, route reserves, defence state, invasion response, and Emergency hidden directorate. | Mechanic breadth is good. Emergency directorate has a real focus group but needs clearer failure and restoration mission text. | Keep scope. Improve route crisis decision descriptions and AI weights for civilian restoration versus permanent security state. |
| Diplomacy and neutrality | Implemented with League voice, neutrality declaration, London, Washington, Vatican, belligerent incident board, British/German pressure, Rome/Burgos, Moscow, Allied association, access audit, balanced sponsors, Atlantic observers, neutrality capstone, and compact. | Broad route is present. Foreign actor AI is too thin for the canonical sponsor matrix. | Add AI strategy profiles or scripted blockers for Germany, Italy, Spain, United States, Soviet Union, Vatican, and sponsor invalidation cleanup. |
| Northern settlement | Implemented with survey, Six Counties problem, nationalist committees, unionist alarm, Boundary Commission, arbitration, plebiscite, observers, cross-border economic zone, frontier defence, route-specific pressure, British response, negotiation table, opportunity clause, state control decision, office, Belfast industry, safeguards, integration, and all-island administration. | This is not a simple focus claim ladder, but it still hardcodes state `119` in settlement checks and has limited foreign and unionist actor AI. | Add a state-target verification note or scripted trigger review. Expand British and Northern actor reactions. Keep unified Ireland as the only identity change. |
| Late game and formable guardrails | Implemented with neutral conference, Emergency lessons, route capstones, unified stabilisation, capital question, Shannon to Belfast, and second-stage guardrail. | Formable scope is correctly restrained. | No new formable. Use validation only. |

## Hidden Paths Checked

| Hidden path or overlay | Current implementation | Gap | Required action |
| --- | --- | --- | --- |
| Civic cultural restoration | Focus group from `irl_hidden_cultural_reveal_gate` through `irl_civic_restoration_capstone`; reveal gated by authority and low foreign access; no crown content. | Strong enough structurally. Needs final text and tooltip polish. | Keep. Do not add monarchy, high kingship, or unsourced slogans. |
| Emergency directorate | Focus group from `irl_emergency_directorate_warning` through civilian restoration or permanent security state; crisis decisions exist. | Good skeleton. AI and failure text need refinement. | Add AI conditions for rare crisis use and clearer recovery or permanent-state consequences. |
| Atlantic neutral compact | Focus group through conference, observers, arbitration, no-basing, member rules, and compact capstone; decision `ireland_call_atlantic_neutral_conference`. | Correctly remains a compact or conference, not a formable. Sponsor and member AI is underdeveloped. | Add acceptance or refusal behavior for likely neutral participants and major power reactions. |
| Common platform Northern settlement | Focus and mission support through observer preparation, `ireland_common_platform_table_mission`, and all-island proclamation path. | Present but thin for a hidden Northern route. | Add local support, unionist alarm, and minority-safeguard checks to make success more than a reveal flag. |
| Corrupted restoration failure | Triggered by `slopx_ireland_trigger_corrupted_restoration_failure` when foreign access is in crisis during cultural guardrail. | Functional guardrail exists. It needs recovery or blocked-route messaging. | Add a recovery or lockout decision so players understand the failure state. |
| Compromised republican network | Flags from safehouses/courier focus and G2 cleanup decision. | Too shallow compared with accepted overlay. | Add exposure stages, safehouse losses, British/G2 reaction, and no clean elite units. |
| Cross-border Labour Council | Labour Northern focuses plus `ireland_labour_cross_border_council` decision. | Present but not a full hidden overlay. | Add legal worker defence, service board, cooperative supply, and return-to-elections missions. |
| Constitutional backchannel | `ireland_constitutional_backchannel_open` and backchannel achievement flag exist through constitutional focuses. | Too shallow as a hidden overlay. | Add document review, liaison safeguards, and concession-test missions. |
| Corporate chambers without O'Duffy | O'Duffy return is optional and chambers achievement can fire without him. | Mechanically present but lacks crisis pathway. | Add Guard leader crisis and institutional chamber-state decisions. |
| Republican reconciliation backchannel | `ireland_republican_reconciliation_backchannel` decision exists. | Single mission cannot carry the accepted overlay. | Add amnesty channel, civilian authority restoration, and border cell stand-down stages. |
| Neutral aftershock recovery | `ireland_neutral_aftershock_recovery_mission` exists. | Adequate as a recovery mission, but needs clearer invalidation rules. | Add blockers for deliberate foreign basing or Axis collaboration. |
| Northern emergency protectorate | `ireland_northern_emergency_protectorate` decision exists. | Present but needs British/Northern actor reaction and exit settlement logic. | Add temporary administration, observer corridor, policing, and exit settlement checks. |

## Mechanic Depth Checked

The four canonical mechanics exist as variables and dynamic modifier logic:

- `ireland_constitutional_authority`
- `ireland_emergency_preparedness`
- `ireland_partition_pressure`
- `ireland_foreign_access_pressure`

They are initialized in country history, clamped by `slopx_ireland_clamp_mechanics`, presented through ledger ideas and the dynamic modifier, and adjusted through route effects and decisions.

Depth gaps:

- Constitutional Authority needs more route-specific failure consequences for militia capture, Army Council dominance, Blueshirt overreach, and Emergency overuse.
- Emergency Preparedness has good focus and mission coverage. It needs AI use tied to war state and invasion danger.
- Partition Pressure is present and prevents easy settlement, but Northern local support and unionist alarm are mostly abstracted into one pressure value.
- Foreign Access Pressure is active and has no-basing and courier cleanup hooks, but sponsor-specific pressure is under-modeled for Britain, Germany, Italy, Spain, the United States, Soviet Union, and Vatican actors.

Do not add a new mechanic. Deepen the existing four through route-specific decisions, AI weights, and localisation.

## Northern Settlement Checked

The Northern settlement avoids the worst claim-ladder failure. `proclaim_all_island_settlement_decision` requires settlement preparation, control of Northern Ireland, low Partition Pressure, and sufficient authority before the all-island settlement is proclaimed. Integration then uses staged decisions for policing, service continuity, Belfast industry, unionist safeguards, failure review, and emergency protectorate.

Remaining action:

- Replace hardcoded Northern state assumptions with a documented scripted trigger review or state-group verification pass.
- Add British, unionist, Northern nationalist, and Northern labour reaction logic from the AI matrix.
- Ensure route-specific coercive paths cannot skip observers, safeguards, or integration cleanup.
- Add clear failure and recovery missions for partition crisis, emergency protectorate, and failed settlement.

## Assets Checked

The implemented asset package is wired and broad:

- Focus icons, decision icons, decision category icons, idea icons, achievement icons, and animated Emergency readiness seal are present.
- `interface/ireland_focus_tree.gfx` defines the sprite tokens used by the Ireland files.
- `docs/assets/ireland_focus_tree/manifest.md` records generated symbolic UI art, final DDS placement, and source notes.

No new asset family is required for closure. Asset follow-up is limited to verification and source-sensitive work:

- Keep generated symbolic icons for fictional or abstract surfaces.
- Continue using vanilla portraits unless the parent accepts a sourced portrait package.
- Do not add new real flags, leader portraits, slogans, Gaelic wording, audio, or attested symbols without the asset and text/audio research workflows.
- If hidden overlays are deepened, reuse existing hidden focus family icons unless a new decision icon is clearly necessary.

## Localisation Checked

Localisation exists for focuses, decisions, ideas, dynamic modifiers, achievements, and tooltips. It is not closure-ready.

Problem patterns:

- Many focus descriptions use repeated branch summaries rather than explaining each focus's specific player choice.
- Many achievement descriptions use "Complete the Ireland focus-tree objective tied to..." placeholder phrasing.
- Many custom effect tooltips expose implementation-like keys such as "Slopx Ireland Hidden Civic Focus Effect Tt" and generic "pressure values, missions, and follow-on choices adjust" phrasing.

Parent action:

- Run a focused Ireland localisation pass after gameplay addendum implementation.
- Keep text concise and player-facing.
- Avoid update-history wording.
- Do not add sourced quotes, slogans, Gaelic phrases, or audio references without the text/audio research workflow.

## AI Checked

Implemented AI strategy profiles cover:

- Historical sovereign neutrality
- Constitutional guarded Britain
- Labour democratic cooperative
- Blueshirt corporatist pressure
- IRA underground crisis
- Emergency preparedness
- British access pressure response
- British border alarm

This does not yet satisfy the canonical AI matrix. Missing or underdeveloped behavior includes Northern actors, unionist and nationalist responses, Germany courier pressure, Italy and Spain route limits, United States recognition support, Soviet pressure limits, Vatican mediation, internal actor cleanup, hidden path rarity, invalid blockers, and sponsor disappearance cleanup.

Parent action:

- Add AI strategy or scripted blockers for each canonical foreign and internal actor where the implementation surface exists.
- Keep historical AI safe and defensive.
- Keep hidden route AI rare.
- Prevent AI from collecting incompatible route rewards after ideology, sponsor, settlement, or target invalidation.

## Achievements Checked

Achievements are implemented widely and have corresponding DDS variants. The gap is not icon coverage. It is condition specificity and localisation polish.

Parent action:

- Review achievement `happened` triggers for route disqualifiers, dependency checks, hidden path proof, and settlement proof.
- Replace placeholder achievement descriptions with final player-facing objectives.
- Preserve existing achievement IDs where possible.

## What Should Not Be Added

- Do not add another ordinary political route.
- Do not add a church government route.
- Do not make the Atlantic compact a formable country.
- Do not turn civic restoration into monarchy, high kingship, or fantasy cultural content.
- Do not add a new scripted GUI unless the Emergency board is explicitly accepted after mechanics and localisation are cleaned up.
- Do not add new country tags for Northern actors unless the parent chooses that representation after state-target review.

## Implementation Surfaces For Parent Action

- `common/national_focus/ireland_focus_tree.txt`: add or refine small hidden overlay focus groups only where a single flag or mission cannot carry canonical depth.
- `common/decisions/ireland_focus_tree_decisions.txt`: add the main missing overlay missions and recovery/failure stages.
- `common/scripted_effects/slopx_ireland_effects.txt`: add overlay-specific effects only when they remove repeated logic.
- `common/scripted_triggers/slopx_ireland_triggers.txt`: add actor, state-target, dependency, and invalidation blockers.
- `common/ai_strategy/ireland_focus_tree_ai_strategy.txt`: expand the AI matrix beyond Ireland route profiles and two British responses.
- `common/achievements/ireland_focus_tree_achievements.txt`: tighten hidden route and settlement conditions.
- `localisation/english/slop_redux_l_english.yml`: replace generic focus, decision, tooltip, and achievement text.
- `docs/ireland_focus_tree.md`: update after implementation to distinguish completed hidden overlay depth from future plans.
- `docs/assets/ireland_focus_tree/manifest.md`: update only if new icons are added.

## Acceptance Criteria

The parent can move from this addendum to closure only when:

- Every accepted hidden path and route overlay is either implemented with comparable depth, merged into another implemented overlay with a clear reason, or explicitly rejected with a reason.
- Northern settlement has British and local reaction logic, state-target validation, integration failure handling, and no route can bypass settlement preparation.
- AI covers Ireland routes, Britain, relevant foreign sponsors, Northern local actors, internal actors, hidden rarity, invalid blockers, and cleanup.
- Localisation no longer contains placeholder-style achievement descriptions or implementation-key tooltips.
- Assets remain wired and documented, with no unsourced real symbols or text/audio material introduced.
- The accepted result is either promoted into `docs/specs/ireland_focus_tree/` or recorded as an implemented plan under `docs/plans/ireland_focus_tree/`.

## Promotion Note

Keep this file in `docs/plans/ireland_focus_tree/` until resolved. The canonical specs already contain most of the design. If the parent accepts the refinements above, promote only the final disposition of merged, trimmed, or rejected hidden overlays into `docs/specs/ireland_focus_tree/specs/ireland_focus_tree_spec_part_11_acceptance_handoffs.md` or a concise follow-up spec note. Do not duplicate the entire addendum into the source spec.
