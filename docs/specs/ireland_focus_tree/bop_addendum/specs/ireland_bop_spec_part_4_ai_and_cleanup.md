# Ireland BOP spec part 4, AI and cleanup

## AI design promise

AI Ireland should use the BOP as a route discipline system. It should not click the strongest side shift every time. Each route should have a desired operating band, a panic band, and a recovery plan.

## Ireland AI route bands

| AI route profile | Preferred BOP mode | Desired band | Panic band | Recovery behavior |
| --- | --- | --- | --- | --- |
| historical sovereign neutrality | historical emergency | cabinet moderate to apparatus moderate | apparatus high or cabinet extreme during war | balance emergency orders with review and coast missions |
| strict neutral watchtower | historical emergency | cabinet moderate, apparatus moderate only when war pressure is high | sponsor dependency or apparatus extreme | lower foreign access, reaffirm neutrality, recover civilian control |
| guarded Commonwealth cooperation | Commonwealth cooperation | review moderate to liaison moderate | liaison extreme or review extreme during invasion threat | use anti basing vote or defence liaison as needed |
| Labour democratic social reform | Labour republic | cabinet Labour moderate to congress moderate | congress high with Soviet dependency or cabinet extreme with worker unrest | run truce, cabinet discipline, and independent anti fascist decisions |
| Labour social republic | Labour republic | congress moderate to congress high | congress extreme and client pressure | reduce dependency and regularize worker defence |
| Blueshirt corporatist | Blueshirt corporate | chambers moderate to guard high | guard extreme or chambers extreme after route lock | discipline guard or commit to route if crisis state is accepted |
| IRA underground | republican underground | front moderate to council high by branch | council extreme with foreign exposure | purge dependency, restore civilian front, or accept hard crisis if player route allows |
| Emergency Directorate | Emergency Directorate | security moderate during war, restoration moderate after threat falls | security extreme during peace or restoration extreme during invasion | choose recovery or permanent security based on route flags and threat |
| hidden cultural restoration | civic cultural | civic moderate to mobilisation moderate | mobilisation extreme | run minority guarantees and civic institution drive |

## Foreign actor reactions

| Actor | BOP reading | Response direction |
| --- | --- | --- |
| Britain | watches armed pressure, Army Council, guard high, liaison bands, and emergency security bands | pressure Ireland when armed or foreign exposed, bargain when review or cabinet bands are credible, demand safeguards when liaison grows |
| Northern unionist actors | react to coercive domestic bands and violent pressure | alarm rises under Army Council, guard, and mobilisation extreme, local talks possible under civic and legal bands |
| Germany | seeks Army Council and high foreign access openings | offers risky tools only when Ireland is exposed or hard IRA route is valid, avoids clean aid to stable neutral Ireland |
| Italy and Spain | favor Blueshirt guard or corporate chamber route | send support only when right wing route is valid, collapse support if route softens or sponsors are defeated |
| United States | favors legal, civic, and anti dependency bands | supports observers and postwar arbitration when Ireland is not foreign captured or coercive |
| Soviet Union | favors Labour congress with anti fascist route | aid raises dependency risk, avoids actions if Labour route remains cabinet democratic or Catholic pressure is severe |
| Vatican and Catholic actors | favor legal order, anti communist right, or moral settlement depending route | adds domestic pressure in Labour congress bands, can mediate if non coercive settlement is pursued |

## Internal actor AI

| Actor | Pushes BOP toward | Pulls BOP away from | AI constraints |
| --- | --- | --- | --- |
| Emergency cabinet | emergency apparatus | civilian cabinet only after threat falls | should not force directorate unless war danger or authority crisis is real |
| G2 | emergency apparatus and security directorate | restoration after foreign cells are cleared | should prioritize Germany, IRA courier pressure, and port incidents |
| LDF | emergency apparatus when centralised | civilian cabinet when regularized | should not create free unit loops |
| constitutional opposition | independent review | defence liaison only when bargain is useful | must stay separate from Blueshirt guard route |
| Labour movement | workers congress | cabinet discipline when crisis is high | must keep democratic socialist route viable |
| Blueshirt organization | Blueshirt guard | chambers if O'Duffy discredited or guard fails | should be rare for AI unless route is explicitly chosen |
| IRA underground | Army Council | civilian front through reconciliation or political route | hard route AI must treat foreign contact as dangerous |
| Northern local groups | no direct side by default | influence through Partition Pressure and settlement missions | should modify BOP only when Dublin actions become coercive or trusted |

