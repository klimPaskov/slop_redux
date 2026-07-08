# Ireland focus tree spec, part 6 reunification and formable design

This file defines how Ireland can become an all island state and how route specific identities should work after reunification. Working labels are internal handles only. They are not final country names, decision names, achievement titles, slogans, or event text.

## Formation design stance

A unified Ireland identity should be focus prepared and decision verified. Focuses can build legitimacy, route claims, observer support, military readiness, or underground support. The final formation or settlement decision must verify state control, settlement flags, subject status, or peace conditions.

Reunification should have three layers:

1. Claim preparation through focuses and missions.
2. Formation or settlement decision that checks control or agreement.
3. Post settlement integration that grants stable benefits only after state work.

Full cores should not appear instantly across Northern Ireland unless the route is already peaceful, internationally recognized, and integration missions have been completed. Violent routes can gain claims and occupation tools first. Cores should follow later, and failure should matter.

## State groups for implementation

Exact state ids must be mapped during implementation from the target mod version. The spec uses geographic working groups so the implementation agent can build readable scripted triggers and tooltips.

| Working state group | Intended geographic meaning | Use |
| --- | --- | --- |
| `ireland_core_south_group` | The states already belonging to Ireland at game start | Formation owner baseline and stability check |
| `northern_ireland_full_group` | All states representing Northern Ireland | Required for full all island formation by conquest or treaty |
| `northern_ireland_key_cities_group` | Belfast and Derry or their target mod equivalents | Required for negotiated settlement and postwar stability |
| `northern_ireland_border_counties_group` | Border counties and road or rail crossing states | Border missions, partial settlement, frontier defence |
| `northern_ireland_port_group` | Belfast, Derry, Larne, or mapped port states | Naval and supply control after settlement |
| `western_approaches_port_group` | Cobh, Berehaven, Lough Swilly, and related coastal states | Port settlement, neutral defence, British access |

## Main formation paths

| Working formation path | Who can prepare it | Verification method | Immediate result | Integration result | Major risks |
| --- | --- | --- | --- | --- | --- |
| `peaceful_all_island_settlement` | Historical, opposition, Labour democratic | Treaty, plebiscite, arbitration, British willingness, high legitimacy | State transfer or claims with legitimacy bonus | Staged cores through administration and rights missions | unionist alarm, failed observers, British refusal |
| `commonwealth_linked_settlement` | Constitutional opposition | British trust, defensive cooperation bargain, Northern safeguards | Settlement with high British support and access pressure | Stable integration if minority safeguards succeed | dependency without concessions |
| `labour_all_island_settlement` | Labour democratic or social republic | Northern labour support, low sectarian alarm, observer conditions | Labour network influence and staged settlement | Worker councils integrated into state economy | church backlash, employer resistance, Soviet suspicion if radical |
| `coercive_frontier_settlement` | Blueshirt route | War, ultimatum, occupation, military readiness | Claims or annexation under high resistance | Slow cores after security and administration missions | British intervention, strikes, republican resistance |
| `revolutionary_northern_campaign` | IRA route | Uprising, war, state control, safehouse network | Irregular control, claims, possible puppet or annexation | Cores only after cells become administration or civil authority returns | exposure, German dependency, crackdown |
| `emergency_border_protectorate` | Rare defensive situation | Britain collapse, Northern chaos, Ireland high preparedness | Temporary security administration or guarantee | Optional integration after peace and observer work | legitimacy loss if abused |

## Unified Ireland identity handling

The all island identity should usually remain the Ireland tag with a cosmetic tag or dynamic country name. A new tag is not necessary unless the repository needs a separate tag for achievement or diplomacy handling. The default should be a cosmetic identity to preserve focus progress and avoid invalid tag switching.

### Route variants

| Working identity variant | Route | Public identity direction | Flag direction | Leader direction | Notes |
| --- | --- | --- | --- | --- | --- |
| `ireland_unified_constitutional` | Historical and constitutional opposition | Direct all island Irish state with constitutional legitimacy | Tricolour or sourced all island civic variant if needed | existing constitutional leader or president handling | Default and most stable form. |
| `ireland_unified_commonwealth_associated` | Opposition with Allied or Commonwealth pact | Ireland remains independent but acknowledges a defence or association framework | Distinct cosmetic flag only if route identity requires it | Cosgrave or successor leadership | Must not look like British puppet unless actually puppet. |
| `ireland_unified_social_republic` | Labour | Social republic identity with democratic or radical sub variants | Generated or sourced labour civic flag depending motifs | Norton, Labour cabinet, or route council | Avoid making it automatically Soviet. |
| `ireland_unified_corporate_state` | Blueshirt | National corporate all island state | Historical symbols sourced where attested, generated variants for invented identity | O'Duffy or corporate council | Should carry unrest and legitimacy penalties. |
| `ireland_unified_revolutionary_republic` | IRA | Revolutionary republic or Army Council state | IRA related symbols require source review | Seán Russell, Stephen Hayes, or Army Council body pending source review | German dependency should alter legitimacy and foreign relations. |
| `ireland_cultural_epilogue` | Peaceful high legitimacy unified state | Ceremonial cultural restoration within constitutional politics | Generated cultural variant or sourced cultural symbol if historically attested | President and cultural institutions, not a new monarch by default | No conquest ladder and no occult content. |

