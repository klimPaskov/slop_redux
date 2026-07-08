# Ireland BOP implementation file surface map

This file names likely implementation surfaces. The implementer must inspect the existing Slop Redux repository before editing and follow existing naming and folder patterns when they differ from these suggested paths.

## Core script surfaces

| Path | Purpose |
| --- | --- |
| `common/bop/ireland_balance_of_power.txt` | Define the Ireland BOP object, sides, ranges, and range modifiers. |
| `common/scripted_effects/ireland_bop_effects.txt` | Initialize BOP, switch modes, translate values, apply route shifts, and cleanup stale state. |
| `common/scripted_triggers/ireland_bop_triggers.txt` | Shared BOP mode, band, route, and safety checks. |
| `common/script_constants/ireland_bop_constants.txt` | Thresholds, shift values, AI weights, cooldown bands, and crisis thresholds. |
| `common/scripted_localisation/ireland_bop_scripted_loc.txt` | Dynamic BOP band, mode, recent cause, and action direction text. |
| `common/decisions/ireland_bop_decisions.txt` | BOP decision families and route crisis missions. |
| `common/decisions/categories/ireland_bop_decision_categories.txt` | Category hooks only if the existing implementation does not already have a suitable Ireland internal politics category. |

## Existing Ireland surfaces to patch

| Surface | Expected patch |
| --- | --- |
| Ireland national focus file | Add BOP initialization, route mode switches, route checks, and major focus shifts. |
| Ireland decision files | Add BOP decisions and link existing Constitutional Authority, Emergency, foreign access, and Partition decisions to BOP where planned. |
| Ireland idea files | Add BOP dependent tooltip and staged idea effects where needed. |
| Ireland AI strategy files | Add route band preferences, crisis recovery, and invalid blockers. |
| Ireland event suite | Add BOP crisis events and hidden recovery events for every implemented BOP mode and recovery path. |
| Ireland localisation files | Add final player facing BOP text from direction. Do not paste working labels. |
| Ireland scripted GUI if present | Only add BOP warning or cross references. Do not replace Emergency board. |
| Ireland docs | Record the BOP as a post implementation addendum. |

## Asset surfaces

| Path | Purpose |
| --- | --- |
| `gfx/interface/bop/ireland_focus_tree_bop/` | Suggested final DDS folder for BOP side icons and range warning assets. |
| `interface/ireland_bop.gfx` | Suggested sprite definitions if no existing Ireland interface file owns BOP sprites. |
| `docs/assets/ireland_focus_tree_bop/manifest.md` | Asset manifest for side icons, warning icons, achievement icons, and optional animation. |
| `docs/assets/ireland_focus_tree_bop/gfx_handoff.md` | Sprite names and final DDS paths for main implementation wiring. |

## Validation surfaces

| Check | Purpose |
| --- | --- |
| duplicate BOP id search | ensure `IRE_state_authority_bop` exists once |
| stale side flag search | ensure old route side flags are cleaned after switch |
| BOP decision visibility check | ensure route decisions do not show outside active mode |
| AI invalid action check | ensure AI cannot take invalid route BOP decisions |
| localisation key check | ensure no working labels appear as final text |
| asset sprite path check | ensure BOP sprites point to real DDS files |
