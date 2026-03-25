# Privacy Policy — Behtar: Prompt Improver

**Last updated: March 25, 2026**

---

## Who We Are

Behtar: Prompt Improver is a Chrome browser extension that helps you write better prompts on AI chat platforms. This policy explains what information the extension handles, how it handles it, and what rights you have. Developed by Shreyansh Gupta.

Questions? Contact us at **privacy@behtar.app**

---

## The Short Version

- Your prompts are scored entirely on your device. Nothing leaves your browser just because you typed something.
- A prompt is only ever sent anywhere if (a) it scores below the weak-prompt threshold and (b) the extension attempts to improve it.
- We do not collect your name, email, browsing history, or any account information — ever.
- We do not sell data. We do not run ads. We do not build profiles.

---

## What We Collect and Why

### 1. Prompt Text (conditionally, and only when weak)

When you type a prompt on a supported AI platform (ChatGPT, Claude, Gemini, or Perplexity), the extension scores it locally on your device using a lightweight algorithm. No network request is made during scoring.

If the score falls below 65 out of 100 — indicating the prompt is likely too vague or underspecified — and the extension is active in Suggest, Review, or Auto mode, the prompt text is sent to **our relay server** (hosted on Cloudflare Workers) for improvement. The relay forwards the text to the **Anthropic API**, which returns an improved version of the prompt.

**The relay does not log or store your prompt text.** It acts as a pass-through. The improved prompt is returned to your browser and displayed in the extension UI. Nothing is retained on the server after the response is delivered.

If your prompt scores 65 or above, it is never sent anywhere.

### 2. Invite Code

During the unlisted beta phase, access to the extension requires an invite code. The invite code you enter is stored locally in your browser's extension storage (`chrome.storage.local`) to unlock the extension. The invite code is also sent to the relay once at validation time to confirm it is valid. We do not associate your invite code with any personal identity.

### 3. Local Usage Counts

The extension stores a small amount of usage data locally in your browser — for example, how many prompts have been improved in your current session. This data never leaves your device and is used only to drive in-extension UI features (such as showing a usage count badge). It is not transmitted to us or any third party.

---

## Usage Analytics

When you interact with the Behtar chip (accepting, dismissing, or rating an improvement), the extension sends a small analytics event to our relay server. This event contains: the action taken (e.g. accepted, dismissed), the platform you were on (e.g. ChatGPT), the mode you had selected, your invite code (as an anonymous identifier), and the time taken to make the decision. This data is used solely for product improvement and is not linked to any personal identity. It is not sold or shared with third parties.

---

## What We Do NOT Collect

- No name, email address, or any account credentials
- No browsing history or URLs visited outside the four supported AI platforms
- No keystrokes, clipboard contents, or page content beyond the specific prompt input field
- No device identifiers, IP address logs, or fingerprinting data
- No payment information (the extension is free)

---

## Third-Party Services

### Anthropic API
When a weak prompt is detected, the text of that prompt is sent to the Anthropic API to generate an improved version. Anthropic's own privacy policy and terms of service govern how they handle data submitted through their API. You can review their policies at [https://www.anthropic.com/legal/privacy](https://www.anthropic.com/legal/privacy).

We send only the prompt text — no user identifiers, no account info, and no metadata about who you are.

### Cloudflare Workers
Our relay is hosted on Cloudflare Workers. Cloudflare may collect standard infrastructure-level data (such as request timestamps and region) as part of running their platform. We do not instruct Cloudflare to log prompt content. Cloudflare's privacy policy is available at [https://www.cloudflare.com/privacypolicy/](https://www.cloudflare.com/privacypolicy/).

---

## Data Storage

| Data | Where stored | Sent anywhere? |
|------|-------------|----------------|
| Prompt score result | In-memory only, discarded immediately | No |
| Prompt text (weak prompts only) | Not stored — sent transiently to relay | Yes, to relay/Anthropic — not retained |
| Invite code | `chrome.storage.local` on your device | Once, to validate |
| Usage counts | `chrome.storage.local` on your device | No |

---

## Your Rights

- **Access / Delete:** All locally stored data (invite code, usage counts) can be cleared by removing the extension from Chrome. Go to `chrome://extensions`, find Behtar, and click "Remove."
- **Opt out of improvement:** If you prefer that weak prompts are never sent for improvement, you can disable the extension at any time via the extension popup or `chrome://extensions`.
- **Contact:** For any privacy questions or requests, email **privacy@behtar.app**. We aim to respond within 7 business days.

---

## Children

This extension is not directed at children under 13. We do not knowingly collect any information from children.

---

## Changes to This Policy

If we make material changes to this policy, we will update the "Last updated" date at the top of this page and, where appropriate, provide notice via the extension or our website. Continued use of the extension after changes are posted constitutes your acceptance of the updated policy.

---

## Contact

**Behtar: Prompt Improver**
Email: privacy@behtar.app
Website: https://behtar.app
