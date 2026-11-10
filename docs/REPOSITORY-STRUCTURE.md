# VELTRIX TECH CLOUD — Repository Structure

**Status:** Phase 1 planning
**Parent brand:** VELTRIX TECH

## 1. Purpose

This document defines the initial repository layout for VELTRIX TECH CLOUD. The structure will grow as the platform is implemented.

## 2. Planned layout

```text
veltrix-tech-cloud/
├── README.md
├── .gitignore
├── docs/
│   ├── ARCHITECTURE.md
│   └── REPOSITORY-STRUCTURE.md
├── apps/
│   └── console/
├── services/
│   └── api/
├── supabase/
│   ├── migrations/
│   └── config/
├── packages/
│   └── shared/
└── tests/
    ├── auth/
    └── security/
```

## 3. Directory responsibilities

- apps/console: VELTRIX developer and organisation dashboard.
- services/api: backend API services.
- supabase/migrations: version-controlled database migrations.
- supabase/config: database platform configuration.
- packages/shared: reusable, shared application code.
- tests/auth: authentication tests.
- tests/security: authorisation, isolation and security tests.
- docs: technical plans and project documentation.

## 4. Development rules

1. Keep application code separate from infrastructure configuration.
2. Keep database changes in reviewed migrations.
3. Never commit passwords, API keys or private credentials.
4. Add tests alongside important functionality.
5. Avoid unnecessary dependencies.
6. Keep development, testing and production environments separate.

## 5. Implementation policy

This is a planned structure, not a claim that all components already exist.

Folders and starter files will be added when their implementation begins. Technology and dependency choices must be checked before installation.

No deployment, purchases or production changes are authorised by this document.
