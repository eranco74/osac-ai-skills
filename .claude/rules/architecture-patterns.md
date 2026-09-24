# Architecture patterns

Before changing OSAC resource flows, tenancy, or shared contracts, read the
OSAC repository's root `AGENTS.md` and each affected component's `AGENTS.md`.

- `docs/ARCHITECTURE.md` describes the current resource hierarchy, service
  stack, and control loops.
- `docs/CONVENTIONS.md` describes cross-component dependencies.
- `docs/INTEGRATION-TESTING.md` and the affected component's `AGENTS.md`
  contain current test setup and coverage boundaries.

Preserve tenant scoping with the `osac.openshift.io/tenant` annotation and,
where applicable, resource hierarchy with `osac.openshift.io/owner-reference`.
Use the current docs as the source for resource names and integration commands.
