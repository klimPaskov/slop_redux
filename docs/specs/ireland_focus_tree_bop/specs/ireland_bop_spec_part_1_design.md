# Ireland BOP spec part 1, design model

## Playable promise

Ireland should feel like a state whose authority is always being argued over. The focus tree already tracks Constitutional Authority, Emergency Preparedness, Partition Pressure, and Foreign Access Pressure. The BOP turns the internal authority question into a visible central struggle that the player reads every few focuses and every major crisis.

The BOP should make constitutional politics, emergency government, Labour pressure, Blueshirt organization, IRA control, and hidden route pressure legible without flattening them into one stability score.

## Relationship with the canonical implementation

The BOP improves the implementation. It does not replace any canonical mechanic.

| Existing canonical surface | BOP relationship |
| --- | --- |
| Constitutional Authority | BOP is the visible struggle layer and can read or alter authority components. |
| Emergency Preparedness | BOP can shift toward emergency command when preparedness and war pressure rise. Preparedness remains the defence system. |
| Partition Pressure | BOP affects which settlement tools are legitimate or coercive. Partition Pressure remains the Northern objective system. |
| Foreign Access Pressure | BOP affects how domestic actors react to foreign pressure. Sponsor pressure remains tracked separately. |
| Hidden paths | BOP bands become reveal gates, disqualifiers, and crisis entry conditions. |
| Focus routes | Route locks initialize the active BOP mode and set the visible side pair. |
| Decision categories | Decisions should alter BOP through concrete actions, not cheap political power clicks. |

## BOP structure ruling

Use one Ireland BOP object with multiple possible sides. Only one pair should be visible at a time. The active pair changes when Ireland commits to a route or enters a hidden crisis route.

Recommended BOP id: `IRE_state_authority_bop`.

Recommended implementation rule: negative values favor the first visible side, positive values favor the second visible side. Keep the exact sign consistent across effects, tooltips, and scripted localisation.

The BOP can contain more than two sides, but the player should see only the active pair. Do not make the player manage three or four sides at once through the BOP UI. The other mechanics already carry the extra values.

## Initialization

Initialize the BOP when Ireland enters the opening constitutional trunk. If the implementation already starts Constitutional Authority on game start, the BOP can start on game start as well.

Opening mode: `ire_bop_mode_opening_state`.

Opening side pair:

- `ire_bop_side_constitutional_government`
- `ire_bop_side_armed_political_pressure`

Starting value should be mildly on the constitutional side, not fully secure. The state has institutions, but the tree begins with real extra constitutional pressure.

## Mode transition philosophy

Route locks should switch the active visible side pair. The BOP value should not reset blindly. The transition should translate the old value into a sensible starting point for the new mode.

Examples:

- A stable constitutional opening gives the historical and opposition modes stronger civilian starting control.
- High armed pressure gives the IRA and Blueshirt modes stronger challenger starting control.
- High Emergency Preparedness and low Constitutional Authority give the Emergency Directorate route stronger security starting control.
- High foreign dependency should not directly move the BOP by itself. It should unlock decisions or crises that move domestic actors.

## What the BOP should change

The BOP should affect visible play through these surfaces:

- route availability and route crisis gates
- decision cost and success chance direction
- mission duration and failure risk direction
- leader, advisor, and cabinet unlock safety
- hidden route reveal conditions
- Northern settlement legitimacy or coercion
- foreign trust and sponsor vulnerability
- Emergency Directorate entry and recovery
- AI route weights and crisis restraint
- achievement tracking

The BOP should not grant repeated tiny modifiers. Its bands can contain modifiers, but each band should also unlock, block, or alter real gameplay.

## Range philosophy

Use seven bands per active mode:

| Working band | Value direction | Meaning |
| --- | --- | --- |
| `left_extreme` | strong first side | first side controls state practice and can overreach |
| `left_high` | clear first side | first side directs policy with manageable opposition |
| `left_moderate` | first side advantage | first side has momentum but needs maintenance |
| `center_contested` | middle | route flexibility and uncertain authority |
| `right_moderate` | second side advantage | challenger has momentum but not control |
| `right_high` | clear second side | challenger directs policy and creates crisis risk |
| `right_extreme` | strong second side | second side can force takeover or collapse |

Exact thresholds should be constants. Suggested thresholds are 75, 45, and 15 on each side, but implementation may adjust after testing.

## Center should matter

The center is not a dead zone. It should provide route flexibility, but it should also make decisive actions harder. A country with contested authority should need extra missions, public work, or internal deals before it can take major Northern or foreign gambles.

## Side overreach rule

A side that wins too completely should create a problem. Constitutional overcentralization can slow emergency action or radicalize opposition. Emergency control can save the state but threaten democracy. Labour congress power can deliver reforms but strain production and church relations. Blueshirt guard control can mobilize cadres but risks civil authority collapse. Army Council control can pursue republican war aims but invites foreign compromise and British action.

## Historical route rule

Historical neutrality should be active. It should keep the BOP between civilian cabinet and emergency apparatus after the opening. The player should use emergency powers without allowing the security apparatus to become the state.

## Alternate route rule

Alternate paths should use the BOP to show their internal tension. The BOP must not make Fine Gael and Blueshirt politics the same path. It must not make Labour only a Soviet path. It must not make IRA foreign contact clean or safe.
