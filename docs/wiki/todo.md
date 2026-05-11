# TODO

## Overview

This page collects code-backed follow-up work that is visible from the current repository state. These items are not a roadmap promise. They are simply the most obvious gaps and cleanup points surfaced while generating the wiki.

## Navigation Gaps

- Keep hidden future surfaces such as MCP, templates, and top-level integrations out of the v2.0 navigation until they have implemented routes.
- If `/settings/account` is added later, reintroduce it to `app/(dashboard)/settings/_components/settings-sidebar.tsx`.

## Project Workspace Follow-Ups

- Decide whether `/projects/[id]/exec-test` is a permanent product surface or a debug-only page, then align navigation and docs accordingly.
- Review the current assumption that the first sandbox and first database are the primary runtime surfaces, even though the schema supports more than one of each.
- Revisit the environment update rule that blocks writes unless the full project is already `RUNNING`, and confirm that this is the intended UX for setup flows.

## API and Control Plane Follow-Ups

- Add stronger request validation around internal route handlers, which currently rely mostly on inline checks instead of shared schemas.
- Finish the migration noted in `lib/actions/sandbox.ts` so sandbox operations do not remain split across route handlers and server actions.
- Continue consolidating platform logic into `lib/platform/` so the newer control-plane layering becomes the clear source of truth.

## Documentation Follow-Ups

- Keep this page in sync when missing routes are implemented or reintroduced.
- If task priority starts to matter, replace this flat list with a status-driven backlog page rather than mixing implementation state into architecture pages.
