# Ireland focus tree lane map

This is the applied route architecture and coordinate envelope for `slopx_ireland_focus_tree`. Working labels remain internal handles. Machine-readable branch, lane, convergence, visibility, AI-route, and pin metadata is stored beside the source in `common/national_focus/ireland_focus_tree.focus-plan.json`.

## Route architecture

```text
Opening constitutional trunk
  constitution, public order, presidency, civil war wounds, ports

Political fork
  historical sovereign neutrality
    strict neutral watchtower side lane
    Emergency cabinet and active neutrality convergence
  constitutional opposition
    guarded Commonwealth cooperation
    anti-dependency and Northern safeguards
  Labour
    democratic social reform
    social republic rare branch
    Northern labour settlement
  Blueshirt corporatist Ireland
    National Guard consolidation
    corporatist chamber
    Spanish and Italian contact side lane
  IRA underground republic
    safehouse network
    German contact risk lane
    Northern uprising and civil authority conversion

Support lanes
  industry and supply
    native factories, Shannon grid, sugar beet, turf, rail, ports
  military and Emergency defence
    G2, LDF, coastal watch, air defence, reserves, garrisons
  diplomacy and neutrality
    recognition, access rules, diaspora, anti-dependency, sponsor limits
  Northern settlement
    surveys, committees, observers, incidents, uprising, integration
  late-game ambition
    Atlantic compact, postwar arbitration, all-island consolidation
```

Support lanes remain reachable from compatible political routes while route-locked actions stay near their political parent. Northern settlement is positioned between diplomacy and military because it draws from both. Late-game ambition converges only after route institutions, Emergency defence, and partition handling are established.

## Applied lane geometry

| Order | Lane | Horizontal bounds | Role |
| ---: | --- | ---: | --- |
| 0 | Historical route | -15 to -10 | Sovereign-neutral political branch |
| 1 | Opposition route | -8 to -5 | Constitutional/Commonwealth branch |
| 2 | Constitutional trunk | -1 to 1 | Shared opening and route locks |
| 3 | Labour route | -1 to 1 | Labour and social-republic branch |
| 4 | Blueshirt route | 5 to 7 | Corporatist branch |
| 5 | IRA route | 11 to 14 | Underground-republic branch |
| 6 | Support gateway | 15 | Shared handoff to support systems |
| 7 | Diplomacy | 19 to 38 | Neutrality, foreign relations, civic and Atlantic hidden routes |
| 8 | Late convergence | 42 | Route-mastery convergence |
| 9 | Industry and supply | 43 to 48 | Industry, fuel, ports, stores, and transport |
| 10 | Northern settlement | 53 to 59 | Settlement, pressure, integration, and failure handling |
| 11 | Military and Emergency | 60 to 73 | Defence, intelligence, air/naval preparation, and directorate route |

The compiled tree spans x = -15 through 73 and y = 0 through 41. Sixteen deliberate anchors define the trunk, five political entries, support roots, late support milestones, and final convergence. The remaining 222 nodes were laid out from prerequisite, mutual-exclusion, branch, and lane constraints. `continuous_focus_position` is `{ x = 50 y = 2000 }`.

## Route coverage

| Branch group | Focuses | Coverage status | Placement note |
| --- | ---: | --- | --- |
| Opening and constitutional trunk | 18 | Complete | Shared vertical trunk and support gateway |
| Historical neutrality | 18 | Complete | Left political fan |
| Constitutional opposition | 18 | Complete | Left-centre political fan |
| Labour social republic | 19 | Complete | Centre political fan |
| Blueshirt corporatism | 19 | Complete | Right-centre political fan |
| IRA republic | 20 | Complete | Right political fan |
| Diplomacy and neutrality | 23 | Complete | First support family after the gateway |
| Hidden civic restoration | 10 | Complete | Tucked under its diplomacy parent |
| Hidden Atlantic compact | 7 | Complete | Tucked under late diplomacy |
| Industry and supply | 22 | Complete | Between convergence and Northern work |
| Military and Emergency defence | 27 | Complete | Rightmost support family |
| Hidden Emergency directorate | 7 | Complete | Tucked under military/Emergency work |
| Northern settlement | 29 | Complete | Between diplomacy and military |
| Late route mastery | 1 | Complete | Explicit convergence gate |

## MCP transaction evidence

The retained layout was applied by public `hoi4-agent-tools@0.1.7` transaction `txn_9f1ad0a1-e100-4377-acc3-29db5d244053` with plan hash `6f73d55afe2175b95f15cdafd6c7b42fe2b9d01b9281a46a5098ff34617ce770` and layout hash `1f27c4d2ccbf158482c04b3ba9e5b0fb3f37f11cf5892633cd8180e70059a832`.

- Baseline source SHA-256: `892b4adec65f96b35eb6709f2ab429e36c3f5573b267538594aba46ef258b006`.
- Applied source SHA-256: `af640f84c9e2438ba3d546c923d3e6af0b72fc6d14e2817c49016dc72ee6f47a`.
- Planning sidecar SHA-256: `26336a2417507f5151dd0be2de59247d947db3053f5fc97fb746ad4e7d7bfd30`.
- A first published-package apply passed post-write validation; rollback restored the exact baseline source hash and removed the new sidecar. A fresh dry run reproduced all 14 non-manifest artifacts byte-for-byte before the retained apply.
- Source and semantic projections are identical after normalising only focus `x`/`y` and `continuous_focus_position`. Prerequisites, exclusions, rewards, triggers, comments, unknown fields, raw blocks, ordering, encoding, and all other source text are preserved.
- All 238 focus IDs and coordinates are unique. There are no parent-order violations, connector-crossing diagnostics, errors, or blockers.
- Symbolic costs remain 4 short, 215 standard, and 19 long.
- The baseline reported 15 avoidable crossings. The retained layout reports none.
- The deterministic review render uses `reviewScale: 0.4`, is 6317 by 1997 pixels, and has PNG SHA-256 `93e60509ee176eea10594762519cacb31fa32e717a7465d5cdbf6e61cfce108d`.

## Remaining nonblocking design findings

The final complete lint resource contains 116 `FOCUS_REPEATED_GENERIC_REWARD` warnings inherited from the gameplay design. This pass deliberately changed layout metadata and coordinates only; rewards, balance, AI behavior, localisation, icons, prerequisites, and route semantics were not rewritten. The broad 88-column canvas and several long support-gateway connectors are retained because they keep all branches distinct and eliminate crossings without changing gameplay structure.
