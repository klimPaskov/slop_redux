# Ireland BOP improvement loop blocker

## Required pass

The feature planning standard requires a near completion pass from `hoi4_improvement_loop_planner` with `fork_context=false`.

## Tooling status

This chat environment does not expose a callable project custom subagent spawning tool. I cannot spawn `hoi4_improvement_loop_planner` from here.

## Handling

The BOP addendum package is complete as a design handoff, but the mandatory project subagent pass remains a procedural blocker for the implementation environment.

Use `prompts/ireland_bop_improvement_loop_prompt.md` in an environment that can spawn the subagent with `fork_context=false`.

If the subagent returns an addendum, the implementation owner must fold accepted content into the relevant spec or implementation docs, queue it with a reason, or reject it with a reason. If it returns a closure handoff, record it before final completion.
