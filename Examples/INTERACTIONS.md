# Example Agent Interactions

Short before/after snippets showing each `CLAUDE.md` principle in practice.

## Always think instead of assume

> **User:** "Cache this function's results."

❌ **Without the rule:** Agent immediately wraps the function in an in-memory memoization decorator.

✅ **With the rule:** Agent asks: in-process memory (simple, but per-instance and lost on restart) or a shared cache like Redis (survives restarts, works across instances, but adds infra)? Which fits, or is there an existing caching layer in the project already?

## Simplicity is key

> **User:** "Add a way to filter the results list by status."

❌ **Without the rule:** Agent builds a generic query-builder abstraction with a plugin system for arbitrary future filter types.

✅ **With the rule:** Agent adds a single `status` parameter to the existing query function — the only filter actually requested.

## Code changes

> **User:** "Fix the off-by-one error in `paginate()`."

❌ **Without the rule:** Agent fixes the bug, then also renames variables, reformats the file, and deletes an unused helper it noticed nearby.

✅ **With the rule:** Agent fixes only the off-by-one error, and separately mentions: "`legacy_sort()` on line 42 looks unused — didn't touch it, flagging in case you want it removed."

## Goal oriented

> **User:** "Refactor the auth module."

❌ **Without the rule:** Agent starts moving code around with no defined endpoint for "done."

✅ **With the rule:** Agent restates the goal first: "I'll restructure `auth/` and verify success by running the existing auth test suite plus a manual login/logout check — behavior should be unchanged. Sound right?"

## Rules

> **User:** "Add a new API endpoint."

❌ **Without the rule:** Agent picks its own naming/response-shape conventions.

✅ **With the rule:** Agent checks `Docs/` for an existing API or style convention first; if none exists, it asks rather than inventing one silently.
