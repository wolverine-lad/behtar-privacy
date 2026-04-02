# Privacy Policy - Behtar: Prompt Improver

Last updated: April 3, 2026

Behtar: Prompt Improver is a browser extension that helps improve prompts before they are sent to AI platforms. This policy explains what data we collect, how we use it, and what rights you have.

---

## 1. Data We Collect and Process

We process a limited set of pseudonymous identifiers and usage metrics to operate and improve the service. Under applicable data protection laws (including GDPR and India's DPDPA 2023), pseudonymous identifiers such as invite codes may constitute personal data.

**Lawful basis (EU/EEA — GDPR):** We process analytics data on the basis of legitimate interest (Article 6(1)(f) GDPR) in operating and improving the service. We have assessed that this interest is not overridden by individual rights because: (a) the data is pseudonymous and not linked to your real-world identity; (b) only minimal data is collected; and (c) you can opt out at any time by disabling the extension.

**Lawful basis (India — DPDPA 2023):** Where required by India's DPDPA 2023, we will seek your explicit consent before processing personal data. You may withdraw consent at any time by disabling or uninstalling the extension.

### Data sent to our servers

| Data point | Purpose | Logged in analytics? | Retention |
|---|---|---|---|
| Invite code | Access verification | Yes | 3 months |
| Install ID | Daily rate limiting | No | Not stored by us |
| IP address | Rate limiting (handled by Cloudflare infrastructure) | No | Not stored by us — Cloudflare may retain per their own policy |
| Prompt text | Forwarded to Anthropic API for rewriting | No | Not stored by us (see Section 3) |

### Data storage summary

| Data | Where stored | Sent to our servers? |
|---|---|---|
| Prompt text (weak prompts only) | Not stored — sent to relay server for processing and discarded after response is returned | Yes, to relay and Anthropic — not retained by us |
| Invite code | Browser local storage | Yes, at validation and per analytics event |
| Install ID | Browser local storage | Yes, for rate limiting — not stored server-side |
| Usage counts / session stats | Browser local storage | No |

### Analytics logged per optimization event (stored 3 months)

invite_code, platform, mode, environment, extension_version, model_used (haiku or sonnet), event_id (UUID), browser, prompt_length (character count only), response_time_ms, prompt_score.

### Analytics logged per action event (stored 3 months)

action_type (e.g. accepted, dismissed, edited, sent_improved, thumbs_up, thumbs_down, nps, relay_error, and similar), invite_code, platform, mode, environment, extension_version, event_id, browser, prompt_score, time_to_decision_ms.

### NPS rating

An optional satisfaction rating (1–10) is logged when you choose to submit one via the extension popup.

### Local storage (never sent to our servers)

Daily improvement counts, lifetime improvement counts, per-platform totals, selected mode preference, and session statistics are stored in your browser's local storage and are never transmitted.

---

## 2. What We Do Not Collect

- We do not log the content of your prompts. Only the character count is recorded in analytics.
- We do not collect your name, email address, or account credentials.
- We do not track browsing history outside the four supported AI platforms (ChatGPT, Claude, Gemini, Perplexity).
- We do not collect keystrokes, clipboard contents, or any page content beyond the specific prompt input field.
- We do not sell data to any third party.
- We do not use data for advertising.

**Note:** We do process pseudonymous identifiers (your invite code and install ID) as described in Section 1. While we do not collect directly identifying information such as your name or email, these identifiers may constitute personal data under applicable law.

---

## 3. How Your Prompts Are Processed

Before any network request is made, your prompt is scored locally in your browser. No data leaves your device during scoring. A prompt is only sent to our relay server if the score falls below the weak-prompt threshold and the extension is active. If your prompt scores above the threshold, it is never sent anywhere.

When the threshold is met, your prompt text is sent to our relay server (hosted on Cloudflare Workers), which forwards it to the Anthropic API (Claude) for rewriting. The improved prompt is returned to your browser. **We transmit your prompt to enable the improvement feature, but we do not log or store the prompt content on servers we control.** The relay acts as a pass-through only.

Anthropic may retain API inputs for up to 30 days in accordance with their data handling and safety review practices. We do not control what Anthropic retains. Please review [Anthropic's Privacy Policy](https://www.anthropic.com/legal/privacy) for details.

---

## 4. Third-Party Services

- **Anthropic API** — Used to rewrite prompts. We send only the prompt text — no user identifiers, no account information, and no metadata about your identity. Anthropic may retain submitted text for up to 30 days. Subject to [Anthropic's Privacy Policy](https://www.anthropic.com/legal/privacy).
- **Cloudflare Workers** — Our relay and analytics infrastructure runs on Cloudflare's global edge network. Data may be processed in any country where Cloudflare operates. Subject to [Cloudflare's Privacy Policy](https://www.cloudflare.com/privacypolicy/).

**International data transfers:** Both Anthropic and Cloudflare are US-based companies. If you are located in the EU/EEA or another jurisdiction with data transfer restrictions, your data is transferred to the United States. These transfers are made subject to Standard Contractual Clauses (SCCs) adopted by the European Commission, which provide appropriate safeguards. Cloudflare's SCCs are documented in their Data Processing Addendum. Anthropic's data transfer mechanisms are described in their Privacy Policy.

---

## 5. Data Retention

Analytics data is retained for up to 3 months (90 days) for monitoring and product improvement. No prompt content is retained on servers we control.

---

## 6. Your Rights

Depending on where you are located, you may have the following rights regarding your data:

- **Access** — Request a copy of analytics data associated with your invite code.
- **Rectification** — Request correction of inaccurate data.
- **Erasure** — Request deletion of analytics data associated with your invite code.
- **Restriction** — Request that we restrict processing of your data pending a query or objection.
- **Object** — Object to processing based on legitimate interest. You may also opt out at any time by disabling the extension, which prevents any prompt from being sent for improvement.
- **Withdraw consent (India)** — If you are located in India, you may withdraw consent at any time by disabling or uninstalling the extension.
- **Supervisory authority** — If you are located in the EU/EEA, you have the right to lodge a complaint with your local data protection supervisory authority.

To exercise any of these rights, email us at shreyiitkgp96@gmail.com. We aim to respond within 7 business days.

All local data stored by the extension is deleted automatically when you uninstall it from your browser.

---

## 7. Data Breach Notification

In the event of a personal data breach that is likely to result in a risk to your rights and freedoms, we will notify the relevant supervisory authority within 72 hours of becoming aware, and will notify affected individuals without undue delay where required by applicable law.

---

## 8. Children

This extension is not directed at children under 16 in the EU/EEA, or under 13 in all other jurisdictions. We do not knowingly collect any information from children below these ages.

---

## 9. Changes to This Policy

We may update this policy from time to time. The "Last updated" date at the top will reflect any changes.

---

## 10. Contact

For any privacy-related questions or requests, email us at shreyiitkgp96@gmail.com. We aim to respond within 7 business days.
