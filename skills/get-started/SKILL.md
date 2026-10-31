---
name: get-started
description: Use when setting up ProWebLook in Claude, connecting or disconnecting an account, checking credits, or choosing the ProWebLook verification or research workflow.
---

Connect the bundled ProWebLook connector from this plugin's Connectors tab, using its OAuth sign-in flow for the user's own account. Never ask for an API key, password or token in chat. `get_account` reads connection status and current balances for free; `get_balance` also reads balances. Explain authentication errors and let the user reconnect through Claude. Pilot access must be enabled; package installation alone does not grant access.

Use the bundled [verify-lists workflow](../verify-lists/SKILL.md) for pasted lists or panel-selected CSV/XLSX files. Use [research-and-lookup](../research-and-lookup/SKILL.md) for single lookups, public web/social research and AI visibility audits. Discover this connector's tools and follow their actual schemas. Do not invoke other plugins to fill missing capabilities or move data to unrelated services.

List jobs use exactly one of WhatsApp, email, phone, caller ID, IP geolocation or blacklist, up to 10,000 input rows, 100 columns, 10 MiB uploaded and 50 MiB expanded XLSX. The hosted Claude panel uses a native file picker and private upload, with explicit worksheet/column selection. Do not promise chat-attachment ingestion, mobile or unqualified host support. Pasted-text preview remains available when the panel is unavailable; never transcribe an ambiguous workbook silently.

Show preview counts, source mapping, estimated credits and available balance, then wait for explicit approval before starting a list job. Existing ProWebLook credits or Geo-IP quota apply; there is no purchase or upgrade flow in this plugin. Job inputs and results expire after seven days; operational usage metadata is retained for 90 days. Retain the job ID for later status requests; do not promise unattended notifications.

For connection management, direct the user to Claude connector settings to disconnect and ProWebLook account connection controls to revoke authorization. Removing the plugin is not proof of server-side revocation or deletion of retained data. Use [support](https://proweblook.com/contact) and the [privacy policy](https://proweblook.com/privacy-policy) for account assistance and data requests.
