# Ireland focus tree improvement loop tooling note

## Status

The mandatory near completion `hoi4_improvement_loop_planner` pass has not been run in this chat environment.

## Reason

The available tools here do not expose a project custom subagent spawning interface. The project source files define `hoi4_improvement_loop_planner` and require it for near completion with `fork_context=false`, but there is no callable subagent tool available in this runtime.

## Implementation meaning

The canonical design package is complete enough for implementation. The process gate remains visible so an implementation agent in a capable environment can run the planner before claiming near completion.

## Required later action

In an environment that exposes project subagents, spawn `hoi4_improvement_loop_planner` with `fork_context=false` and pass the feature slug, all spec files, all matrices, all prompt files, research notes, hidden path material, this tooling note, and the exact question in `prompts/ireland_focus_tree_improvement_loop_prompt.md`.

Resolve the planner result before final implementation completion by folding accepted content into specs or code, queueing it with reason, rejecting it with reason, or recording closure.
