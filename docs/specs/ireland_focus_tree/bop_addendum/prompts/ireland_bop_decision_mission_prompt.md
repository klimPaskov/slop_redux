# Ireland BOP decision and mission prompt

Use this prompt with the decision and mission implementation skill or subagent after the core BOP object exists.

Task: implement or audit Ireland BOP decision and mission families for `ireland_focus_tree_bop`.

Read:

- `specs/ireland_bop_spec_part_3_focus_decision_integration.md`
- `matrices/ireland_bop_decision_matrix.md`
- `implementation/ireland_bop_id_registry.md`
- the existing Ireland decision files and scripted helpers
- `hoi4-decisions-missions`
- `AGENTS.md`

Rules:

- BOP decisions must represent real political or military actions.
- Avoid a store of political power purchases.
- Use concrete costs and requirements such as equipment, manpower, command power, army XP, factory output, local support, stability floor, supplied divisions, convoys, fuel, trains, and deadlines.
- Important BOP missions must require active work such as keeping order in named city groups, guarding ports, maintaining production, disciplining guards, controlling safehouses, or restoring civilian rule.
- Every important decision family needs success, failure, partial failure where useful, AI behavior, route validity, cleanup, and readable cost localisation direction.
- Use phased visibility. Opening decisions appear early, route decisions appear after mode switch, crisis decisions appear only in high or extreme bands, recovery decisions appear after failure or directorate entry.
- Northern settlement decisions may read BOP legitimacy, but state control and integration remain verified by the canonical settlement system.

Required families:

- public confidence session
- reconciliation board
- emergency order review
- coast security transfer
- anti basing vote
- defence liaison mission
- congress mandate vote
- worker production truce
- guard discipline review
- cadre mobilisation
- civilian front conference
- Army Council mandate
- civic institution drive
- public cultural mobilisation
- civilian rule timetable

After implementation or audit, write a handoff listing changed files, decision ids, mission ids, BOP helper calls, AI behavior, cleanup checks, localisation keys, validation performed, and remaining risks.
