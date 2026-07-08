# Ireland BOP spec part 3, focus and decision integration

## Integration principles

The BOP must be wired into the existing focus tree without turning every focus into a small BOP nudge. Major political, emergency, settlement, and crisis focuses should move the BOP. Support focuses should move the BOP only when they change the governing balance in a visible way.

Decisions should move the BOP through concrete actions. Costs should use resources that match the action, such as equipment, command power, army XP, civilian capacity, manpower, local support, legitimacy, factory output, state objectives, fuel, convoys, or trains.

## Opening trunk integration

| Canonical focus group | BOP effect direction | Notes |
| --- | --- | --- |
| `irl_audit_free_state` | initialize opening BOP, mild constitutional advantage | reveal BOP tooltip and first authority missions |
| `irl_dail_holds` | move toward constitutional government | stronger if public order mission succeeds |
| `irl_constitutional_authority_choice` | branch based movement | legal reform moves constitutional, emergency reach may prepare later emergency mode, reconciliation lowers armed pressure |
| `irl_border_file_reopened` | no direct shift by default | only moves BOP if the player uses agitation or public restraint decisions |
| `irl_route_convention` | center or route leaning movement | route choice should set up mode switch but not lock instantly if prerequisites are missing |

## Historical and strict neutral integration

| Focus or decision family | BOP effect direction | Failure or overuse |
| --- | --- | --- |
| constitutional referendum family | toward civilian cabinet or constitutional government | failed legitimacy mission leaves opening BOP closer to contested center |
| Treaty Ports settlement | toward civilian cabinet if handled legally, toward emergency apparatus if militarized | British pressure can create emergency shift if preparedness is weak |
| coast watch and G2 | toward emergency apparatus in historical mode | overuse opens directorate warning |
| fair internment rules | toward civilian cabinet | weak enforcement can increase Foreign Access Pressure |
| censorship and public order orders | toward emergency apparatus | overuse lowers Constitutional Authority and Labour support |
| postwar neutrality arbitration | requires cabinet or balanced emergency band | security extreme blocks clean arbitration |

## Constitutional opposition integration

| Focus or decision family | BOP effect direction | Failure or overuse |
| --- | --- | --- |
| Cosgrave legal government | switch to Commonwealth cooperation mode with review advantage | if armed pressure is high, a Blueshirt split mission must run first |
| parliamentary restraint | toward independent parliamentary review | may reduce Emergency Preparedness if war threat is high |
| defence liaison | toward defence liaison cabinet | raises British access and dependency risk |
| anti basing clauses | toward independent review and lower Foreign Access Pressure | Britain may reduce support if war pressure is high |
| partition bargain | best in review moderate to liaison moderate | liaison extreme creates domestic backlash and invalidates strict neutral hooks |

## Labour integration

| Focus or decision family | BOP effect direction | Failure or overuse |
| --- | --- | --- |
| Labour in Dáil | switch to Labour mode with cabinet advantage | employer and church pressure missions begin |
| trade union congress | toward workers congress | production disruption if moved too far during war |
| cooperative industry | mild congress movement if worker run, cabinet movement if state board run | repeated use without supply support creates output strain |
| worker defence | toward workers congress | high armed pressure can disqualify peaceful Northern tools |
| anti fascist diplomacy | depends on sponsor choice | Soviet support raises Foreign Access Pressure and can push congress crisis through events |
| social republic capstone | requires congress high but not extreme, low client pressure | congress extreme can trigger route crisis instead |

## Blueshirt integration

| Focus or decision family | BOP effect direction | Failure or overuse |
| --- | --- | --- |
| corporate route opener | switch to Blueshirt mode near center | if opening BOP was armed high, start closer to guard side |
| chamber legality | toward parliamentary right and chambers | O'Duffy hard route becomes harder if chambers dominate |
| cadre mobilization | toward Blueshirt guard | costs equipment and legitimacy, raises Labour and republican resistance |
| Catholic corporate diplomacy | small guard or chamber movement by choice | foreign right wing pressure can make guard movement sharper |
| anti communist security | toward guard | overuse raises armed pressure and unionist alarm |
| O'Duffy commitment | requires guard high but not extreme | guard extreme can force coup crisis before focus completion |
| corporate chambers without O'Duffy | requires chambers high or guard discredited | hidden contingency route uses BOP as disqualifier for O'Duffy personal control |

## IRA integration

| Focus or decision family | BOP effect direction | Failure or overuse |
| --- | --- | --- |
| underground route opener | switch to republican underground mode | if opening BOP was constitutional high, require stronger route preparation |
| civilian front | toward civilian republican front | reconciliation route and Northern support safer |
| Army Council authority | toward Army Council | raises British pressure and G2 response |
| safehouse network | toward Army Council unless tied to civilian discipline | equipment and intelligence exposure cost required |
| foreign courier contact | no direct clean reward | creates decisions that may push Army Council and Foreign Access Pressure sharply |
| Plan Kathleen style branch | only through risky exposed content | must raise dependency, British reaction, and crisis risk |
| republican reconciliation backchannel | toward civilian front | requires high authority and low courier pressure |

## Hidden path integration

