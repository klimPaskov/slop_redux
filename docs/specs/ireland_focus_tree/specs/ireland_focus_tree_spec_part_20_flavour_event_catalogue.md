# Ireland focus tree spec part 20, flavour event catalogue

## Catalogue authority

This file is the catalogue guide for the mandatory flavour event layer. The row level source is `matrices/ireland_focus_tree_flavour_event_catalogue_matrix.md`, which contains 169 working flavour event handles. The matrix is canonical. Implementation may merge handles into dynamic events only when the final report proves that the historical anchor, trigger family, route variant, gameplay effect, AI behavior, asset need, and cleanup survive.

Working handles are internal labels. They are not final localisation.

## Family coverage

| Family | Working handle count | Required gameplay role |
| --- | --- | --- |
| Agriculture, sugar, creameries, and rural industry | 12 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Constitutional civic life | 12 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Defence, LDF, G2, and civil protection | 14 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Emergency supply, rationing, and turf | 14 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Foreign legations, diaspora, Church, and humanitarian | 14 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Hidden path civic and security signs | 14 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Industry, electrification, aviation, and transport | 12 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Language, folklore, and schools | 12 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Late game, reunification, and postwar memory | 12 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Northern border and community life | 14 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Political route ambience with effects | 15 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Ports, coasts, and merchant marine | 12 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |
| Press, radio, and public information | 12 | Implement as state, country, report, hidden, or dynamic variants with real mechanic effects and route weighting. |

## Catalogue implementation rule

Every working handle in the matrix requires one of four dispositions in the final implementation report.

| Disposition | Meaning | Evidence |
| --- | --- | --- |
| final event | The handle has a final event id. | event id, trigger, options, localisation keys, effect package, AI chance, cleanup. |
| dynamic variant | The handle is a variant inside a shared event family. | base event id, variant trigger, variant effect, dynamic localisation keys, cleanup. |
| mission or decision result | The handle is implemented as a decision or mission event. | decision or mission id, event id, success and failure handling. |
| rejected with reason | The handle is cut because another implemented row carries the same role. | replacement id, effect comparison, lost content assessment. |

A generic event with similar mood is not enough. The row needs preserved historical background and gameplay consequence.

## Required implementation table

| Working flavour handle | Final event or variant | Trigger source | Historical anchor | Effect package | AI behavior | Asset or text gate | Cleanup | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |

The implementation table should be stored with the final completion report or feature documentation. It should not be a loose scratch note.

## Catalogue use by event files

Use separate or clearly grouped event file sections for civic, media and culture, Emergency home front, ports and industry, Northern local life, route micro flavour, and hidden or late flavour. Final filenames can follow the repository pattern, but the implementation must remain traceable from the matrix.

## Merge guidance

Merging is allowed for repeated household, local council, border, and state mission patterns. Merging is not allowed when it erases route identity. A Labour relief event, a Blueshirt public order event, an IRA exposure event, and a historical Emergency administration event cannot become one generic stability popup.

## Mandatory effect rule

Every row must affect play. Valid payloads include BOP movement, Constitutional Authority, Emergency Preparedness, Partition Pressure, Foreign Access Pressure, local support, worker support, church trust, food security, fuel strain, coastwatch readiness, shipping capacity, state modifiers, decision costs, mission timers, idea lifecycle, AI strategy memory, achievement memory, and cleanup.

Empty ambience popups fail the package.
