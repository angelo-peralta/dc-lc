# 11. Database Plan

## Shared Tables
- users
- roles
- permissions
- schools
- programs
- service_fees
- payment_proofs
- audit_logs
- notifications
- archive_exports

## Data Consultation
- data_consultation_requests
- data_consultation_requirements
- data_consultation_documents
- data_consultation_document_versions
- data_consultation_assignments
- data_consultation_agreements
- data_consultation_outputs
- data_consultation_status_history
- data_consultation_evaluations

## Language Editing
- language_editing_requests
- language_editing_requirements
- language_editing_documents
- language_editing_document_versions
- language_editing_assignments
- language_editing_outputs
- language_editing_status_history
- language_editing_evaluations

## Common Request Fields
- id
- tracking_number
- current_status
- submitted_at
- completed_at
- archived_at
- retention_started_at
- retention_expires_at

## Applicant Snapshot
Preserve the student data used at the time of the case so later reference-data changes do not alter historical records.
