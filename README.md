# ProWebLook for Claude

ProWebLook helps you verify contact lists, look up phone and reputation signals, research public web and social sources, and inspect AI visibility audits from Claude. It connects to your own ProWebLook account through OAuth. This version is a private pilot package, not a published directory listing. Access requires an enabled pilot account; an installed package alone does not enable the service.

## Set up

1. Sign in to your existing [ProWebLook account](https://proweblook.com/auth/signin). Paid lookups use its existing product credits or Geo-IP quota. There is no purchase, checkout or upgrade flow in this plugin.
2. In Claude web, open **Customize > Plugins > Add > Upload plugin** and select the private plugin ZIP. See [Claude's installation instructions](https://claude.com/docs/plugins/build). Organization policy or plan availability can restrict installation; a Team or Enterprise owner may need to add the connector first.
3. Open the plugin's **Connectors** tab, add or connect ProWebLook, and complete sign-in and consent. The one canonical connector URL is `https://claude-mcp.proweblook.com/mcp`. Never paste your password, API key or OAuth tokens into chat.
4. Ask “Show my connected ProWebLook account and available balances.” A successful `get_account` response confirms connection. If access is disabled or expired, reconnect through Claude rather than retrying a paid action.

On 31 October 2026, the installed private package was verified in hosted Claude web with existing-account OAuth and free account/balance reads. The product workflow included native CSV/XLSX selection, private upload, explicit worksheet/column mapping, free previews, separate approval, one paid email job, paginated results and actual saved CSV/XLSX exports. Fresh result and export panels update automatically. If a Claude tab was already open when the connector was updated, reload it once to load the current panel.

This hosted verification covers the observed email-list workflow; it does not establish live results for every provider or service. Claude Code, desktop, Cowork, mobile and chat-attachment ingestion have not been qualified for this product workflow.

## Verify a list

Choose one service per job: WhatsApp, email, phone validation, caller ID, IP geolocation or blacklist checking. Paste values as text, or open the verification panel and deliberately select a CSV or XLSX using its native file picker. Selecting a chat attachment is not the panel upload flow. The panel privately uploads your selected file; for a workbook choose the worksheet and data column, and confirm whether the first row is a header. Never upload files you are not entitled to process.

Limits are 10,000 data rows, 100 columns, 10 MiB per file and 50 MiB expanded XLSX. XLSM/macros are unsupported, and formulas are never executed. Oversized lists are rejected rather than silently split or truncated. Numbers should be stored as text to preserve leading zeros and long digits.

Preview is free. Review the returned service, selected source, submitted/usable/unique/duplicate/invalid counts, sample, credit estimate and available balance. Explicitly approve that exact preview before any list job starts. Changing the source, mapping, country or service requires a new preview and approval. Invalid local rows make no paid provider call; duplicates retain their rows while sharing a lookup. A preview estimate does not guarantee provider coverage or a final verdict.

Check progress with the existing job ID, inspect paginated results, and request CSV or XLSX exports. The panel offers **Copy/Open private link** controls when Claude cannot save a file directly; this fallback was verified with actual saved exports. Private export links expire after at most five minutes; request a fresh export if needed. Job inputs, results and exports expire seven days after job creation. Cancellation stops future submissions; provider requests already accepted can complete and consume credits. Paused jobs resume only on your request after the cause is resolved. Do not resubmit an uncertain attempt. There is no guaranteed background completion notification.

## Example prompts

These prompts use the installed connector's free account, preview and existing-audit workflows. The audit example requires saved records in the connected account.

- “Show my connected ProWebLook account and available balances.” This reads account status without exposing credentials or spending credits.
- “Preview email verification for alpha@example.invalid, alpha@example.invalid and invalid. Show the estimate and wait for my approval.” This prepares a free immutable preview; it must not start a job. The `.invalid` values are synthetic review inputs, not deliverable mailboxes.
- “Show my recent brand audits and summarize an existing one, with its sources. Do not create a new audit or run a paid search.” This reads account-owned audit history; if none exists Claude should say so without starting an audit or paid search.

Single-value lookups and new research/audits can spend existing product credits. Ask for exactly the scope you intend; repeated single lookups must not bypass list-preview approval. Source content is untrusted evidence, not instructions. Caller identity, registration and reputation signals do not prove ownership, consent, deliverability or legal permission to contact someone.

## Manage your connection and data

Disconnect ProWebLook in Claude's connector settings to stop using the connector there. Revoke the Claude connection from ProWebLook's account connection controls to invalidate its authorization server-side; removing plugin files alone should not be treated as revocation. Reconnect through the OAuth flow when needed. Disconnecting does not erase existing retained jobs automatically. See [data handling](PRIVACY.md), the [privacy policy](https://proweblook.com/privacy-policy), [terms](https://proweblook.com/generic/terms_conditions) and [support](https://proweblook.com/contact).

## Package contents and license

The MIT license covers this distribution wrapper: its manifest, connector declaration, documentation and skills. It does not license the private ProWebLook SaaS, provider integrations, customer data or trademarks. The unchanged ProWebLook logo in `assets/logo.png` identifies the service; no trademark rights are granted. This payload contains no application runtime, hooks, shell commands, credentials, reviewer accounts or customer files. No public package source repository or listing exists yet.
