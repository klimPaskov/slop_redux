# Ireland BOP spec part 2, modes and ranges

## Mode map

| BOP mode | Active first side | Active second side | Used by | Core question |
| --- | --- | --- | --- | --- |
| `ire_bop_mode_opening_state` | constitutional government | armed political pressure | opening trunk before route lock | Can the state keep politics inside the law. |
| `ire_bop_mode_historical_emergency` | civilian cabinet | emergency apparatus | historical sovereign neutrality and strict neutral route | Can wartime powers defend neutrality without becoming permanent rule. |
| `ire_bop_mode_commonwealth_cooperation` | independent parliamentary review | defence liaison cabinet | Fine Gael constitutional opposition and Commonwealth cooperation | Can cooperation with Britain remain a bargain rather than dependency. |
| `ire_bop_mode_labour_republic` | Dáil Labour cabinet | workers congress | Labour democratic socialist and social republic routes | Can reform power be expanded without losing constitutional control. |
| `ire_bop_mode_blueshirt_corporate` | parliamentary right and chambers | Blueshirt guard | corporatist Ireland and O'Duffy route | Does the right govern through institutions or through a uniformed movement. |
| `ire_bop_mode_republican_underground` | civilian republican front | Army Council | IRA underground republic and reconciliation overlay | Does republican policy remain political or become military command. |
| `ire_bop_mode_civic_cultural` | civic institutions | cultural mobilisation networks | hidden civic cultural restoration | Can cultural renewal remain inclusive and constitutional. |
| `ire_bop_mode_emergency_directorate` | civilian restoration | security directorate | hidden Emergency Directorate | Does emergency rule return power or keep it. |

Do not create a separate Partition BOP. Partition Pressure already handles Northern support, unionist alarm, British willingness, and integration progress. The BOP changes the domestic legitimacy of those actions.

## Opening state mode

Visible pair:

- First side: `ire_bop_side_constitutional_government`
- Second side: `ire_bop_side_armed_political_pressure`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `constitutional_extreme` | the Dáil can block radical shortcuts but risks complacency and opposition resentment | hidden civic route easier, IRA and Blueshirt crisis harder, emergency response slower if preparedness is low |
| `constitutional_high` | legal politics are credible | peaceful settlement costs fall, reconciliation missions improve, radical route gates require stronger triggers |
| `constitutional_moderate` | the government has advantage but must still manage old wounds | normal historical and opposition options stay open |
| `contested_center` | all routes remain possible but major gambles need authority work | route convention, confidence missions, and public order debates matter more |
| `armed_moderate` | armed actors gain public space | IRA and Blueshirt path reveal chances rise, foreign trust falls |
| `armed_high` | the state is visibly challenged | public order missions, crackdown or reconciliation choices, opposition split risk |
| `armed_extreme` | the government may lose initiative | forced crisis branch, coup or crackdown risk, peaceful Northern tools blocked |

Shift sources:

- Dáil and constitution focuses move toward constitutional government.
- Amnesty and veterans reconciliation can move toward constitutional government if not paired with repression.
- IRA tolerance, Blueshirt rallies, failed public order, and border incidents move toward armed pressure.
- Economic distress can drift toward armed pressure unless industry or relief decisions address it.

## Historical emergency mode

Visible pair:

- First side: `ire_bop_side_civilian_cabinet`
- Second side: `ire_bop_side_emergency_apparatus`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `cabinet_extreme` | civilian restraint dominates | high legitimacy, weak emergency reaction, longer defence missions, lower directorate risk |
| `cabinet_high` | cabinet controls the Emergency | better diplomacy and neutrality credibility, moderate readiness penalties if war pressure is high |
| `cabinet_moderate` | public law leads with useful security support | best historical neutrality band when preparedness is healthy |
| `emergency_center` | authority is contested by wartime needs | balanced route, decision costs depend heavily on preparedness |
| `apparatus_moderate` | emergency services shape policy | stronger port, coast, and counter espionage actions, mild democratic strain |
| `apparatus_high` | security state tools become normal | Emergency Directorate reveal gate, Labour and cultural routes strained, Northern peaceful tools harder |
| `apparatus_extreme` | emergency apparatus can rule | directorate commitment or legitimacy crisis, high survival tools, serious postwar cleanup |

