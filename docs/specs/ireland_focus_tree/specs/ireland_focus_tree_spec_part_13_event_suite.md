# Ireland focus tree spec part 13, event suite

## Canonical ruling

Events are required content for the Ireland package. They are required presentation and gameplay content. The focus tree, decision systems, BOP, Northern settlement, hidden paths, diplomacy, and country package changes should all be connected through events.

The earlier package wording that made events sound conditional is superseded. The implementation should use events as one of the main ways HOI4 tells the player that a political route, mission outcome, foreign reaction, BOP crisis, or settlement stage has changed the campaign.

Player facing event titles, descriptions, option text, news prose, report prose, quotes, slogans, and audio remain direction only in this planning package. Working labels are internal handles. Final event localisation belongs to implementation and source dependent wording belongs to the text and audio research workflow.

## Event density target

The implemented feature should be event heavy. The exact final count is an implementation decision, but the design target is large enough that the tree does not feel quiet.

Recommended minimum event package:

| Event surface | Minimum design target | Purpose |
| --- | --- | --- |
| visible country events | 65 or more | route decisions, mission results, internal crises, BOP overreach, advisor and leader transitions |
| news events | 14 or more | public route capstones, formation, compact, major Northern settlement, dangerous authoritarian or underground turns |
| report events | 12 or more | Emergency, coastwatch, G2, safehouse, port, integration, cultural, and hidden route documentary moments |
| hidden runtime events | 20 or more | setup, AI route nudges, invalid target cleanup, delayed follow ups, achievement state checks |
| foreign reaction events | 20 or more across actors | British, unionist, German, Italian, Spanish, American, Soviet, and Vatican channel reactions |
| flavour events | 140 to 190 or merged dynamic equivalents | ordinary historical texture with real mechanics, state targets, BOP hooks, missions, and cleanup |

These targets should not produce event spam. The events should be gated by focus completion, missions, BOP thresholds, route flags, state targets, foreign actor validity, curated flavour pools, active caps, and cooldowns.

## Namespace and file family direction

Use a stable Ireland event namespace. Suggested namespace: `slopx_ireland_focus`.

Recommended split:

- country events for Ireland route and mission outcomes
- hidden events for setup, delayed consequences, cleanup, and AI only routing
- news events for public international consequences
- report events for documentary style Emergency, G2, coastwatch, Northern integration, and hidden path moments

The implementation may use one file or several files, but every event should remain traceable from focus, decision, mission, BOP mode, or route family.

## Opening constitutional trunk events

The opening trunk should teach the player that Ireland has institutions, unresolved armed pressure, Northern pressure, foreign access pressure, and a choice over what kind of neutrality or state authority will exist.

Required event roles:

| Working event handle | Trigger | Visible direction | Gameplay role |
| --- | --- | --- | --- |
| `opening_dail_mandate` | first constitutional trunk focus | Dáil and cabinet authority, no final speech text | initializes Constitutional Authority and BOP education |
| `constitution_public_authority` | constitution focus or trunk milestone | legal state building and public sovereignty direction | raises legal authority and enables route convention decisions |
| `presidency_and_public_symbol` | presidency or civic symbol focus | civic office and public continuity | enables cultural route seeds and sourced portrait needs |
| `civil_war_memory_returns` | low authority or armed pressure rise | unresolved civil conflict memory, no cheap drama | opens public order and reconciliation paths |
| `first_public_order_test` | armed pressure or BOP contested center | street pressure and state response direction | player chooses reconciliation, policing, or restraint tools |
| `route_convention_opens` | trunk fork | public route decision direction | opens political route events and locks invalid branches after choice |
| `first_northern_question_hearing` | Partition Pressure unlocked | Dáil hearing and border concern direction | opens Northern settlement mission family |

## Historical sovereign neutrality and Emergency events

Historical neutrality should be event rich. The route should not play as passive waiting. Events should give the player public evidence of ports, coast watching, G2, LDF, Emergency powers, supply shortages, internment, and foreign pressure.

Required event roles:

