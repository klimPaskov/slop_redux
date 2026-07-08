# Ireland focus tree achievement prompt

Feature slug: `ireland_focus_tree`
Feature name: Ireland comprehensive national focus tree

This prompt defines achievement design. Working labels are not final achievement titles. Do not copy working labels into localisation. Final title and description wording should be written during implementation, and any source dependent allusion must go through the text and audio research workflow.

## Achievement implementation rules

Achievements should be difficult and route specific. Do not unlock achievements merely because the player selected a route or survived a few days. Each achievement should require route mastery, a hard combination, strict disqualifiers, a rare peaceful settlement, avoidance of dependency, or a dangerous crisis solved without the easiest shortcut.

Each achievement needs tracking flags or variables, unlock triggers, disqualifiers, localisation direction, and 64x64 icon direction. Asset work must create completed, grey, and not eligible variants if the achievement system requires them.

## Planned achievement set

| Working id | Working label, not final title | Eligible start | Required route or situation | Unlock conditions | Disqualifiers | Difficulty | Visibility | Icon direction |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `ireland_focus_tree_constitutional_neutrality_mastery` | constitutional neutral mastery | Ireland | Historical sovereign neutrality | pass constitution, regain ports, keep neutrality, reach high Emergency Preparedness, avoid faction entry, complete at least one postwar arbitration step | foreign base access above dependency threshold, Axis or Allied faction entry, failed port transfer | hard | visible | constitution seal with coastal watch motif |
| `ireland_focus_tree_ports_without_bases` | ports without bases | Ireland | historical or strict opposition neutrality | regain Cobh, Berehaven, and Lough Swilly, defend each port, refuse permanent foreign basing, survive a major war nearby | cede port access, lose any port state, preparedness below route floor | hard | visible | three harbour lights or coastal batteries |
| `ireland_focus_tree_emergency_watch_complete` | emergency watch complete | Ireland | any non collapsed route | complete all Coastwatching and G2 preparedness mission families before a major war ends | ignore LOP chain, accept German spy dependency, lose coastal state | medium hard | visible | binoculars and signal lamp |
| `ireland_focus_tree_cosgrave_settlement` | constitutional opposition settlement | Ireland | Opposition | put constitutional opposition in power, keep democracy, secure British supported Northern concession or full settlement, avoid Blueshirt route | O'Duffy route active, Ireland becomes puppet, no Northern concession after Allied cooperation | hard | visible | legal boundary paper and ballot |
| `ireland_focus_tree_labour_without_dependency` | independent labour republic | Ireland | Labour democratic or social republic | complete social republic, cooperative industry, worker defence regularization, all island labour mission, keep Soviet pressure below dependency threshold | become Soviet puppet or dependent, Blueshirt crackdown, failed worker boards | hard | visible | cooperative factory and red green civic motif without final slogan |
| `ireland_focus_tree_workers_cross_the_border` | all island labour route | Ireland | Labour | win peaceful or semi peaceful Northern settlement through labour support and observer missions, complete worker integration stage | use border war or IRA uprising, high unionist alarm at formation | very hard | hidden | workers bridge over border road |
| `ireland_focus_tree_blueshirt_brittle_victory` | corporate state coercive victory | Ireland | Blueshirt | complete corporate state, coerce or conquer Northern settlement, survive labour resistance and republican backlash, complete security integration | Britain controls Dublin or route collapses, foreign sponsor annexes or puppets Ireland | very hard | visible | blue uniformed silhouette and cracked state seal, no real symbol unless sourced |
| `ireland_focus_tree_oduffy_against_the_reds` | anti communist route victory | Ireland | Blueshirt | complete Irish Brigade lessons, defeat or contain a communist major or local communist backed threat, keep corporate state intact | switch out of route, lose corporate capstone, dependence on defeated sponsor | hard | hidden | anti communist shield motif, source caution |
| `ireland_focus_tree_ira_absorbed_not_broken` | absorbed underground | Ireland | IRA absorption | integrate the underground under state orders, complete border service sections, avoid German dependency, reach a negotiated or limited Northern settlement | Army Council takeover, Plan Kathleen exposure crisis unresolved, failed crackdown | hard | visible | safehouse key and state seal |
| `ireland_focus_tree_plan_kathleen_exposed` | dangerous courier exposed | Ireland | historical counter espionage or IRA | expose or survive the Plan Kathleen style foreign courier chain without becoming a German dependent route | accept compromised formation, lose legitimacy below collapse threshold | medium hard | hidden | intercepted map and radio code, no readable text |
| `ireland_focus_tree_revolutionary_all_island` | revolutionary all island state | Ireland | IRA hard route | complete Army Council route, win Northern campaign, form revolutionary all island identity, then reduce German pressure below compromised threshold | fail uprising, remain German dependent, lose capital | very hard | hidden | council shadow and border flame motif, no final slogan |
| `ireland_focus_tree_no_one_gets_the_ports` | strict coastal sovereignty | Ireland | any neutral route | maintain Irish control of all returned ports, no permanent foreign access, high port readiness, high coast watch readiness | faction entry, leased ports, lost port state | hard | visible | locked harbour gate and tricolour light motif |
| `ireland_focus_tree_atlantic_compact` | neutral Atlantic compact | Ireland | strict neutral late game | form the rare Atlantic compact or conference mechanic, keep no foreign base doctrine, include at least two eligible partners | foreign access dependency, joined major faction before compact | very hard | hidden | Atlantic compass and small state circle |
| `ireland_focus_tree_reconciled_island` | reconciled all island state | Ireland | peaceful all island formation | form unified Ireland through peaceful or legal settlement, complete all integration stages, keep unionist alarm below final threshold | violent Northern war, coercive route, unresolved resistance | very hard | visible | joined hands over border marker, no text |
| `ireland_focus_tree_cultural_epilogue` | civic cultural epilogue | Ireland | peaceful unified high legitimacy | complete cultural restoration epilogue after peaceful reunification, keep constitutional authority high, avoid extremist routes | Blueshirt or Army Council route, violent formation, failed integration | rare hard | hidden | harp, book, and presidential seal style, source review for motifs |
| `ireland_focus_tree_small_army_long_coast` | prepared small power | Ireland | any route | remove or transform `Small Army, Long Coast`, complete coast watch, port defence, air warning, naval patrol, and LDF chains before being invaded | fail any emergency component, lose a port, rely on foreign occupation | hard | visible | coastline with watch post and reserve rifle |
| `ireland_focus_tree_no_fairy_dust` | meaningful branch coverage | Ireland | meta route mastery | complete one political route, one industry route, one military route, one diplomacy route, one Northern route, and one mechanic capstone in same campaign | use debug or fallback content, skip route capstone | hard | hidden | focus tree branch motif with strong central seal |

