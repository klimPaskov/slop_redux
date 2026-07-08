# Ireland focus tree spec part 12, balance of power

## Canonical ruling

The Ireland BOP is now part of the canonical package. It is not a replacement for the implemented focus tree and it is not a replacement for Constitutional Authority, Emergency Preparedness, Partition Pressure, or Foreign Access Pressure. It is a visible internal authority layer that reads those systems and lets the player see which domestic institution has the initiative.

The full detailed BOP addendum is included under `bop_addendum/`. The canonical matrices are copied into `matrices/` with the `ireland_focus_tree_bop_` prefix. The implementation agent should treat this part as the source link between the already implemented focus tree and the BOP addendum.

## BOP object and active modes

Recommended BOP id: `IRE_state_authority_bop`.

Use one Ireland BOP object with route specific active side pairs. Only one pair should be visible at a time. Route locks, hidden reveals, crisis branches, and recovery states switch the active pair and translate the old value into the new mode instead of resetting it.

| Mode | Visible first side | Visible second side | Used by | Gameplay question |
| --- | --- | --- | --- | --- |
| `ire_bop_mode_opening_state` | constitutional government | armed political pressure | opening trunk | Can politics stay inside the law. |
| `ire_bop_mode_historical_emergency` | civilian cabinet | emergency apparatus | historical neutrality and strict neutral route | Can Emergency powers defend neutrality without becoming permanent rule. |
| `ire_bop_mode_commonwealth_cooperation` | independent parliamentary review | defence liaison cabinet | constitutional opposition and guarded cooperation | Can British cooperation remain a bargain instead of dependency. |
| `ire_bop_mode_labour_republic` | Dáil Labour cabinet | workers congress | Labour democratic and social republic routes | Can reform power expand without losing constitutional control. |
| `ire_bop_mode_blueshirt_corporate` | parliamentary right and chambers | Blueshirt guard | corporatist route | Does the right govern through institutions or a uniformed movement. |
| `ire_bop_mode_republican_underground` | civilian republican front | Army Council | IRA route and reconciliation overlay | Does republican policy stay political or become military command. |
| `ire_bop_mode_civic_cultural` | civic institutions | cultural mobilisation networks | hidden civic cultural restoration | Can cultural renewal remain inclusive and constitutional. |
| `ire_bop_mode_emergency_directorate` | civilian restoration | security directorate | hidden Emergency Directorate | Does emergency rule return power or keep it. |

## Focus integration

Opening trunk focuses initialize the BOP and teach the player that authority is contested. Route lock focuses switch the visible side pair. Support branches alter the active BOP through concrete effects rather than flat drift.

Historical neutrality should use the BOP to keep tension between cabinet authority and emergency apparatus. The player should want enough security control to defend ports, coast watching, G2, and the LDF, but not so much that the Emergency Directorate path becomes easy.

Fine Gael constitutional opposition should use the BOP to separate legal parliamentary review from defence liaison dependence. A high liaison side helps cooperation but damages sovereign neutrality and raises Foreign Access Pressure.

Labour uses the BOP to separate a Dáil led social republic from a workers congress that can outgrow parliament. This preserves democratic socialism while allowing radical pressure and foreign dependency risk.

Blueshirts use the BOP to separate parliamentary corporatist chambers from Blueshirt guard control. This keeps the non O'Duffy corporate route distinct from street movement capture.

The IRA route uses the BOP to separate a civilian republican front from Army Council command. German contact, courier exposure, sabotage, and Plan Kathleen style material should move toward military command and crisis.

## Decision and mission integration

BOP movement must come from actions the player understands. Public order missions, amnesty, port defence, LDF training, strike arbitration, chamber legality votes, safehouse raids, courier interception, Northern observer missions, and restoration deadlines should move the BOP.

Do not build BOP decisions as a political power store. Use mission objectives, equipment, supplied divisions, local support, legitimacy, foreign access, trains, convoys, manpower, XP, and time pressure where the relevant route calls for those costs.

## Event integration

The event suite in part 13 must fire when BOP modes switch, when a side reaches a dangerous band, and when a side overreaches. These events should not only report a number. They should create choices, missions, or visible consequences.

BOP events should cover contested opening authority, emergency overreach, liaison dependency, Labour congress pressure, Blueshirt guard escalation, Army Council capture, civic route corruption, and security directorate restoration.

## Acceptance rules

- Every BOP mode has range effects, focus hooks, decisions or missions, AI behavior, localisation direction, and cleanup.
- BOP bands unlock or block content, change mission risk, alter decision availability, affect hidden route reveal, or trigger events.
- BOP values never replace the four main mechanics.
- BOP thresholds and weights are centralized in constants or documented tuning helpers.
- AI never pushes a route into a crisis band unless route logic, war state, ideology, and survival pressure justify it.
- The implementation report must show how each focus route initializes and uses the BOP.
