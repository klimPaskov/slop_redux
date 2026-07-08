# Ireland BOP spec part 5, acceptance and handoffs

## Implementation acceptance standard

The BOP addendum is complete only when the implementation includes a working BOP definition, active side pair initialization, route mode switching, BOP range effects, route decisions, route AI, cleanup helpers, localisation direction converted into final text by the implementation agent, and documentation aligned with the existing Ireland implementation.

## Required gameplay evidence

| Surface | Required evidence |
| --- | --- |
| BOP definition | one Ireland BOP object with route relevant sides and ranges |
| route initialization | opening mode starts and route lock focuses switch active mode |
| focus integration | major route focuses move BOP or require BOP bands where planned |
| decision integration | route BOP decisions exist with concrete costs and failures |
| mission integration | timed BOP missions require real objectives or resources |
| idea lifecycle | existing Ireland idea families read or react to BOP without idea spam |
| AI | every Ireland route has preferred bands and recovery logic |
| hidden paths | hidden path reveal and disqualifier rules read BOP bands where planned |
| Northern settlement | BOP affects legitimacy and coercion but does not replace state control checks |
| foreign pressure | sponsor influence affects BOP through decisions and crises, not clean free support |
| assets | BOP side icons, warning icons, and optional animated warning assets have source modes and handoffs |
| achievements | BOP mastery achievements have tracking and disqualifiers |
| docs | existing Ireland docs mention the BOP as a post implementation improvement |

## Anti bloat rules

Do not implement multiple simultaneous Ireland BOPs unless the UI has been tested and the user approves the larger surface.

Do not build a full custom GUI for the BOP. The vanilla BOP surface plus decision category headers and idea tooltips are enough. The Emergency board remains the only major scripted GUI from the canonical package.

Do not add seven new national spirits for each mode. Use staged idea families and scripted localisation.

Do not turn BOP decisions into a store. Every important BOP decision needs a concrete action, cost, state objective, crisis consequence, or route tradeoff.

Do not write unresearched slogans, route mottos, quotes, or audio cues for BOP bands.

## Prompt alignment

The coding prompt, decision prompt, asset prompt, achievement prompt, and goal prompt in this package are updated to treat the canonical Ireland focus tree as implemented. They ask the implementer to patch the existing implementation, not rebuild it.

## Final package note

This addendum has no continuation prompt. The only procedural limitation is the unavailable improvement loop subagent in this chat environment. The ready improvement loop prompt is included for the target implementation environment.
