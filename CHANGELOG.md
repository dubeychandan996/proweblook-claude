# Changelog

## First-release scope update — 1 November 2026

- Defer LinkedIn social search and post lookup in addition to the existing X (Twitter) deferral. Retain Reddit social search/post tools and their existing Reddit default.
- Reject deferred social-tool requests before provider work or credit use. ChatGPT, the public REST API, Google results and general website extraction are unchanged.
- Document Reddit provider limitations: returned data may be unrelated, incomplete or truncated. A successful response does not establish relevance or full post content.
- This candidate requires the matching Claude Worker update; package preparation does not establish production deployment or directory approval. The earlier scope below is historical and is superseded by this update.

## Earlier scope — X deferral, 1 November 2026

- Defer X (Twitter) social search, post lookup and comments from the Claude connector. Retain Reddit and LinkedIn search/post tools and their existing Reddit default.
- Reject excluded X social requests before provider work or credit use. ChatGPT, the public REST API, Google results and general website extraction are unchanged.
- This candidate requires the matching Claude Worker update; package preparation does not establish production deployment or directory approval.

## 1.0.0 — private pilot

- Package ProWebLook account setup, confirmed list verification, and public research/audit workflows as three Claude skills.
- Declare the canonical OAuth-enabled remote HTTP connector without embedded credentials.
- Document existing credit usage, private panel uploads, limits, connection controls and retention.

### Hosted product verification — 31 October 2026

- Verified the installed private package in Claude web with existing-account OAuth and free account/balance reads.
- Verified native CSV/XLSX selection, private upload, explicit worksheet/column mapping, free previews and separate approval before one paid email job.
- Verified completed results, pagination and actual saved CSV/XLSX exports through the private-link fallback, including expired-link rejection. Links last at most five minutes; job inputs, results and exports expire seven days after job creation.
- Verified automatic updates in fresh result/export panels. An already open Claude tab may need one reload after a connector update.
- Updated example prompts for free account reads, preview-and-wait behavior and existing account-owned audit records.

These observations cover the hosted email-list workflow, not live execution of every provider or service. Claude Code, desktop, Cowork, mobile and chat-attachment ingestion remain unqualified for this product workflow. This version remains a private pilot requiring an enabled account; no marketplace submission or public release is claimed.
