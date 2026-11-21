# LinkedIn Outreach AI (v3.2.0) — Product & Engineering Upgrade

An AI-powered Chrome Extension (Manifest V3) that turns scraped LinkedIn profiles and cached PDF resumes into structured, channel-compliant outreach notes and DMs—with one-click LinkedIn DOM injection.

## Product & Engineering Upgrades

| Area | Baseline Starter | Upgraded Build (v3.2.0) | User & Product Impact |
| :--- | :--- | :--- | :--- |
| **3-Layer AI Pipeline** | Stubbed mock responses in Deep Mode | Structured JSON extraction across **L1 (Profile Intelligence)**, **L2 (Hook & Fit Extractor)**, and **L3 (Structured Writer)** with interactive hook checkboxes | Gives users human-in-the-loop control over personalization angles |
| **Multimodal Resume Caching** | PDF saved in storage but never sent to AI | Native Claude `document` block parsing cached into reusable sender skills & highlights | Grounds drafts & **Profile Fit** matching without per-request token bloat |
| **Structured Copywriting** | Generic text dump with no explanation | Modular anatomy (**Greeting → Hook → Bridge → CTA → Sign-off**) + **Strategy Insight Bar** | Higher reply conversion and transparent AI reasoning |
| **Channel Guardrails** | No length awareness | Dual **Note (300 chars)** & **DM (600 chars)** modes with live counter & AI **Shorten to fit** | Prevents LinkedIn connection-note truncation |
| **LinkedIn DOM Injection** | Manual copy-paste only | Multi-frame (`all_frames`) + Shadow DOM (`#interop-outlet`) piercing with React-safe input events | One-click auto-insertion into *Add a note* and *Message* composers |
| **Zero-Friction Dual Mode** | Activation-key friction | Works out-of-the-box in **Free Mode** (local heuristics) and upgrades seamlessly with user's Anthropic API key | Zero-setup reliability for any user |

## Quick Setup
1. Open `chrome://extensions` and enable **Developer mode**.
2. Click **Load unpacked** and select this folder.
3. Open any `linkedin.com/in/...` profile, configure your bio/PDF resume in **Settings**, and click **Scrape + Enrich (L1 + L2)**.