| Hidden route | BOP mode | Main BOP gate |
| --- | --- | --- |
| civic cultural restoration | civic cultural mode | civic or balanced band, high Constitutional Authority, low armed pressure |
| Emergency Directorate | Emergency Directorate mode | apparatus high or security pressure, low authority, high war pressure |
| Atlantic neutral compact | historical emergency mode | civilian or balanced band, high neutrality credibility, low sponsor dependency |
| common platform Northern settlement | current route mode | peaceful or civic leaning band, low coercion, strong local support |
| corrupted restoration failure | civic cultural mode | mobilisation extreme, low authority, high armed pressure or dependency |
| compromised republican network | republican underground mode | Army Council high or extreme and foreign courier exposure |
| cross border Labour council | Labour republic mode | congress high but not client controlled, low violence, low Soviet dependency |
| neutral aftershock recovery | historical or directorate mode | emergency failure followed by recoverable BOP band |
| Northern emergency protectorate | historical or directorate mode | emergency apparatus can support temporary protectorate only with British trust and exit plan |

## Decision families

| Decision family | BOP mode | Cost direction | Success | Failure |
| --- | --- | --- | --- | --- |
| `bop_public_confidence_session` | opening, historical, opposition | political capacity, stability floor, no active violence | moves toward legal side and lowers armed pressure | contested authority mission appears |
| `bop_reconciliation_board` | opening, historical, republican | political capacity, veteran support, local trust | moves away from armed pressure or toward civilian front | hardliners gain pressure |
| `bop_emergency_order_review` | historical, directorate | legal authority, time, emergency threat check | shifts toward civilian cabinet or restoration | weakens preparedness or enables security escalation |
| `bop_coast_security_transfer` | historical, directorate | equipment, command power, supplied port units | shifts toward emergency apparatus with preparedness gain | legitimacy hit and Labour criticism |
| `bop_anti_basing_vote` | opposition | high authority, Britain relation threshold, low invasion pressure | shifts toward independent review and lowers dependency | Britain reduces support or raises pressure |
| `bop_defence_liaison_mission` | opposition | convoys, air warning gap, British trust | shifts toward liaison and adds defence support | dependency and domestic backlash |
| `bop_congress_mandate_vote` | Labour | union support, factory disruption risk, stability floor | shifts toward workers congress and unlocks reform mission | employer resistance and authority loss |
| `bop_cabinet_discipline_vote` | Labour | party support, public trust | shifts toward Dáil Labour cabinet | worker support falls |
| `bop_guard_discipline_review` | Blueshirt | command power, legitimacy, local order | shifts toward chambers or stops guard extreme | guard splinter or republican violence |
| `bop_cadre_mobilisation` | Blueshirt | infantry equipment, manpower, command power, unrest risk | shifts toward guard and unlocks route units | Labour strike and diplomatic backlash |
| `bop_civilian_front_conference` | IRA | legitimacy, safehouse restraint, no German exposure | shifts toward civilian front | Army Council rejects restraint |
| `bop_army_council_mandate` | IRA | equipment, intelligence exposure, local support | shifts toward Army Council and unlocks hard actions | G2 crackdown or foreign compromise |
| `bop_civic_institution_drive` | cultural | civilian capacity, education or administration mission | shifts toward civic institutions | route becomes slower |
| `bop_public_cultural_mobilisation` | cultural | local support, diaspora links, low violence | shifts toward mobilisation networks | unionist alarm and corruption risk |
| `bop_civilian_rule_timetable` | directorate | war threat lower, authority recovery, public order | shifts toward restoration and closes directorate | permanent security branch opens |

## Timed mission families

BOP missions should require action, not passive waiting.

| Mission family | Objective direction | Duration band | Success effect | Failure effect |
| --- | --- | --- | --- | --- |
| `bop_keep_order_in_major_cities` | keep supplied police or army presence in Dublin, Cork, Limerick, and Galway while avoiding high repression | 90 to 120 days | constitutional side gains and armed pressure falls | armed side gains and route crisis visibility rises |
| `bop_port_security_without_bases` | guard port state group without granting foreign basing | 120 to 180 days | emergency or review side gain by route | foreign access and emergency pressure rise |
| `bop_worker_production_truce` | maintain production output while congress reforms proceed | 120 to 180 days | Labour route stabilizes near desired band | congress or employer crisis rises |
| `bop_guard_under_chain_of_command` | keep guard units supplied and subordinated while unrest stays below threshold | 90 to 150 days | chambers gain or guard pressure becomes usable | guard extreme crisis |
| `bop_safehouses_under_political_control` | keep safehouse network from exceeding exposure and violent pressure | 120 to 180 days | civilian front gain or Army Council moderated | compromised republican network risk |
| `bop_restore_civilian_rule` | lower war threat, run public order recovery, keep authority above floor | 180 days or more | restoration band reached and directorate closes | security directorate entrenchment |

## Decision clutter control

Do not add all BOP decisions into one category from game start. Use phases:

- Opening BOP decisions visible after the first trunk focus.
- Route BOP decisions visible only after route mode initializes.
- Crisis BOP decisions visible only when a band is high or extreme.
- Recovery decisions visible after failure or directorate entry.
- Hidden route BOP decisions visible only after reveal.

AI can see equivalent decisions when valid. Human UI should remain curated.

## Idea lifecycle integration

Use staged ideas, not one idea per band. Recommended idea families:

| Idea family | Role | BOP interaction |
| --- | --- | --- |
| `ire_constitutional_authority_idea` | starting state authority | tooltip reads BOP mode and band |
| `ire_emergency_powers_idea` | wartime emergency reach | strengthened by emergency bands, weakened by restoration |
| `ire_labour_mandate_idea` | Labour governing route | changes effect package by cabinet or congress band |
| `ire_corporate_order_idea` | Blueshirt and chamber route | changes route risks by chamber or guard band |
| `ire_republican_command_idea` | IRA route | changes safehouse, foreign contact, and uprising tools by front or council band |
| `ire_civic_cultural_idea` | hidden cultural route | changes integration and corruption risk by civic or mobilisation band |

Do not create seven separate ideas per BOP mode.
