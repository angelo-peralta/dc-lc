# Project Agent Rules

## Project
CPRINT Data Consultation and Language Editing System

## Stack
Use:
- Laravel
- Inertia.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- MySQL
- Eloquent ORM + Query Builder

Do not add:
- Next.js
- Prisma
- PostgreSQL
- Supabase
- S3
- Microsoft Entra ID
- JWT for normal staff login

## Role Rules

Authenticated roles:
- Data Consultation Coordinator
- Language Editing Coordinator
- Data Consultant
- Language Editor
- CPRINT Director
- Admin

No generic CPRINT Coordinator.

Public undergraduate student has no account.

## Module Boundary

Keep Data Consultation and Language Editing separate in routes, pages, controllers, services, statuses, requirements, assignments, and storage folders.

## Payment Rule

Payment is made at the Business Affairs Office (BAO). The application never handles payment processing.

Students upload an official receipt. The relevant service coordinator verifies it.

Assignment can happen only after:
1. requirements complete;
2. receipt uploaded;
3. receipt verified.

## Director Rule

CPRINT Director performs final review/approval before release.

## Evaluation Rule

Final output cannot be downloaded until the student completes the evaluation.

## Data Consultation SLA

15 working days begin when the Data Consultant is assigned. Weekends are excluded.

## Files

Use private storage only. Never store research documents in `/public`.

Support versioning and SHA-256 hashes.

## Archive Rule

Only the specific service coordinator archives/exports a case.

Export:
- generates ZIP;
- marks case archived/exported;
- starts 3-year retention.

Documents remain accessible during retention.

If not exported, retention does not start.

After retention expiry, files may be purged while database/audit records remain.

## Audit Rule

Every meaningful case action must be auditable.

Do not create noisy page-view audits.

## Code Quality

- thin controllers
- service/action classes
- Laravel policies
- Form Requests
- transactions for workflow changes
- modular React components
- no giant files
