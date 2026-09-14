# kba-forge

A Joule Work Desktop skill for creating, updating, and reviewing SAP Knowledge Base Articles (KBAs) — with AQI scoring, CSG content standards enforcement, and local domain skill integration for technical accuracy.

## What it does

- **Create** — Draft a complete KBA (Symptom, Environment, Cause, Resolution, Keywords) from a plain-language scenario description
- **Update** — Revise an existing KBA based on requested changes
- **Review** — Score a KBA draft against the 8-point AQI criteria (Q1=20pts, Q2–Q7=10pts each, Q8=20pts) and output a structured improvement report
- **Technical accuracy check** — Automatically invokes matching local domain skills (e.g. payroll, tax) to verify technical content before drafting

## Installation

**Option A — via Extensions UI**

1. Open **Joule Work Desktop**
2. Go to **Extensions → Skills**
3. Find `kba-forge` and click **Add to Joule Work Desktop**

**Option B — manual install from this repo**

1. Clone this repo:
   ```
   git clone https://github.com/WANGLI0/kba-forge.git C:\Users\<your-username>\kba-forge
   ```
2. Open **Joule Work Desktop**
3. In the chat box, type:
   ```
   请帮我安装这个 skill：C:\Users\<your-username>\kba-forge\skills\kba-forge
   ```
   Replace `<your-username>` with your Windows username (e.g. `JohnDoe`)
4. Click **Confirm** in the dialog — installation complete
5. Verify: type `review this KBA` in the chat. If kba-forge responds, the skill is active.

## Updating to the latest version

**If you installed from this repo (Option B above):**

> **Important**: `git pull` only updates your local repo files. It does NOT automatically update the skill inside Joule. You must complete both steps below.

**Step 1 — Pull the latest files from GitHub**

```powershell
cd C:\Users\<your-username>\kba-forge
git pull origin main
```

**Step 2 — Reinstall the skill into Joule**

Open Joule Work Desktop and type in the chat box:
```
请帮我安装这个 skill：C:\Users\<your-username>\kba-forge\skills\kba-forge
```
Replace `<your-username>` with your Windows username. Click **Confirm**.

Joule will read the updated files from your local repo and overwrite the existing skill installation. Both steps are required every time you update.

**Changelog**

| Version | Date | Changes |
|---------|------|---------|
| v2.4.0 | 2026-09-14 | Added Q6 checks: H4 headings for scenario variants, bullet points for parallel information; Keywords rule: no module/component codes (e.g. PY-HK) |
| v2.3.0 | — | Initial release |

## Usage

Start a conversation and say:
- `"Review this KBA: [paste KBA content]"`
- `"Create a KBA about [topic]"`
- `"Update this KBA: [paste KBA content]"`

## Standards

Follows SAP KCS Content Standards Guide (SF HCM) and AQI Review Reference Guide v2.4.

## Author

Li Wang (I058758) — SAP SuccessFactors HCM Core & Pay China, Dalian

## License

Apache License 2.0