| Working event handle | Trigger | Visible direction | Gameplay role |
| --- | --- | --- | --- |
| `ports_handover_public_relief` | Treaty Ports recovery focus or decision | sovereignty and port transfer direction | removes or transforms treaty port weakness and starts port defence missions |
| `treaty_ports_military_assessment` | port defence mission starts | practical defence assessment | lets player choose batteries, naval patrol, or port repair priority |
| `emergency_powers_debate` | Emergency route focus or war pressure | public safety and constitutional strain | moves Emergency Preparedness and BOP toward cabinet or apparatus |
| `coastwatch_service_expands` | LOP mission chain | coastal observation and civil defence | unlocks coast watch missions and report image |
| `neutral_ship_incident` | war nearby and foreign access pressure | shipping danger and neutrality under strain | tests convoys, relations, and neutrality stance |
| `internment_policy_dispute` | security mission or foreign actor intrusion | detention policy and legal unease | moves BOP, authority, and foreign trust |
| `g2_counter_espionage_report` | courier or spy threshold | intelligence success or incomplete lead | opens G2 missions and IRA foreign contact exposure |
| `ldf_public_mobilisation` | LDF focus or mission | local defence and training pressure | raises readiness with equipment and manpower costs |
| `neutrality_survives_first_test` | major foreign pressure resisted | public confidence and continued danger | route reward through decisions and ideas, not flat stability only |
| `emergency_powers_sunset_review` | postwar or low threat recovery | return to civilian normality | blocks permanent directorate unless hidden route active |

## Constitutional opposition and guarded Commonwealth cooperation events

This route needs events that separate Fine Gael legal opposition from Blueshirt street politics. Cooperation with Britain should feel useful and costly, never a free sovereignty shortcut.

Required event roles:

| Working event handle | Trigger | Visible direction | Gameplay role |
| --- | --- | --- | --- |
| `opposition_front_built` | opposition opener | legal opposition and cabinet change direction | changes route AI and opens parliamentary review decisions |
| `guarded_london_channel` | cooperation focus | careful diplomatic channel | unlocks bounded British liaison without ceding bases |
| `commonwealth_liaison_offer` | liaison decision | defence cooperation under public scrutiny | can raise readiness and Foreign Access Pressure |
| `defence_consultation_backlash` | high liaison pressure | sovereignty concern and opposition splits | forces BOP choice between review and liaison cabinet |
| `unionist_reassurance_attempt` | Northern legal settlement path | reassurance and guarantees direction | lowers unionist alarm if authority and Britain trust are valid |
| `parliamentary_review_asserts_sovereignty` | review focus or BOP recovery | legal review as a check on dependency | reduces Foreign Access Pressure and blocks puppet drift |
| `british_base_request_rejected_or_limited` | Britain pressure | hard choice on port or air access | decision outcome changes foreign trust, readiness, and dependency |
| `opposition_settlement_conference` | Northern settlement stage | legal settlement and observer direction | opens peaceful Northern path or partial concession |

## Labour and social republic events

Labour events should show democratic socialist state building, union pressure, cooperative industry, anti fascist defence, church and social pressure, and a radical congress risk. Labour must not collapse into a Soviet route by default.

Required event roles:

| Working event handle | Trigger | Visible direction | Gameplay role |
| --- | --- | --- | --- |
| `labour_conference_mandate` | Labour route opener | democratic labour mandate | changes ruling politics and starts reform missions |
| `trade_union_pressure_rises` | strike or reform mission | organized labour demands | moves BOP toward Dáil Labour or workers congress |
| `church_and_labour_tension` | social policy focus | religious and social concern direction | affects legitimacy and route diplomacy without caricature |
| `cooperative_industry_program` | industry link focus | cooperative works and production | unlocks geographically grounded construction missions |
| `worker_defence_regularisation` | military link focus | worker defence under state law | creates route units through decisions with equipment costs |
| `anti_fascist_veteran_question` | anti fascist branch | veterans, Spain memory, and route caution | unlocks advisors or volunteer memory only if sourced and valid |
| `soviet_liaison_warning` | Soviet pressure threshold | foreign aid pressure and dependency warning | moves Foreign Access Pressure and BOP through decision choice |
| `cross_border_labour_contacts` | Northern Labour route | worker networks across border | opens Labour settlement missions and British reaction |
| `workers_congress_overreach` | BOP congress high or extreme | reform body exceeds parliamentary control | triggers crisis or recovery decisions |
| `labour_constitutional_capstone` | Labour democratic capstone | social republic under law | locks democratic Labour payoff and blocks client route |

## Blueshirt corporatist events

Blueshirt events should be explicit about authoritarian risk and internal split. They should not glorify real extremist symbols. The non O'Duffy corporate chamber hidden route must remain separate from guard capture.

Required event roles:

