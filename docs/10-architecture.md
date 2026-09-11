# 10. System Architecture

```text
Browser
  ↓
Nginx
  ↓
Laravel
  ├── Authentication
  ├── Authorization
  ├── Public Submission
  ├── Tracking
  ├── Data Consultation
  ├── Language Editing
  ├── Director Review
  ├── Audit
  ├── Archive / Retention
  ├── Reporting
  └── Notifications
       ├── MySQL
       ├── Private File Storage
       ├── Queue
       └── Mail

Laravel → Inertia.js → React + TypeScript → Tailwind + shadcn/ui
```

## Rules
- backend is authoritative;
- React never decides permissions;
- workflow transitions are enforced in Laravel;
- audit events are server-side;
- files stream through authorized Laravel routes;
- DC and LE remain separate modules;
- important multi-record changes use transactions.