## Tracking notes

- Strict neutrality achievements need flags for no faction entry, no permanent foreign base access, and no sponsor dependency.
- Northern settlement achievements need route of formation flags: peaceful, legal, labour, coercive, uprising, emergency protectorate.
- Integration achievements need stage tracking for each Northern state group.
- Plan Kathleen achievement needs a flag for exposure, refusal, containment, or compromised acceptance.
- Labour dependency achievements need Soviet pressure band and anti dependency mission completion.
- Blueshirt achievements need route survival, repression backlash state, and sponsor collapse safety checks.
- Atlantic compact achievement needs member count, compact formed flag, and base access disqualifier.

## Asset directions

Use `hoi4-feature-assets` for icons. Each icon should be readable at 64x64. Avoid text in icons. Do not use real movement emblems unless sourced and context appropriate. Use generated symbolic art for most achievement icons. Produce grey and not eligible variants according to the achievement workflow.

## Canonical hidden path achievement addendum

The hidden path achievements below are mandatory planned achievements. Working labels are not final localisation.

| Working id | Working label, not final title | Eligible start | Required route or situation | Unlock conditions | Disqualifiers | Difficulty | Visibility | Icon direction |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `ireland_focus_tree_restoration_without_a_crown` | civic restoration without crown | Ireland | hidden civic cultural restoration | complete civic cultural capstone while democratic, independent, high authority, low armed pressure, and no violent Northern war | Blueshirt route, Army Council takeover, entrenched directorate, sponsor dependency | very hard | hidden | constitution, harp, and open civic book, source review for motifs |
| `ireland_focus_tree_common_platform` | common platform settlement | Ireland | hidden Northern civic settlement | settle Northern question through observer backed guarantees and integration work without war | border war, IRA uprising, high unionist alarm, coercive settlement | very hard | hidden | bridge, schoolbook, and observer seal |
| `ireland_focus_tree_watchmen_of_the_west` | Emergency directorate recovery | Ireland | hidden Emergency directorate | enter directorate under invasion danger, defend ports, then restore civilian rule | permanent security state, port loss, permanent foreign basing | very hard | hidden | coast watch post and emergency seal |
| `ireland_focus_tree_conference_of_neutrals` | conference of neutrals | Ireland | Atlantic neutral compact | create compact or conference with enough valid observers while refusing permanent bases | major faction entry, sponsor dependency, insufficient members | very hard | hidden | compass and small state circle |
| `ireland_focus_tree_no_crown_no_courier` | no crown and no courier | Ireland | civic restoration plus counter espionage | complete civic restoration and expose or contain the foreign courier chain in the same campaign | German dependency, Army Council rule, cultural corruption | extreme | hidden | civic book and intercepted radio map |