Shift sources:

- Emergency Orders, censorship, G2 central files, LDF centralization, port garrison powers, and rationing enforcement move toward emergency apparatus.
- Parliamentary review, fair internment rules, public confidence missions, and civilian rule timetables move toward civilian cabinet.
- Failed war incidents can push toward emergency apparatus if the player responds with coercion, or toward cabinet if the player refuses urgent powers.

## Commonwealth cooperation mode

Visible pair:

- First side: `ire_bop_side_independent_parliamentary_review`
- Second side: `ire_bop_side_defence_liaison_cabinet`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `review_extreme` | Ireland refuses meaningful defence liaison | high independence, weak British trust, partition talks harder during war |
| `review_high` | parliament controls cooperation | safe democratic route, slower defence support, lower foreign access pressure |
| `review_moderate` | cooperation remains tightly negotiated | best band for guarded Commonwealth cooperation without dependency |
| `cooperation_center` | London and Dublin argue over the bargain | unlocks bargaining missions and observer channels |
| `liaison_moderate` | defence liaison gives useful support | better air and naval warning, higher British leverage, improved war access if needed |
| `liaison_high` | British cooperation shapes Irish policy | partition concessions possible, dependency risk rises, strict neutrality blocked |
| `liaison_extreme` | cooperation becomes dependency | base access crisis, domestic backlash, constitutional authority damage |

Shift sources:

- Defence liaison, shared intelligence, convoy protection, and air warning arrangements move toward defence liaison cabinet.
- Parliamentary review, anti basing clauses, independent cabinet votes, and public legal safeguards move toward independent review.
- British betrayal, denied partition concessions, or unpopular base pressure can snap the value back toward review.

## Labour republic mode

Visible pair:

- First side: `ire_bop_side_dail_labour_cabinet`
- Second side: `ire_bop_side_workers_congress`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `cabinet_labour_extreme` | Labour governs cautiously and loses movement energy | stable democracy, weaker worker defence, social republic capstone blocked |
| `cabinet_labour_high` | reform is cabinet led | good democratic socialist band, lower church and employer crisis, slower radical industry |
| `cabinet_labour_moderate` | cabinet and unions cooperate | best band for stable Labour government |
| `labour_center` | unions and cabinet bargain constantly | strike missions and congress decisions become central |
| `congress_moderate` | worker institutions drive policy | stronger cooperative industry and worker defence, rising church and employer pressure |
| `congress_high` | congress authority challenges cabinet | social republic gates, foreign suspicion, production disruption risk |
| `congress_extreme` | congress can outgrow parliamentary control | cross border Labour council or client risk, possible route crisis if Soviet pressure is high |

Shift sources:

- Parliamentary reform bills, coalition discipline, and rights guarantees move toward Dáil Labour cabinet.
- Strike victories, factory committees, worker defence, and congress votes move toward workers congress.
- Soviet aid should move the route through Foreign Access Pressure first, then create BOP decisions that test whether the movement accepts dependency.

## Blueshirt corporate mode

Visible pair:

- First side: `ire_bop_side_parliamentary_right_chambers`
- Second side: `ire_bop_side_blueshirt_guard`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `chambers_extreme` | the right stays parliamentary and guard politics lose force | route may soften into Fine Gael legalism, O'Duffy route blocked |
| `chambers_high` | corporate language stays institutional | corporate chamber route without street takeover, lower civil conflict risk |
| `chambers_moderate` | party and guard share influence | transition band, internal split decisions matter |
| `corporate_center` | route direction is unresolved | O'Duffy confidence and chamber legality missions decide path |
| `guard_moderate` | Blueshirt organization shapes policy | stronger paramilitary tools, labour unrest and republican resistance rise |
| `guard_high` | uniformed movement dominates | O'Duffy hard route, foreign right wing access, democratic isolation |
| `guard_extreme` | guard power can become state capture | coup crisis, civil resistance, severe foreign reaction and Northern alarm |

Shift sources:

- Legal chamber acts, party discipline, and moderate conservative deals move toward parliamentary right and chambers.
- Uniformed rallies, cadre mobilization, anti communist street action, and Spanish connection decisions move toward Blueshirt guard.
- Failed guard discipline can push sharply to guard extreme or force a split back to chambers.

