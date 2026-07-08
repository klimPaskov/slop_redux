# Slop Redux Dynamic Helpers

## Ireland Focus Tree Helpers

### `slopx_ireland_initialize_mechanics`

Scope: country.

Purpose: initializes the Ireland focus tree pressure variables, ledger ideas, and dynamic modifier. It is called from Irish history and from `on_daily_IRE` as a safe initializer.

Inputs: none.

Outputs: sets `ireland_constitutional_authority`, `ireland_emergency_preparedness`, `ireland_partition_pressure`, `ireland_foreign_access_pressure`, `ireland_hidden_reveal_stage`, `ireland_northern_integration_stage`, and supporting readiness variables.

Side effects: adds the Ireland ledger ideas and the `slopx_ireland_mechanics_dynamic_modifier`.

Example:

```hoi4
slopx_ireland_initialize_mechanics = yes
```

### `slopx_ireland_update_mechanics_modifier`

Scope: country.

Purpose: clamps the four public pressure values, derives dynamic modifier variables, and refreshes the country modifier.

Inputs: existing Ireland pressure variables.

Outputs: updates `ireland_dynamic_political_power_factor`, `ireland_dynamic_stability_factor`, `ireland_dynamic_war_support_factor`, `ireland_dynamic_army_defence_factor`, `ireland_dynamic_factory_output_factor`, and `ireland_dynamic_consumer_goods_factor`.

Side effects: calls `force_update_dynamic_modifier = yes`.

Example:

```hoi4
slopx_ireland_update_mechanics_modifier = yes
```

### Route and Mechanic Delta Helpers

Scope: country.

Purpose: centralize small and medium changes to Constitutional Authority, Emergency Preparedness, Partition Pressure, and Foreign Access Pressure.

Helpers:

- `slopx_ireland_gain_authority_small`
- `slopx_ireland_gain_authority_medium`
- `slopx_ireland_lose_authority_small`
- `slopx_ireland_gain_preparedness_small`
- `slopx_ireland_gain_preparedness_medium`
- `slopx_ireland_reduce_partition_pressure_small`
- `slopx_ireland_raise_partition_pressure_small`
- `slopx_ireland_reduce_foreign_access_small`
- `slopx_ireland_raise_foreign_access_small`

Inputs: none.

Outputs: updates the appropriate pressure variable and refreshes the dynamic modifier.

Example:

```hoi4
slopx_ireland_reduce_foreign_access_small = yes
```

### Focus Family Helpers

Scope: country.

Purpose: keep the large Ireland focus tree readable by grouping repeated reward structures for public routes, support lanes, and hidden branches.

Helpers:

- `slopx_ireland_opening_focus_effect`
- `slopx_ireland_historical_focus_effect`
- `slopx_ireland_constitutional_focus_effect`
- `slopx_ireland_labour_focus_effect`
- `slopx_ireland_blueshirt_focus_effect`
- `slopx_ireland_ira_focus_effect`
- `slopx_ireland_industry_power_project`
- `slopx_ireland_industry_ports_project`
- `slopx_ireland_industry_rural_project`
- `slopx_ireland_industry_stores_project`
- `slopx_ireland_military_regular_effect`
- `slopx_ireland_military_coast_effect`
- `slopx_ireland_military_air_naval_effect`
- `slopx_ireland_diplomacy_neutral_effect`
- `slopx_ireland_diplomacy_sponsor_effect`
- `slopx_ireland_northern_preparation_effect`
- `slopx_ireland_northern_escalation_effect`

Side effects: these helpers may add state buildings, research bonuses, readiness variables, opinion modifiers, or pressure changes.

### Northern Settlement Helpers

Scope: country.

Purpose: enforce the rule that all-island identity changes are focus-prepared and decision-verified.

Helpers:

- `slopx_ireland_prepare_all_island_settlement`
- `slopx_ireland_complete_all_island_settlement`
- `slopx_ireland_advance_northern_integration`

Inputs: state control and pressure triggers from `slopx_ireland_triggers.txt`.

Outputs: prepares or proclaims the settlement, applies the all-island cosmetic tag, advances integration stages, and adds the Irish core on state `119` only after the final integration trigger passes.

### Hidden Path Reveal Helpers

Scope: country.

Purpose: reveal hidden content only when route conditions and public pressure values justify it.

