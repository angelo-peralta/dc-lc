# 14. Security and Privacy

## Public Tracking
Since tracking number alone is used, it should be difficult to guess.

Use:
- random component;
- rate limiting;
- failed-access logging;
- HTTPS;
- generic error messages.

## Staff
- hashed passwords;
- Laravel sessions;
- CSRF;
- secure cookies;
- login throttling;
- password reset.

## Authorization
Use Laravel policies so each role only accesses permitted service/cases.

## Documents
- private storage only;
- authorized download routes;
- generated stored filenames;
- MIME validation;
- file-size limits;
- SHA-256 hash;
- no direct public URLs.

## Sensitive Research Data
Limit to authorized staff and log important downloads.

## Secrets
Keep secrets in `.env`, not source control.
