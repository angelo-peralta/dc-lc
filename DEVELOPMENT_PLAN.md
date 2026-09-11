# CPRINT Data Consultation and Language Editing System
## Finalized Development Plan

## 1. Purpose

Build a secure, auditable, web-based case management system for the two CPRINT services:
- Data Consultation
- Language Editing

The system should replace most paper-based routing and tracking with digital workflows while preserving traceability, file history, payment-proof verification, staff responsibility, and final institutional approval.

## 2. Applicant Model

Applicants are undergraduate students.

Students do not create accounts.

They submit publicly and receive a tracking number.

The tracking page acts as the student portal for:
- status viewing;
- editing permitted case information;
- correcting requirements;
- uploading payment proof;
- downloading previous uploads;
- seeing assigned consultant/editor;
- completing evaluation;
- downloading final output.

## 3. Staff Roles

- Data Consultation Coordinator
- Language Editing Coordinator
- Data Consultant
- Language Editor
- CPRINT Director
- Admin

## 4. Final Workflow

### Data Consultation

```text
Public Submission
→ DC Coordinator checks requirements
→ If incomplete: return for correction
→ If complete: instruct student to pay at BAO
→ Student pays PHP 1,650
→ Student uploads official receipt
→ DC Coordinator verifies receipt
→ DC Coordinator assigns Data Consultant
→ Consultant accepts or declines
→ 15-working-day processing period starts upon assignment
→ Consultant processes case
→ Consultant uploads output
→ CPRINT Director reviews
→ Revision if needed
→ Director approves for release
→ Student completes evaluation
→ Final output download enabled
→ Case completed
→ DC Coordinator may archive/export
```

### Language Editing

```text
Public Submission
→ LE Coordinator checks requirements
→ If incomplete: return for correction
→ If complete: instruct student to pay at BAO
→ Student pays PHP 1,650
→ Student uploads official receipt
→ LE Coordinator verifies receipt
→ LE Coordinator assigns Language Editor
→ Editor accepts or declines
→ Editor processes manuscript
→ Editor uploads edited manuscript
→ CPRINT Director reviews
→ Revision if needed
→ Director approves for release
→ Student completes evaluation
→ Final output download enabled
→ Case completed
→ LE Coordinator may archive/export
```

## 5. Archiving

Archiving is performed by the specific service coordinator.

Archive action:
- generates a ZIP package;
- records export metadata;
- marks the case archived/exported;
- starts the 3-year retention period.

If the coordinator does not export the case, retention does not start.

Archived documents remain accessible for the entire 3-year retention period.

After retention expiry:
- database records remain;
- document metadata remains;
- server files may be purged;
- audit history remains.

## 6. Technology Stack

- Laravel
- React + TypeScript
- Inertia.js
- Tailwind CSS
- shadcn/ui
- MySQL
- Laravel Eloquent + Query Builder
- Email/password staff authentication
- Private filesystem storage
- Laravel Mail/Notifications
- Laravel Queues
- Nginx + PHP-FPM

## 7. Payment

The system does not collect funds.

Students pay at the **Business Affairs Office (BAO)**.

The application only:
- displays payment instructions;
- stores payment-proof details;
- stores uploaded receipt;
- allows service coordinator to verify or reject the proof.

Current fee for both services:
- PHP 1,650

Fee must be configurable by Admin.

## 8. Evaluation Gate

Evaluation is mandatory before final output download.

```text
Director Approved
→ Evaluation Required
→ Evaluation Submitted
→ Final Download Enabled
```

## 9. Audit Philosophy

Audit only meaningful events needed to trace a case:
- submission;
- edits;
- requirement decisions;
- uploads;
- payment-proof actions;
- assignments;
- acceptance/decline;
- status changes;
- output versions;
- director approval/revision;
- release;
- withdrawal;
- reopening;
- archive/export;
- important downloads.

## 10. Development Priority

1. Project foundation
2. Roles/authentication
3. Private storage
4. Audit foundation
5. Public submission/tracking
6. Data Consultation workflow
7. Language Editing workflow
8. Director approval
9. Evaluation gate
10. Archive/export + retention
11. Reports
12. Notifications
13. Testing
14. Deployment