## Invalid route blockers

BOP actions must be hidden, bypassed, or weighted to zero when invalid.

| Invalid condition | Blocker rule |
| --- | --- |
| Ireland is annexed, tag switched away, or not controlling its capital | remove BOP and cancel BOP missions |
| route lock contradicts current BOP mode | switch mode through cleanup effect or hide old decisions |
| foreign sponsor no longer exists | remove sponsor driven BOP decisions |
| Britain no longer exists or cannot act | block liaison and British pressure BOP decisions unless replaced by a valid successor in the implementation |
| Northern Ireland or Northern state group is invalid | hide Northern BOP reactions and settlement BOP missions |
| Labour route is not active | hide workers congress decisions |
| Blueshirt route is not active | hide guard and chamber decisions |
| IRA route is not active | hide civilian front and Army Council decisions except reconciliation cleanup |
| Emergency Directorate not revealed | hide directorate mode decisions |
| hidden cultural route not revealed | hide civic cultural decisions |

## Cleanup requirements

The BOP must clean itself up through helper effects. Do not leave old side flags, old missions, old dynamic localisation state, or old AI strategy flags after a route shift.

Required cleanup moments:

- route lock focus completes
- route is abandoned, failed, or superseded
- hidden route enters or closes
- Ireland joins a faction or becomes a client state
- all island formation decision fires
- Northern settlement fails or succeeds
- war ends after Emergency Directorate route
- Ireland is annexed or loses capital
- a foreign sponsor is defeated or no longer valid

## BOP crisis events

The implementation may use hidden or visible events when a BOP extreme band is reached. Use event text direction only from the canonical package. Do not write final event prose from this addendum.

Recommended crisis families:

| Crisis family | Trigger band | Outcome direction |
| --- | --- | --- |
| `bop_opening_authority_crisis` | armed extreme or constitutional extreme with severe pressure | forces public order, route split, or confidence mission |
| `bop_emergency_overreach_crisis` | apparatus extreme | directorate reveal, parliamentary pushback, or emergency recovery |
| `bop_commonwealth_dependency_crisis` | liaison extreme | base access scandal, anti basing vote, or dependency route |
| `bop_labour_congress_crisis` | congress extreme | worker council route, production truce, or client risk |
| `bop_blueshirt_guard_crisis` | guard extreme | coup risk, guard split, or corporate chamber correction |
| `bop_ira_army_council_crisis` | council extreme | compromised network, crackdown, or hard takeover |
| `bop_cultural_capture_crisis` | mobilisation extreme | corrupted restoration failure or civic recovery |
| `bop_directorate_entrenchment_crisis` | security extreme | permanent security state or civilian rule timetable |

## AI validation scenarios

Implementation should validate at least these scenarios:

1. Historical Ireland reaches war with BOP near cabinet or moderate apparatus, high Emergency Preparedness, and no directorate unless crisis conditions are real.
2. Fine Gael legal route can use defence liaison without becoming a dependency by default.
3. Labour democratic route can complete without drifting into Soviet client pressure.
4. Labour social republic can use congress power while still needing anti dependency choices.
5. Blueshirt route can reach guard power but faces crisis if it pushes too far.
6. IRA route can reach hard route tools but foreign contact creates real exposure and British pressure.
7. Hidden cultural route can remain civic and open the common platform path.
8. Emergency Directorate can enter during severe crisis and can exit through restoration.
9. Northern settlement uses BOP legitimacy but still relies on Partition Pressure and integration decisions.
10. AI does not keep stale BOP decisions after a route closes.