## Republican underground mode

Visible pair:

- First side: `ire_bop_side_civilian_republican_front`
- Second side: `ire_bop_side_army_council`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `front_extreme` | civilian republican policy dominates | reconciliation and political front available, hard underground disabled |
| `front_high` | political republicanism directs strategy | safer Northern support, lower foreign exposure, slower uprising tools |
| `front_moderate` | civilian front has advantage | balanced republican route, armed tools need approval decisions |
| `republican_center` | policy is contested between front and military command | safehouse, amnesty, and command discipline decisions matter |
| `council_moderate` | Army Council has leverage | faster border and sabotage tools, British and G2 pressure rises |
| `council_high` | military command directs policy | hard route unlocks, German contact risk, civilian legitimacy collapses |
| `council_extreme` | Army Council can consume the state | compromised network, British intervention risk, route failure or unstable takeover |

Shift sources:

- Civilian front conferences, public political support, amnesty under watch, and non German channels move toward civilian front.
- Sabotage, safehouse expansion, courier contact, arms raids, and Army Council decisions move toward Army Council.
- German contact must create exposure and dependency risk. It should never be a clean power path.

## Civic cultural mode

Visible pair:

- First side: `ire_bop_side_civic_institutions`
- Second side: `ire_bop_side_cultural_mobilisation_networks`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `civic_extreme` | culture is institutional and cautious | safe legitimacy, hidden payoff slower, popular mobilization weak |
| `civic_high` | schools and civil service lead renewal | stable cultural route, safer Northern contacts |
| `civic_moderate` | institutions guide civic renewal | best band for hidden civic route |
| `cultural_center` | public networks and institutions balance each other | route decisions are most flexible |
| `mobilisation_moderate` | voluntary networks drive the route | faster cultural progress, higher Partition Pressure risk |
| `mobilisation_high` | cultural mobilization becomes political pressure | common platform possible, unionist alarm rises if safeguards weak |
| `mobilisation_extreme` | revival can be captured by coercive politics | corrupted restoration failure, route cleanup, cultural route disqualification |

Shift sources:

- Civil service, presidency, legal guarantees, and school administration move toward civic institutions.
- Public language societies, rural networks, diaspora drives, and Northern cultural contacts move toward cultural mobilisation.
- Sectarian pressure, route slogans, or armed movement infiltration should push toward mobilisation extreme and possible corruption.

## Emergency Directorate mode

Visible pair:

- First side: `ire_bop_side_civilian_restoration`
- Second side: `ire_bop_side_security_directorate`

| Band | Gameplay direction | Unlocks and pressure |
| --- | --- | --- |
| `restoration_extreme` | emergency rule is being dismantled | return to normal government, weaker emergency decisions, lower authoritarian risk |
| `restoration_high` | timetable is credible | restoration missions improve and directorate penalties shrink |
| `restoration_moderate` | civilian government is regaining control | safest recovery band |
| `directorate_center` | restoration and security compete | player must choose recovery or permanent security route |
| `security_moderate` | security command still drives policy | strong defence and counter espionage, high democratic strain |
| `security_high` | directorate becomes entrenched | permanent security state route, Northern peaceful settlement strained |
| `security_extreme` | security command can become the regime | authoritarian neutral capstone, diplomatic isolation, forced cleanup if war ends badly |

Shift sources:

- Civilian rule timetable, public review, election preparation, and party restoration move toward civilian restoration.
- Emergency arrests, G2 centralization, permanent censorship, LDF political use, and security integration move toward security directorate.

## Mode switching rules

| Trigger family | BOP action |
| --- | --- |
| opening trunk completed | initialize opening mode if not already active |
| route lock focus completed | switch to route mode and translate prior value |
| route fails or is abandoned | switch to a recovery mode or opening mode with penalties |
| hidden route reveal accepted | switch to hidden mode when the hidden route becomes the new governing conflict |
| foreign client state reached | do not switch to a foreign BOP. Keep route BOP and add Foreign Access Pressure penalties |
| Northern settlement starts | keep current route BOP and add domestic legitimacy shifts based on settlement tools |
| tag switch or cosmetic identity change | keep BOP if Ireland remains the same gameplay country, clean invalid side flags |
| annexation or country invalid | remove BOP, clear variables and active missions |