## Formation decisions

### `proclaim_all_island_settlement_decision`

Purpose: Perform the ordinary unified Ireland formation after peaceful settlement or full state control.

Visible requirements direction:

- Ireland controls or has treaty backed transfer for `northern_ireland_full_group`, or it has completed an accepted plebiscite route that transfers the relevant state group.
- Ireland has completed one accepted political route that can govern the all island state.
- Ireland has enough Constitutional Authority for peaceful formation, or enough route authority for coercive formation.
- Britain is willing, defeated, unable to object, or directly party to the settlement.
- Northern unionist alarm is below the threshold for clean formation, or the player accepts a contested formation with harsher integration.

Costs and sacrifices:

- Political legitimacy or route authority.
- Civilian factory burden for administration.
- Infantry equipment and support equipment for police transition.
- Stability or war support cost if formation is contested.
- Foreign access or recognition cost if a sponsor helped.

Effects direction:

- Apply route specific cosmetic identity.
- Add claims or provisional cores according to settlement quality.
- Unlock post settlement integration category.
- Remove obsolete border agitation decisions.
- Start integration missions for Belfast, Derry, border counties, and port states.
- Fire a formation event or news event for the public formation milestone.

AI behavior:

- AI forms only when it controls the required state groups or has a clear treaty route.
- AI should not form during active losing war unless emergency protectorate route is valid.
- AI should delay if stability is low and resistance is high unless route is coercive.

### `commonwealth_linked_settlement_decision`

Purpose: A route specific formation for the constitutional opposition that gains British support or acquiescence through defence cooperation.

Requirements direction:

- Opposition route active.
- Britain trust high.
- Defensive cooperation or Allied association complete.
- Ireland has secured a concession through Treaty Review Office or Allied settlement conference.
- Ireland is not a puppet unless the design explicitly accepts a puppet failure state.

Effects direction:

- Opens integration with lower British diplomatic penalty.
- Raises foreign access pressure unless anti dependency safeguards were taken.
- Improves minority rights mission success.
- Disqualifies strict neutral achievement.

Failure state:

If Ireland gives defence access but fails to secure Northern concessions, the route should produce a dependent ally outcome. It can still be playable, but the all island formation remains locked until a later war or diplomatic reversal.

### `social_republic_all_island_decision`

Purpose: Labour route formation through worker solidarity and social reforms.

Requirements direction:

- Labour route active.
- Northern labour support high.
- Unionist alarm not above hard block, unless violent postwar conditions apply.
- Worker defence committees either regularized or explicitly stood down for observer conditions.
- Foreign access pressure from Soviet support below dependency threshold for clean democratic formation.

Effects direction:

- Applies social republic identity and worker integration missions.
- Northern industry integration gives production and labour council benefits after missions.
- Church and employer backlash missions may appear.

Failure state:

Radical dependency, failed worker missions, or sectarian backlash can split the settlement and force a slower integration chain.

### `corporate_all_island_decision`

Purpose: Blueshirt route formation after coercive settlement or war.

Requirements direction:

- Blueshirt route active.
- Military preparedness high.
- Required states controlled, or Northern government capitulated, or ultimatum accepted under pressure.
- Labour resistance and republican underground pressure not already in runaway failure.

Effects direction:

- Applies corporate all island identity.
- Grants claims first and only limited cores after security missions.
- Unlocks strong security decisions and anti communist foreign policy.
- Raises resistance and international suspicion.

Failure state:

If integration missions fail, the corporate state should face general strike, guerrilla resistance, and legitimacy collapse. The route should be powerful but brittle.

### `revolutionary_all_island_decision`

Purpose: IRA route formation after uprising, war, or state collapse.

Requirements direction:

- IRA route active.
- Either full control of Northern state group or successful Northern uprising mission.
- Foreign dependency must be resolved for clean formation, or accepted as a dangerous compromised formation.
- Army Council authority or absorption path must be clear.

Effects direction:

- Applies revolutionary identity.
- Unlocks cell integration, dependency purge, and civil authority restoration decisions.
- Creates severe British and international reaction unless Britain is defeated or unable to respond.

Failure state:

German contact exposure, failed uprising, or failure to turn cells into administration should create a broken revolutionary state with harsh penalties until repaired.

