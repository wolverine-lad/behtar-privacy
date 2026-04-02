# Privacy Policy - Behtar: Prompt Improver

Last updated: April 3, 2026

Behtar: Prompt Improver is a browser extension that helps improve prompts before they are sent to AI platforms. This policy explains what data we collect, how we use it, and what we do not do.

## 1. Data We Collect and Process

We process a limited set of pseudonymous identifiers and usage metrics to operate and improve the service. Under applicable data protection laws (including GDPR and India's DPDPA 2023), pseudonymous identifiers may constitute personal data. We process this data on the basis of legitimate interest in providing and improving the service.

### Data sent to our servers

| Data point | Purpose | Logged in analytics? | Retention |
|---|---|---|---|
| Invite code | Access verification | Yes | 3 months |
| Install ID | Daily rate limiting | No | Not stored on our servers |
| IP address | Rate limiting | No | Not stored on our servers |
| Prompt text | Forwarded to Anthropic API for rewriting | No | Not stored on servers we control (see Section 3) |

### Analytics logged per optimization event (stored 3 months)

invite_code, platform, mode, environment, extension_version, model_used (haiku or sonnet), event_id (UUID), browser, prompt_length (character count only), response_time_ms, prompt_score.

### Analytics logged per action event (stored 3 months)

action_type (e.g. accepted, dismissed, edited, sent_improved, thumbs_up, thumbs_down, nps, relay_error, and similar), invite_code, platform, mode, environment, extension_version, event_id, browser, prompt_score, time_to_decision_ms.

### NPS rating

An optional satisfaction rating (1-10) is logged when you choose to submit one via the extension popup.

### Local storage (never sent to our servers)

Daily improvement counts, lifetime improvement counts, per-platform totals, selected mode preference, and session statistics are stored in your browser's local storage and are never transmitted.

## 2. What We Do Not Collect

- We do not log the content of your prompts. Only the character count is recorded.
- We do not collect your name, email address, or account credentials.
- We do not track browsing history outside the four supported AI platforms.
- We do not sell data to any third party.
- We do not use data for advertising.

## 3. How Your Prompts Are Processed

When you trigger an improvement, your prompt is sent to our relay server (hosted on Cloudflare Workers), which forwards it to the Anthropic API (Claude) for rewriting. The improved prompt is returned to your browser. We do not store prompt content on servers we control.

However, Anthropic may retain API inputs in accordance with their own data handling practices. We cannot speak for what Anthropic retains on their servers. Please review [Anthropic's Privacy Policy](https://www.anthropic.com/legal/privacy) for details.

## 4. Third-Party Services

- **Anthropic API** - Used to rewrite prompts. Subject to [Anthropic's Privacy Policy](https://www.anthropic.com/legal/privacy).
- **Cloudflare Workers** - Our relay and analytics infrastructure runs on Cloudflare's global edge network. Data may be processed outside your country of residence. Subject to [Cloudflare's Privacy Policy](https://www.cloudflare.com/privacypolicy/).

## 5. Data Retention

Analytics data is retained for up to 3 months (90 days) for monitoring and product improvement. No prompt content is retained on servers we control.

## 6. Data Deletion

You may request deletion of analytics data associated with your invite code by emailing us at the address below. All local data stored by the extension is deleted automatically when you uninstall it from your browser.

## 7. Changes to This Policy

We may update this policy from time to time. The "Last updated" date at the top will reflect any changes.

## 8. Contact

For any privacy-related questions or deletion requests, email us at shreyiitkgp96@gmail.com