| Working event handle | Trigger | Visible direction | Gameplay role |
| --- | --- | --- | --- |
| `right_unity_council` | corporatist opener | conservative and corporatist coordination | locks route and opens chamber or guard choices |
| `uniformed_march_crisis` | armed pressure or guard focus | paramilitary pressure and public order | moves BOP and triggers Labour and republican backlash |
| `corporate_chamber_proposal` | chamber focus | institutional corporatism direction | opens chamber decisions and avoids O'Duffy hard route if moderated |
| `oduffy_confidence_test` | leader focus or guard pressure | leader authority test | can hard lock guard route or split movement |
| `spanish_connection_returns` | foreign right branch | foreign veteran and anti communist memory direction | unlocks foreign sponsor risk and anti communist missions |
| `italian_contact_alarm` | Italy pressure | right wing foreign contact unease | raises Foreign Access Pressure and democratic backlash |
| `labour_resistance_to_corporate_state` | corporate repression or Labour opposition | strikes and resistance direction | starts missions with costs and failure states |
| `guard_overreach_event` | guard high or extreme BOP | movement capture risk | triggers crisis, coup, or chamber recovery route |
| `corporate_chambers_without_chief` | hidden route reveal | institutional survival after leader crisis | opens hidden chamber route and blocks guard excess |
| `corporate_route_foreign_reaction` | capstone | foreign reaction to authoritarian Ireland | news event and diplomacy consequences |

## IRA underground republic events

IRA events must treat foreign contact and Plan Kathleen style content as unstable. German contact should create exposure, dependency, and British reaction, not a clean power route.

Required event roles:

| Working event handle | Trigger | Visible direction | Gameplay role |
| --- | --- | --- | --- |
| `safehouse_network_revealed` | IRA pressure or G2 miss | clandestine infrastructure direction | opens safehouse missions and public order response |
| `arms_cache_dispute` | arms decision or raid | weapons and state authority conflict | shifts BOP and equipment pools |
| `army_council_demands_voice` | IRA route focus | military command pressure | moves BOP toward Army Council |
| `civilian_front_attempts_control` | absorption or reconciliation route | political front tries to contain armed command | opens safer republican settlement path |
| `courier_contact_arrives` | German probe threshold | foreign courier risk direction | raises Foreign Access Pressure and exposure mission |
| `plan_kathleen_style_exposure` | courier failed or G2 success | compromised invasion planning risk | creates British reaction and state crisis |
| `german_contact_dependency_crisis` | German access accepted | dependency and counter intelligence danger | can break route, puppet risk, or unlock emergency crackdown |
| `border_cell_action` | border mission or uprising path | local armed action and civilian cost | changes Partition Pressure and unionist alarm |
| `uprising_deadline_warning` | hard route timer | action deadline and risk | starts mission with success, failure, and partial success |
| `state_absorbs_or_crushes_network` | absorption or crackdown result | state authority over underground | transforms idea and closes unsafe decisions |
| `compromised_network_collapse` | dependency extreme or failure | route failure and exposure | triggers cleanup and recovery events |

## Industry and supply events

Industry events should keep economic branches grounded in Irish state building. They should not be silent factory rewards.

Required event roles include Shannon grid program, sugar beet board expansion, turf fuel drive, native manufactures debate, port repair contracts, rail and depot survey, rationing and supply trust, and industrial self sufficiency capstone. Each event should connect to named construction missions, state targets, resource decisions, supply or readiness values, and trade dependence.

## Military and Emergency defence events

Military events should make the small army and long coast problem visible. Required event roles include army exercise public review, coastal battery plan, Look Out Posts network complete, LDF training problem, Air Corps warning gap, naval patrol shortage, border drill incident, G2 security success, and Emergency defence capstone.

These events should create decisions, unit pathway changes, command appointments, mission success, mission failure, or idea transformations. Repeated free division rewards are blocked.

## Diplomacy and foreign access events

Foreign events should make neutrality active. Britain, Germany, Italy, Spain, United States, Soviet Union, and Vatican channel content should react to Irish route choices, foreign access pressure, BOP mode, war state, and Northern settlement.

Required event roles include Britain pressure note, Germany access probe, Italy and Spain contact, United States observer question, Soviet mission offer, Vatican channel debate, foreign access threshold warning, neutral conference invitation, Atlantic compact conference, and sponsor dependency backlash.

The Vatican channel remains route relevant only where implementation has a serious diplomatic or social policy surface. It should not become generic blessing flavour.

## Northern settlement and integration events

Northern events are mandatory. The Northern route is not a claim ladder. Events should show British response, unionist alarm, observer legitimacy, settlement negotiation, border incidents, local integration, and possible failure.

Required event roles:

