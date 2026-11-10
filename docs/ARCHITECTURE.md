# VELTRIX TECH CLOUD — Architecture

**Status:** Phase 1 foundation plan  
**Parent brand:** VELTRIX TECH

## 1. Product vision

VELTRIX TECH CLOUD is the backend platform for VELTRIX products and, eventually, external developers and businesses.

Its planned services include:
- VELTRIX AUTH — authentication and identity.
- VELTRIX DATABASE — database management.
- VELTRIX STORAGE — file and object storage.
- VELTRIX API — developer integrations.
- VELTRIX CONSOLE — customer dashboard.
- VELTRIX ADMIN — restricted internal administration.

## 2. Technology direction

Initial proposed foundation:
- PostgreSQL
- Open-source, self-hosted Supabase components
- Supabase Auth initially
- TypeScript backend
- React and TypeScript web console
- GitHub for source control
- Docker where development hardware supports it
- Flutter as a candidate for future mobile applications

VELTRIX will gradually develop its own branded control plane and replace components when technically and financially sensible.

## 3. Organisation and project structure

The initial logical structure is:

User → Organisation membership → Organisation → Projects → Resources

Users may belong to multiple organisations. Permissions must be enforced server-side, not just hidden in the user interface.

## 4. Phase 1 — Foundation and authentication

Planned deliverables:
1. Establish repository structure and development workflow.
2. Design the database schema.
3. Implement email/password registration and sign-in.
4. Support email verification and password recovery.
5. Establish organisations and projects.
6. Define roles and permissions.
7. Build a responsive VELTRIX Console.
8. Prepare an integration path for STAYORA.
9. Test account isolation, unauthorised access, sessions, recovery and database access.

STAYORA must remain unchanged until VELTRIX AUTH is ready and tested.

## 5. Security requirements

- Never store plaintext passwords.
- Never commit passwords, API keys or service secrets.
- Enforce permissions on the server.
- Use PostgreSQL Row Level Security where appropriate.
- Isolate organisation and project data.
- Apply least-privilege access.
- Separate development, testing and production.
- Test security before using real customer data.

## 6. Budget and deployment policy

Initial development budget: **₦0**.

No paid APIs, subscriptions, servers, hosting purchases or production deployment without explicit approval.

Open-source software may be free, but hosting, storage, bandwidth, email delivery, backups and maintenance can still incur costs. We must verify free-tier limits and never promise unlimited free production usage.

## 7. Open decisions

- Suitable zero-cost development environment.
- Exact Supabase components for Phase 1.
- Email verification and recovery delivery.
- Database schema and permission policies.
- Backup and recovery strategy.
- Future STAYORA integration and migration plan.

## 8. Change control

This document records the approved architectural direction. It does not authorise purchases, deployment, production migration or changes to existing applications. Each requires separate explicit approval.
