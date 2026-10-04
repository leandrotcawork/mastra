---
'@mastra/core': patch
---

Fixed `session.abort()` leaving the `agentic-loop` registration and the `agentic-loop` and `executionWorkflow` snapshot rows behind for a run parked in a tool suspension. Once the abort has denied the parked tool calls, the run is released, so `agent.listSuspendedRuns()` no longer offers it and its in-memory state is freed.