## Post settlement integration ladder

Integration should use stages. Each stage should be visible in the decision category and in national spirit tooltips.

| Stage | Working label | Requirements | Result | Failure pressure |
| --- | --- | --- | --- | --- |
| 0 | `contested_transfer` | State transferred or occupied but no administration | Claims, resistance, garrison need | resistance, unionist alarm, foreign criticism |
| 1 | `security_transition` | Police transition mission complete | resistance down, state no longer emergency only | raids and security incidents |
| 2 | `civil_administration` | local administration and infrastructure missions | compliance or local support rises, state modifiers improve | corruption, supply strain |
| 3 | `rights_and_representation` | minority rights or route specific settlement | legitimacy and unionist alarm improve | political backlash |
| 4 | `constitutional_integration` | stable peace, low resistance, high enough authority | staged cores or permanent integration | frozen claims or crisis |
| 5 | `reconciled_all_island_state` | all key states integrated and route capstone complete | final unified idea upgrade and achievement hook | none beyond normal politics |

## Partial settlement handling

A partial settlement can occur if only border counties or key cities transfer. This should be allowed when it makes sense, but it should not be treated as complete reunification.

Partial outcomes:

- `border_adjustment_only`: border counties transfer or become claims after arbitration. Opens limited integration missions.
- `city_observer_zone`: Belfast or Derry receives observer or autonomy status. This should be rare and event driven.
- `security_protectorate`: Ireland temporarily administers a Northern state group during British collapse or major war. Requires later decision to integrate, return, or federalize.
- `failed_plebiscite`: no transfer, but Ireland gains legitimacy or lessons if the process was fair and peaceful.
- `failed_violent_attempt`: Britain and Northern Ireland become more hostile, and Ireland receives route crisis missions.

## Hidden or second stage formables

### Full hidden high kingship route

Rejected for this package. It adds bloat, pushes the design toward mythology, and does not improve the core Ireland gameplay loop enough. It should not be implemented as a full focus route.

### Cultural restoration epilogue

Accepted only as a rare ceremonial epilogue for a peaceful unified state.

Requirements direction:

- Unified Ireland formed through peaceful or legally accepted route.
- Integration stage at or near final form.
- Constitutional Authority high.
- Foreign Access Pressure low or balanced.
- No Blueshirt corporate state and no Army Council state.
- No active unionist alarm crisis.

Effects direction:

- Unlock cultural and language decisions.
- Possible cosmetic identity or president linked idea stage.
- No new cores, no war goals, no monarchy, no supernatural content.
- Achievement hook for peaceful cultural consolidation.

Asset direction:

- Generated cultural focus and achievement icons may be used.
- Any use of Gaelic League, presidential, or historical cultural symbols requires source review.
- No final slogans or quotations without text research.

### Atlantic compact

Accepted as a late game neutral faction or conference mechanic, not a formable.

Requirements direction:

- Ireland remained neutral or strictly independent.
- Emergency Preparedness high.
- Foreign Access Pressure below dependency threshold.
- At least two eligible friendly neutral or democratic states exist.
- Ireland has coastal, shipping, and diplomatic credibility.

Effects direction:

- Creates shared observation, convoy safety, and small state arbitration decisions.
- Does not force automatic wars.
- Can support postwar recognition or Northern settlement if Britain is friendly or exhausted.

Failure state:

If Ireland takes foreign bases or accepts too much sponsor dependency, this branch should downgrade into ordinary diplomacy.

## Formable asset and text requirements

Required visual assets:

- Formation decision icons for each formation path.
- All island identity flags where route identity changes public presentation.
- Ideology variants only when the route needs distinct public identity.
- Leader portraits for real route leaders, sourced only.
- Generated council portraits for collective or fictional bodies.
- Achievement icons for hard formation outcomes.
- Optional news or report image for first all island formation, with source mode based on final event presentation.

Research gates:

- No final proclamation title.
- No final formation event body.
- No final slogan or cultural motto.
- No quote from Irish literature, speeches, hymns, songs, or political sources until sourced through text research.

## Formable AI safety

Ireland AI should not pursue every formation path. It should follow route and campaign state.

- Historical AI seeks peaceful settlement only after high legitimacy, high preparedness, and favourable postwar conditions.
- Opposition AI can bargain for settlement if Britain trust is high and Ireland has not become a client without concessions.
- Labour AI seeks worker and plebiscite route if not foreign dependent.
- Blueshirt AI attempts coercive settlement only if Britain is weak, Ireland is prepared, and internal resistance is manageable.
- IRA AI attempts uprising only under rare valid conditions, such as Britain distracted, Northern support high, and exposure low.
- AI should delay formation if it controls Northern land but resistance is severe and stability is low, unless route identity explicitly accepts coercion.
