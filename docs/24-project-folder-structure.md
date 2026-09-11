# 24. Proposed Code Folder Structure

## Laravel

```text
app/
├── Models/
│   ├── DataConsultation/
│   ├── LanguageEditing/
│   ├── User.php
│   ├── AuditLog.php
│   └── ArchiveExport.php
├── Services/
│   ├── DataConsultation/
│   ├── LanguageEditing/
│   ├── Audit/
│   ├── Documents/
│   ├── Tracking/
│   ├── PaymentProof/
│   ├── Archive/
│   ├── Retention/
│   └── Notifications/
├── Actions/
│   ├── DataConsultation/
│   ├── LanguageEditing/
│   ├── Archive/
│   └── DirectorReview/
├── Http/
│   ├── Controllers/
│   │   ├── Public/
│   │   ├── DataConsultationCoordinator/
│   │   ├── LanguageEditingCoordinator/
│   │   ├── Consultant/
│   │   ├── Editor/
│   │   ├── Director/
│   │   └── Admin/
│   ├── Requests/
│   └── Middleware/
└── Policies/
```

## React / Inertia

```text
resources/js/
├── pages/
│   ├── Public/
│   ├── DataConsultationCoordinator/
│   ├── LanguageEditingCoordinator/
│   ├── Consultant/
│   ├── Editor/
│   ├── Director/
│   └── Admin/
├── components/
├── features/
│   ├── data-consultation/
│   ├── language-editing/
│   ├── tracking/
│   ├── director-review/
│   ├── archive/
│   └── retention/
├── layouts/
├── hooks/
├── types/
└── lib/
```
