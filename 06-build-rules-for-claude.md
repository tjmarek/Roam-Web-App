# ROAM Build Rules for Claude Code

## Goal
Build a working beta web app for ROAM based on the markdown spec files in this folder.

## Build Priorities
1. Start with a working end-to-end MVP.
2. Use a clean, production-style folder structure.
3. Make the app easy to run locally.
4. Use seed data only if needed for demo mode.
5. Prefer boring, reliable patterns over clever architecture.

## Suggested Tech Stack
- Next.js or another straightforward React web framework.
- TypeScript.
- Supabase or Postgres-backed auth/database.
- Tailwind for UI if it speeds up implementation.
- Server actions or API routes for marketplace actions.

## Non-Negotiables
- Role-based auth.
- Protected routes.
- Secure server-side checks for load ownership and bid acceptance.
- Form validation.
- Clear status transitions.
- Basic error handling and empty states.
- Environment variables for secrets.

## Implementation Order
1. Create app shell and auth.
2. Create database schema.
3. Build shipper flow to post a load.
4. Build driver flow to browse and bid.
5. Build shipper bid review and accept flow.
6. Add notifications.
7. Add basic admin tools.
8. Deploy beta.

## Guardrails
- Do not overbuild maps or geolocation early.
- Do not add payments in beta.
- Do not add ratings in beta.
- Keep notifications simple.
- Do not block progress with edge cases unless they break core flow.

## Required Demo Scenario
The finished beta must support this exact test:
1. User A signs up as a shipper.
2. User A posts a dump truck load.
3. User B signs up as a driver with matching equipment.
4. User B sees the load and submits a bid.
5. User A accepts the bid.
6. User B sees the load marked as assigned.

## What Claude Should Produce
- Full code files, not partial snippets.
- Clear setup instructions.
- Database schema and migration instructions.
- Seed or demo instructions.
- Deployment steps.
