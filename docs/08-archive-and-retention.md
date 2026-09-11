# 08. Archive, Export, and Retention

## Archive Ownership
- Data Consultation cases: Data Consultation Coordinator
- Language Editing cases: Language Editing Coordinator

## Retention Start
The 3-year retention begins only after successful archive/export.

If the coordinator does not export the case, no retention countdown begins.

## Archive Action
Coordinator selects **Archive / Export Case**.

System should:
1. show confirmation dialog;
2. generate ZIP package;
3. confirm generation;
4. allow download;
5. mark case archived/exported;
6. record export metadata;
7. start 3-year retention.

## Recommended ZIP Contents

```text
CASE-TRACKING-NUMBER.zip
├── 01_Case_Information/
├── 02_Student_Submissions/
├── 03_Payment/
├── 04_Agreement/
├── 05_Assignment/
├── 06_Outputs/
├── 07_Evaluation/
├── 08_Audit/
├── case-data.json
└── manifest.json
```

## Metadata
- archived_at
- archived_by
- exported_at
- exported_by
- archive_filename
- archive_version
- retention_started_at
- retention_expires_at

## During Retention
For 3 years:
- files remain accessible;
- files remain downloadable;
- archived case is generally read-only;
- archive can be regenerated if permitted.

## At Retention Expiry
- server documents may be purged;
- database case record remains;
- document metadata remains;
- audit history remains;
- archive/export metadata remains.

## Retention Alerts
Recommended:
- 90 days before expiry
- 30 days before expiry
- 7 days before expiry
