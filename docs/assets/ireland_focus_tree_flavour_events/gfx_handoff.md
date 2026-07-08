# Ireland Focus Tree Flavour Report GFX Handoff

Asset subagent handoff only. Do not treat this as a `.gfx` edit.

Suggested target `.gfx` file: `interface/ireland_focus_tree.gfx`, or the existing event-picture registry if the main implementation has already created one.

Ready-to-copy pattern:

```txt
spriteType = {
	name = "GFX_flavour_report_civic_life"
	texturefile = "gfx/event_pictures/ireland_focus_tree/flavour_report_civic_life.dds"
}
```

| Proposed sprite | Final DDS | Shared flavour pools | Size |
| --- | --- | --- | --- |
| `GFX_flavour_report_civic_life` | `gfx/event_pictures/ireland_focus_tree/flavour_report_civic_life.dds` | civic administration, councils, petitions | 210x176 |
| `GFX_flavour_report_press_radio` | `gfx/event_pictures/ireland_focus_tree/flavour_report_press_radio.dds` | press, radio, censorship, public information | 210x176 |
| `GFX_flavour_report_language_school` | `gfx/event_pictures/ireland_focus_tree/flavour_report_language_school.dds` | schools, language, folklore, civic culture | 210x176 |
| `GFX_flavour_report_turf_rationing` | `gfx/event_pictures/ireland_focus_tree/flavour_report_turf_rationing.dds` | turf, rationing, coupons, winter heat | 210x176 |
| `GFX_flavour_report_rural_industry` | `gfx/event_pictures/ireland_focus_tree/flavour_report_rural_industry.dds` | sugar beet, creameries, mills, workshops | 210x176 |
| `GFX_flavour_report_power_transport` | `gfx/event_pictures/ireland_focus_tree/flavour_report_power_transport.dds` | Ardnacrusha-adjacent maintenance, rail, bus fuel, transport | 210x176 |
| `GFX_flavour_report_ports_coast` | `gfx/event_pictures/ireland_focus_tree/flavour_report_ports_coast.dds` | ports, coast posts, fishermen, merchant marine | 210x176 |
| `GFX_flavour_report_civil_defence` | `gfx/event_pictures/ireland_focus_tree/flavour_report_civil_defence.dds` | ARP, blackout, civil defence, LDF drills | 210x176 |
| `GFX_flavour_report_g2_internment` | `gfx/event_pictures/ireland_focus_tree/flavour_report_g2_internment.dds` | G2, internment, wireless checks, crash salvage | 210x176 |
| `GFX_flavour_report_border_life` | `gfx/event_pictures/ireland_focus_tree/flavour_report_border_life.dds` | border markets, customs, rail crossings, safeguards | 210x176 |
| `GFX_flavour_report_relief` | `gfx/event_pictures/ireland_focus_tree/flavour_report_relief.dds` | relief, first aid, parcels, postwar aid | 210x176 |

Use notes:

- All flavour assets are shared family images, not unique one-row event illustrations.
- All final files use the report-event 210x176 treatment with transparent corners.
- `flavour_report_relief` intentionally avoids the Red Cross emblem; use it for generic relief unless sourced emblem approval is added later.
- No `.gfx`, gameplay, localisation, focus, decision, or spec files were edited by this asset pass.
