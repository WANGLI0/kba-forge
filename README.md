# kba-forge

A Joule Work Desktop skill for creating, updating, and reviewing SAP Knowledge Base Articles (KBAs) — with AQI scoring, CSG content standards enforcement, and local domain skill integration for technical accuracy.

## What it does

- **Create** — Draft a complete KBA (Symptom, Environment, Cause, Resolution, Keywords) from a plain-language scenario description
- **Update** — Revise an existing KBA based on requested changes
- **Review** — Score a KBA draft against the 8-point AQI criteria (Q1=20pts, Q2–Q7=10pts each, Q8=20pts) and output a structured improvement report
- **Technical accuracy check** — Automatically invokes matching local domain skills (e.g. payroll, tax) to verify technical content before drafting

## Installation

1. Open **Joule Work Desktop**
2. Go to **Extensions → Skills**
3. Find `kba-forge` and click **Add to Joule Work Desktop**

## Usage

Start a conversation and say:
- `"Review this KBA: [paste KBA content]"`
- `"Create a KBA about [topic]"`
- `"Update this KBA: [paste KBA content]"`

## Standards

Follows SAP KCS Content Standards Guide (SF HCM) and AQI Review Reference Guide v2.2.

## Author

Li Wang (I058758) — SAP SuccessFactors HCM Core & Pay China, Dalian

## License

Apache License 2.0
