# Ireland BOP addendum package manifest

Package name: `ireland_focus_tree_bop_addendum_package.zip`

Package role: separate implementation addendum for a comprehensive Ireland Balance of Power system.

## Files

| Path | Role |
| --- | --- |
| `README.md` | package overview |
| `ireland_bop_planning_state.md` | current state and source of truth |
| `specs/ireland_bop_spec_part_1_design.md` | BOP design model |
| `specs/ireland_bop_spec_part_2_modes_and_ranges.md` | BOP modes and ranges |
| `specs/ireland_bop_spec_part_3_focus_decision_integration.md` | focus, decision, mission, hidden path integration |
| `specs/ireland_bop_spec_part_4_ai_and_cleanup.md` | AI, crises, cleanup, validation |
| `specs/ireland_bop_spec_part_5_acceptance_handoffs.md` | acceptance standard and anti bloat rules |
| `implementation/ireland_bop_file_surface_map.md` | likely file surfaces |
| `implementation/ireland_bop_id_registry.md` | suggested ids and helpers |
| `matrices/ireland_bop_mode_matrix.md` | mode summary |
| `matrices/ireland_bop_range_matrix.md` | range summary |
| `matrices/ireland_bop_focus_integration_matrix.md` | focus hook summary |
| `matrices/ireland_bop_decision_matrix.md` | decision and mission summary |
| `matrices/ireland_bop_ai_matrix.md` | AI behavior summary |
| `matrices/ireland_bop_asset_matrix.md` | asset needs |
| `matrices/ireland_bop_achievement_matrix.md` | achievement hooks |
| `research/ireland_bop_research_notes.md` | design research notes |
| `research/ireland_bop_bibliography.md` | source list |
| `prompts/ireland_bop_coding_prompt.md` | implementation prompt |
| `prompts/ireland_bop_decision_mission_prompt.md` | decision prompt |
| `prompts/ireland_bop_asset_prompt.md` | asset prompt |
| `prompts/ireland_bop_achievement_prompt.md` | achievement prompt |
| `prompts/ireland_bop_goal_prompt.md` | short goal prompt |
| `prompts/ireland_bop_improvement_loop_prompt.md` | improvement loop prompt |
| `plans/ireland_bop_improvement_loop_blocker.md` | subagent blocker note |
| `reports/ireland_bop_implementation_readiness_report.md` | readiness report |
| `package_checksums.sha256` | checksums generated after packaging |

## Validation before zip

- no temporary continuation prompt is included
- no em dash characters are present
- no semicolon characters are present
- goal prompt length is under 4000 characters
- package includes all prompt and matrix files needed for implementation