| Working event handle | Trigger | Visible direction | Gameplay role |
| --- | --- | --- | --- |
| `northern_offer_announced` | settlement branch opener | public offer and legal claim direction | starts British and unionist response chain |
| `unionist_council_alarm` | Partition Pressure or coercive move | local unionist concern and resistance | raises alarm and modifies integration conditions |
| `british_cabinet_response` | settlement request | British war state and trust dependent reaction | opens concession, refusal, protectorate, or pressure path |
| `observer_mission_deployed` | peaceful path mission | observers and guarantee direction | creates mission and reduces legitimacy cost if successful |
| `border_security_incident` | armed route or failed mission | local violence and pressure | can redirect to emergency, crackdown, or de escalation |
| `plebiscite_preparation_dispute` | plebiscite path | franchise, safeguards, and local institutions | starts timed objective with failure path |
| `cross_border_labour_mediation` | Labour route | worker and trade union mediation | opens Labour settlement route if dependency is low |
| `common_platform_talks` | hidden civic route | guarantees and civic compromise direction | opens hidden settlement route and disqualifies coercive path |
| `protectorate_emergency_claim` | Britain weak and emergency route | temporary protectorate claim under crisis | requires handback, settlement, or failure outcome |
| `settlement_vote_or_agreement` | mission success | public legal settlement direction | prepares decision verified identity change |
| `integration_commission_begins` | formation or settlement | local administration and guarantee work | starts integration missions |
| `integration_backlash` | failed integration or high alarm | local backlash and state strain | creates penalties and recovery route |
| `all_island_identity_news` | verified formation | international public event direction | news event and diplomatic reactions |

## Hidden path events

Hidden paths need events for reveal, acceptance, overreach, failure, and cleanup. They should not be invisible modifiers. The player should see why civic cultural restoration, Emergency Directorate, Atlantic compact, common platform settlement, corrupted restoration failure, compromised republican network, and route specific overlays matter.

Civic cultural restoration events must stay civic, constitutional, educational, and inclusive. They must not drift into high kingship fantasy, occult content, or forced cultural policy.

Emergency Directorate events must show survival pressure and restoration deadlines. They must not be a clean authoritarian reward.

Corrupted restoration failure events should catch extremist capture, coercive cultural policy, foreign dependency, armed route contamination, or fantasy abuse and turn it into a failure and recovery system.

## BOP threshold events

Every active BOP mode needs events for center contest, high pressure, extreme pressure, overreach, and recovery. The event should not repeat the BOP value. It should show which institution is acting and what decision or mission follows.

Required BOP event roles include opening contested center, constitutional overcentralisation, armed pressure extreme, emergency apparatus overreach, liaison cabinet dependency, workers congress pressure, Blueshirt guard state capture, Army Council state capture, civic cultural capture, security directorate permanent rule, and BOP recovery settlement.

## Formable, late game, and public news events

Unified Ireland, route specific all island identities, Atlantic compact, Labour all island route, corporate state, revolutionary republic, and neutral postwar arbitration need public events. The formation event should fire after the decision verifies state control or settlement conditions. A focus should prepare identity and legitimacy, not grant the formable alone.

Late game events should show what the country becomes through actual route play. They should not be reward dumps or generic victory messages.

## AI runtime and cleanup events

Hidden events must support AI and cleanup. They should handle route rebalance, invalid Britain response, invalid foreign sponsor, invalid Northern actor, BOP mode cleanup, active mission cleanup, tag switch cleanup, annexation cleanup, and achievement state audits.

AI hidden events must not create content for invalid routes. They should check state control, sponsor existence, ideology, war state, BOP mode, route flags, foreign access pressure, and Northern settlement stage.

## Localisation handoff direction

Event localisation should be written as final in world text during implementation. This spec gives direction only. Event text should explain visible public action, actor choices, mission results, and consequence direction without exposing hidden variables or future secret branches.

Do not write final quotes, slogans, Gaelic wording, movement phrases, lyrics, prayers, cultural remarks, or audio selections without research. Working event handles are not titles.

## Acceptance rules

- Events are implemented for every major route, support branch, hidden path, BOP mode, Northern settlement stage, and formation outcome.
- Events trigger decisions, missions, idea lifecycle changes, BOP movement, foreign reactions, AI behavior, assets, or cleanup.
- News and report events exist for public and documentary milestones.
- Every route capstone or crisis event has AI chance and invalid route blockers.
- Every event family has cleanup for tag switch, route failure, invalid foreign actor, settlement completion, or country invalidation.
- Event assets and text research gates are included in prompts and matrices.
- The implementation report includes an event coverage table.


## Canonical flavour event dependency

Part 19 and part 20 are required. The event suite must include the large flavour event layer as implementation content. The flavour layer covers ordinary historical life through schools, radio, rationing, coast posts, merchant shipping, parish halls, county councils, creameries, sugar beet, turf, Red Cross relief, LDF drill, border markets, political offices, hidden path warning signs, and postwar memory.

Flavour events must not be passive popups. They must alter Constitutional Authority, Emergency Preparedness, Partition Pressure, Foreign Access Pressure, BOP, local support, integration progress, compact cohesion, route pressure, decisions, missions, AI behavior, idea stages, or cleanup.

The implementation report must map every row in `matrices/ireland_focus_tree_flavour_event_catalogue_matrix.md` to a final event id, dynamic event variant, queued row with reason, or rejected row with reason.
