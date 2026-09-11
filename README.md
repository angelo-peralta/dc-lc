# CPRINT Data Consultation and Language Editing System

This folder contains the finalized project documentation for the planned **CPRINT Data Consultation and Language Editing System**.

The system digitizes two separate CPRINT services:

- **Data Consultation**
- **Language Editing**

The two services are part of one application but remain separated in workflow, pages, routes, files, business rules, staff responsibility, and reporting.

## Final Technology Stack

- **Backend:** Laravel
- **Frontend:** React + TypeScript
- **Integration:** Inertia.js
- **UI:** Tailwind CSS + shadcn/ui
- **Database:** MySQL
- **Database Access:** Laravel Eloquent ORM + Query Builder
- **Authentication:** Email + Password for staff only
- **Applicant Access:** Public submission + tracking number
- **File Storage:** Private local/server storage
- **Web Server:** Nginx + PHP-FPM
- **Email:** Laravel Mail / Notifications
- **Queues:** Laravel Queues

## Final User Roles

### Public User
- Undergraduate Student / Client
- No account
- Uses public submission and tracking number

### Authenticated Staff
- Data Consultation Coordinator
- Language Editing Coordinator
- Data Consultant
- Language Editor
- CPRINT Director
- Admin

There is **no generic CPRINT Coordinator role**.

## Final Core Workflow

```text
Public Submission
→ Requirements Review by Service Coordinator
→ Correction if Incomplete
→ Requirements Complete
→ Student Pays at Business Affairs Office (BAO)
→ Student Uploads Official Receipt
→ Service Coordinator Verifies Payment Proof
→ Coordinator Assigns Consultant / Editor
→ Assigned Staff Accepts or Declines
→ Processing
→ Output Submitted
→ CPRINT Director Reviews
→ Revision if Needed
→ Approved for Release
→ Student Completes Evaluation
→ Final Output Download Enabled
→ Case Completed
→ Coordinator May Archive / Export
→ 3-Year Retention Begins from Export Date
```

## Important Final Rules

- Both services currently cost **PHP 1,650**, configurable by Admin.
- Applicants are undergraduate students only.
- Only the research leader / primary contact is recorded.
- Students can edit submitted information, but changes must be audited.
- Tracking number alone is used for applicant access in Version 1.
- Student can withdraw only before payment.
- Closed cases may be reopened by authorized staff.
- Data Consultation payment covers the entire case; no second payment is required for additional consultation within the same case.
- Multiple output versions are supported.
- Final evaluation is mandatory before the final output can be downloaded.
- Data Consultation 15-working-day processing starts once the consultant is assigned.
- Weekends are excluded.
- Archive/export starts the 3-year document retention period.
- If a case is not exported, the 3-year retention does not start.
- Archived documents remain normally accessible during the 3-year retention period.
- After retention expiry, documents may be removed from server storage while the database record remains.

## Documentation Index

See `/docs` for the complete finalized development plan.

Also included:
- `DEVELOPMENT_PLAN.md`
- `AGENTS.md`
