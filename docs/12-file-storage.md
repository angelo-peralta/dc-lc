# 12. File Storage and Versioning

## Private Storage
Recommended root:
`/srv/cprint-storage/`

## Separation

```text
/srv/cprint-storage/
├── data-consultation/
│   └── YEAR/
│       └── TRACKING-NUMBER/
└── language-editing/
    └── YEAR/
        └── TRACKING-NUMBER/
```

## Metadata
Store:
- original_filename
- stored_filename
- storage_path
- mime_type
- file_size
- sha256_hash
- version_number
- document_type
- uploaded_by
- uploaded_at
- is_current_version
- status

## Versioning
Preserve old versions. Never silently overwrite.

## Recommended File Types

### Data Consultation
`.doc`, `.docx`, `.pdf`, `.xlsx`, `.xls`, `.csv`, `.sav`, `.zip`

Optional later: `.dta`, `.rdata`

### Language Editing
`.doc`, `.docx`, `.pdf`

## Recommended Initial Limits
- Manuscript: 50 MB
- Dataset: 100 MB
- Other Supporting File: 50 MB
- Receipt: 10 MB

Admin should be able to configure limits.