Tracking must include route flags, disqualifiers, hidden reveal completion, violent Northern war flag, foreign dependency band, port control, compact member count, and civilian restoration after directorate.

## Route-specific hidden overlay achievement hooks

| Working key | Overlay | Core challenge | Disqualifiers | Icon direction |
| --- | --- | --- | --- | --- |
| `ireland_focus_tree_backchannel_without_bases` | constitutional backchannel | Secure a Northern concession or compact through legal cooperation while refusing dependency. | Blueshirt route, puppet status, permanent foreign base policy | boundary file and sealed coast light |
| `ireland_focus_tree_front_without_masters` | Labour independent front | Build Labour anti-fascist defence and cooperative supply while keeping Soviet pressure below client band. | Soviet client route, militia capture, failed worker discipline | worker shield and supply crate |
| `ireland_focus_tree_chambers_after_the_chief` | corporate chambers without O'Duffy | Keep the corporatist route alive after leader crisis without becoming foreign owned. | Fine Gael route, movement fracture, sponsor capture | chamber hall and cracked baton motif |
| `ireland_focus_tree_amnesty_before_uprising` | republican reconciliation backchannel | Stand down border cells and restore civil authority before an uprising or British ultimatum. | Army Council state, active courier dependency, sabotage crisis | broken rifle and civic seal motif |


## BOP and event achievement addendum

Achievements may use BOP and event state. Do not unlock route achievements from focus completion alone when the challenge includes event choices, BOP bands, mission outcomes, or settlement events.

Additional tracking requirements:

| Working id | Core challenge | Required event or BOP proof | Icon direction |
| --- | --- | --- | --- |
| `ireland_focus_tree_cabinet_over_emergency` | keep historical neutrality active while preventing permanent emergency rule | Emergency BOP never reaches security extreme, Emergency powers sunset event completed | cabinet table and coast light |
| `ireland_focus_tree_no_one_commands_the_council` | complete IRA absorption without Army Council state capture | Army Council capture event never fires, absorption event completed, courier crisis contained | broken command seal and safehouse key |
| `ireland_focus_tree_events_of_the_island` | complete a full campaign path with required route event chains and no fallback route | event coverage flags for opening, political route, industry, military, diplomacy, Northern, BOP, and late game | branching event cards around Ireland outline |
| `ireland_focus_tree_balanced_authority` | finish a peaceful Northern settlement while BOP stays out of extreme bands | observer and integration events complete, no BOP extreme crisis event | scales, border bridge, and civic seal |

Event achievements need hidden flags for event family completion, crisis avoidance, major event outcome, and cleanup completion.


Add achievement hooks for flavour event mastery

Add difficult achievement hooks where the flavour layer supports real play. Candidate working keys should reward completing a full coast watch flavour chain without foreign access scandal, completing school and folklore civic work without corrupted restoration, solving winter fuel pressure while keeping Emergency powers limited, completing Northern local safeguard events without coercion, and honoring merchant marine memory after maintaining strict neutrality. These are working labels only and require final title direction during implementation.