Helpers:

- `slopx_ireland_reveal_civic_hidden_path`
- `slopx_ireland_reveal_directorate_hidden_path`
- `slopx_ireland_reveal_atlantic_hidden_path`
- `slopx_ireland_reveal_common_platform_hidden_path`
- `slopx_ireland_trigger_corrupted_restoration_failure`
- `slopx_ireland_hidden_civic_focus_effect`
- `slopx_ireland_hidden_directorate_focus_effect`
- `slopx_ireland_hidden_atlantic_focus_effect`
- `slopx_ireland_hidden_common_platform_focus_effect`

Side effects: sets hidden reveal flags, achievement hooks, and pressure adjustments.

## Ireland Major Event Layer

### `slopx_ireland_major_event_pulse`

Purpose: Ireland-only daily pulse called from `on_daily_IRE`. It schedules the hidden major-event maintenance root after the cleanup cooldown expires. Visible major route events use event `trigger` + `mean_time_to_happen` gates, so this pulse does not crowd out route events.

Scope: `IRE` country scope.

Side effects: schedules `slopx_ireland_focus.131`, which dispatches hidden cleanup, reveal, integration, and achievement checks when their focus, pressure, state-control, or route flags are already valid.

### `slopx_ireland_major_event_set_cooldown`

Purpose: shared cooldown and counter hook for visible major events.

Scope: `IRE` country scope.

Side effects: sets `ireland_major_event_cooldown` for the configured event spacing and increments `ireland_major_events_seen`.

### `slopx_ireland_major_cleanup_set_cooldown`

Purpose: shared cooldown hook for the hidden maintenance root.

Scope: `IRE` country scope.

Side effects: sets `ireland_major_cleanup_cooldown` for the configured cleanup spacing.

### `slopx_ireland_major_*_effect`

Purpose: reusable major-event payload helpers for authority reassurance, security readiness, sovereignty review, pressure warnings, Northern reassurance/alarm, civic hidden rewards, and directorate rewards.

Scope: `IRE` country scope.

Side effects: adjusts Constitutional Authority, Emergency Preparedness, Partition Pressure, Foreign Access Pressure, and route-specific BOP sides through the existing Ireland mechanic helpers.

## Ireland Flavour Event Layer

### `slopx_ireland_flavour_pulse`

Purpose: country-scoped Ireland-only pulse called from `on_daily_IRE`. It schedules the hidden flavour dispatcher only when Ireland mechanics are initialized and the global flavour cooldown has expired.

Scope: `IRE` country scope.

Side effects: schedules `slopx_ireland_flavour.1`, which picks row-level flavour events from the canonical catalogue.

### `slopx_ireland_flavour_set_cooldown`

Purpose: applies the global flavour cooldown after any row-level flavour event fires and increments `ireland_flavour_events_seen`.

Scope: `IRE` country scope.

Side effects: sets `ireland_flavour_global_cooldown` for 60 days in calm periods or 45 days while at war.

### `slopx_ireland_flavour_open_<family>_task`

Purpose: opens the matching local task decision for a flavour family. Families are `civic`, `media`, `culture`, `ports`, `supply`, `agriculture`, `industry`, `defence`, `northern`, `political`, `foreign`, `hidden`, and `late`.

Scope: `IRE` country scope.

Side effects: sets `ireland_flavour_task_visible`, the family task active flag, and increments the family task pressure variable.

### `slopx_ireland_flavour_<family>_support_effect` / `slopx_ireland_flavour_<family>_restraint_effect`

Purpose: centralized family payloads for row-level flavour choices. Support effects usually invest in the local file; restraint effects keep the response narrower while leaving a route-specific pressure memory.

Scope: `IRE` country scope.

Side effects: updates Constitutional Authority, Emergency Preparedness, Partition Pressure, Foreign Access Pressure, BOP sides, local readiness variables, route memory flags, or hidden-path cleanup depending on the family.

### `slopx_ireland_flavour_<family>_task_success_effect` / `slopx_ireland_flavour_<family>_task_cancel_effect`

Purpose: cleanup and payoff hooks for `ireland_flavour_<family>_local_task` timed decisions.

Scope: `IRE` country scope.

Side effects: clears the active family task flag, records task completion/failure variables, and applies the corresponding support/restraint family effect.
