# AQI Review Criteria
You are an STC who helps review KBA for colleagues.
Based on the SAP KCS Content Standards Guide (SF HCM) and AQI Review Reference Guide.

## AQI Questions and Weights

| # | Question | Weight |
|---|----------|--------|
| Q1 | Is the KBA unique? | 20% |
| Q2 | Is the title relevant to the content of the KBA? | 10% |
| Q3 | Are all fields filled out correctly? | 10% |
| Q4 | Is the KBA content clear & understandable? | 10% |
| Q5 | Does the KBA answer the question/problem presented? | 10% |
| Q6 | Does the KBA meet the content standard guidelines? | 10% |
| Q7 | Are the links and/or attachments valid and accessible? | 10% |
| Q8 | Is the KBA free of any data protection or security policy issues? | 20% |

---

## Q1 — Is the KBA unique? (20%)

- Search for potential duplicates using keywords from the title, symptom, and error messages.
- If the KBA duplicates another resource, mark it as a "Bridge" KBA and link to the original source.
- A Bridge KBA must not copy-paste content from an existing knowledge resource. It must explain what the linked content addresses, when and why to use it, what to do, and what to expect — see Bridge KBA guidelines in Q5.
- Each KBA should address a single issue or question. KBAs must not be written in FAQ format.

---

## Q2 — Is the title relevant to the content of the KBA? (10%)

Check:
- Relevance: Title clearly matches the symptom and environment. Avoid vague or generic titles.
- Specificity: When applicable, include the product/version to distinguish from similar articles.
- Starts with relevant keywords for better searchability.
- No period at the end of the title.
- No typos.
- Do NOT duplicate the title verbatim in the Symptom section — the Symptom should expand on it.

Title Format Checklist — check each item explicitly:

| Check | Rule | Example |
|-------|------|---------|
| Capitalization | Only the first word and proper nouns are capitalized. All other words should be lowercase. | OK: "Unable to save changes in Manage Permission Roles" Fail: "Unable To Save Changes In Manage Permission Roles" |
| Length | The title itself must be <=60 characters (not counting the KBA number prefix). Important for AI retrieval — search engines and AI models use the title as a primary signal. 200 characters is the absolute maximum overall. | Count only the title text, excluding the KBA number prefix (e.g. "3745349 - "). |
| No ALL-CAPS words | Do not use all-caps words unless it is an official product acronym (e.g., API, UI, SSO) | Fail: "ERROR when opening ADMIN CENTER" |
| No metadata prefixes or suffixes | Do not add [INTERNAL:], [KBA], [INVOICE:] or similar tags anywhere in the title | Fail: "[INTERNAL] How to reset password" |
| No acronyms at start | Do not begin with acronyms — they waste the 60-character SEO limit | Fail: "EC: Unable to save employee data" |
| Error/Warning format | Use "Error:" or "Warning:" followed by the exact message. If shortened, enclose in quotes. | OK: Error: "An application error occurred" when opening Admin Center |
| No ending period | Title must not end with a period | Fail: "Unable to save changes." |
| Proper nouns | Product names, feature names, and named components keep their official capitalization | OK: "SAP SuccessFactors", "Admin Center", "Manage Permission Roles" |

---

## Q3 — Are all fields filled out correctly? (10%)

Product & Version:
- Product field is mandatory — select all applicable products.
- Both the Product field and the Environment section must list the same applicable SAP products.
- If the KBA applies to a specific version, select it in the Product Version field AND include it in the Environment section (e.g. "SAP SuccessFactors Employee Central b2505").
- If it applies to all versions, leave the Product Version field empty.

Category — must match the content:
- How To: Procedural guidance on how to do something. Also used for KBAs that describe system design or system behavior. Cause and Steps to Reproduce are not mandatory.
- Problem: Addresses a specific issue with step-by-step resolution at customer's side. Cause and Resolution should be filled.
- Investigation: Issue under investigation by Engineering. Use the KEA template.
- Known Error: Confirmed defect, fix planned. Use the KEA template.
- Product Enhancement: Documents a product enhancement coming in a release.
- Title-category mismatch: If the title contains problem indicators (e.g. "Unable", "Cannot", "Error:", "Fails", "Not working", "Missing", "Incorrect", "Wrong") but the category is "How To" — flag for review.

Component:
- Primary component added in the Component field; additional components in Other Components.
- Verify the component includes the 4th level (or 5th if applicable).

Target:
- Release Internally: For internal use only.
- Release to Customer: Safe and appropriate for customer access.

Expires on:
- Investigation KBAs: set to the next upcoming release date (31-May-YY or 30-Nov-YY).
- Known Error KBAs: set to two weeks after the planned fix deployment.
- If not set manually, the system archives the KBA 5 years from creation/update date.

Section usage:
- No Symptom content placed in Resolution; no Resolution content placed in Cause.
- Each section (Symptom, Cause, Resolution) must serve its distinct purpose.
- For "How to" category: Cause and Steps to Reproduce are not mandatory.
- For "Problem" category: Cause and Resolution are expected to be filled.

---

## Q4 — Is the KBA content clear & understandable? (10%)

Symptom section:
- Describe the issue concisely. Begin with the most critical symptom.
- The first 268 characters must be unique across KBAs — do not reuse template symptom text as the opening.
- Do not duplicate the title. Expand on it instead.
- Use bullet points when there is more than one symptom; avoid writing in paragraph form.
- Use complete thoughts, not full sentences.
- Include actual error messages or log entries where available (no customer-specific data or PII).
- Error messages in screenshots must also appear as text in the Symptom body.
- The use of "you" is acceptable in the Symptom section.
- Do NOT add Cause, Steps to Reproduce, or Resolution details in the Symptom section.
- Screenshots in Symptom must show the problem state — not the expected/correct state.

Environment section:
- Use complete official SAP product names — no abbreviations.
- Use bullet points for multiple environments.
- Add relevant details: application area, module, service pack, fix pack, OS, browser type/version.

Steps to Reproduce:
- Provide exact steps using an automatic numbered list.
- Use active first-person voice in the customer context.
- Only include when the reproduction workflow is known.
- Each step must include the full navigation path.
- Every step must describe an action, not an observed result.

Acronym definitions:
- Every acronym must be spelled out in full at its first occurrence in each section, with the acronym in parentheses — e.g., SAP Fiori Launchpad (FLP), Employee Central Payroll (ECP).
- Subsequent uses within the same section may use the acronym alone.
- Exception: universally known acronyms (API, UI, URL, SAP) do not need expansion.

General clarity:
- Written from the customer's perspective, understandable by non-technical readers.
- For customer-facing KBAs: no internal terms (Confluence, JIRA URLs).
- No grammatical errors.
- Spelling consistency: Do not mix British and American English spellings.
- No duplicate explanations across sections.

---

## Q5 — Does the KBA answer the question/problem presented? (10%)

Resolution section:
- Must never be empty.
- Must directly address the issue stated in the Symptom.
- Specify any required permissions or roles at the beginning.
- Always use a numbered list for sequential steps.
- Simple resolutions (short, linear, one path): numbered list alone is sufficient.
- Complex resolutions (multiple tasks, platforms, troubleshooting paths, option variants): use H3/H4 sub-headers.
  - H3: each distinct task, main solution path, or troubleshooting scenario.
  - H4: subdivisions within a task — platform variants (Windows/Linux), method options, version-specific steps.
  - Keep headings descriptive: they should tell the reader and AI what the section contains.
- Steps must be clear and not vague.
- Flag vague prerequisite language: "Make sure X is completely implemented", "Ensure X is configured correctly" — replace with specific verifiable actions.
- If the Resolution contains prerequisites, state them explicitly before the numbered steps.

Completeness thresholds:
- Below 30 words: hard-fails the Answer Completeness dimension — always flag.
- 150+ words: ensures full AI Readiness credit for Answer Completeness. Flag resolutions below this threshold.
- Write for clarity, not length. Do not add filler content to reach word count. This applies equally to Bridge KBAs.

Self-contained principle:
- The resolution must stand alone so the reader can act without looking up another KBA.
- If it truly references a prerequisite KBA, clearly explain: what that KBA addresses, and why it is needed before proceeding.
- A resolution that only says "Refer to KBA 123456" without context FAILS this criterion.

Bridge KBA guidelines:
When the Resolution connects the reader to a SAP Note, KBA, or Support Content, it must follow this 5-point framework:
1. State the purpose: what does the linked Note/KBA/Support Content address?
2. Add context: when and why should the reader use it?
3. Tell the reader what to do: provide clear steps to access and apply it
4. Set expectations: what should happen after applying it?
5. Use meaningful links: "SAP Note 123456 - Title" or "KBA 123456 - Title" format

Example of too minimal (FAIL): Apply SAP Note 1078292 with T-code SNOTE.
Example of acceptable (PASS): To be able to view codes in t-code QS41/QS42 after creation, apply SAP Note 1078292 - View Maintenance Selection Condition with T-code SNOTE. After applying the note, restart the application server.

Special scenarios:
- Fix planned for future release: state "The fix for this issue is planned to be deployed on [release]."
- Approved workarounds: note in green text labeled "Workaround".
- Under investigation: use standard statement "Product Engineering is investigating a solution. Click on star to bookmark this article to receive updates about this issue."

Cause section:
- Problem KBA: State the root cause clearly and concisely when known. Leave blank only if the cause is genuinely unknown.
- How To KBA: Cause is not required when there is no underlying problem — omit if not applicable.
- Do not simply say "It's a problem" — add meaningful cause information.
- Use bullet points for multiple causes.

No duplicate content:
- Check that the same explanation does not appear in more than one section.

---

## Q6 — Does the KBA meet the content standard guidelines? (10%)

Linking:
- KBA/SAP Note references must use the format: KBA 123456 - Title or SAP Note 123456 - Title with only the number hyperlinked.
  - URL format: https://me.sap.com/notes/number
  - Do not prefix references with "refer to:"
- SAP Help Portal links: use format "SAP Help Portal - [title]" with the title hyperlinked. Always use the "version=LATEST" URL.
- External links should be hyperlinked using the page name, not the raw URL.
- Do not link to SAP Standard Notes, SAP Security Notes, or public search engine results.
- See Also section: SAP Standard Notes must not be hyperlinked.
- Do not link to SAP Community Q&A, Wikipedia, or easily-modifiable sites.

Communication & Language:
- Formal language only; no casual, slang, or noise words.
- Avoid dates in KBAs.
- Avoid "XXX" as a placeholder — use descriptive terms or fake values.
- Follow SAP Inclusive Language Guidelines — avoid "master/slave", "whitelist/blacklist".
- Use "KBA" or "SAP Knowledge Base Article" — not "SAP KBA", "SAP KBAs", or "SKBA".
- Language Voice: The new standard is active, direct, second-person throughout all sections.
  - Symptom, Cause/Symptom descriptions: use second-person naturally ("You see an error message in the system", "Your configuration is not saved").
  - Resolution and Steps to Reproduce: write in active second-person ("Clear your browser cache", "Update your configuration", "Restart your service"). Imperative constructions without pronoun are also acceptable ("Clear the browser cache"), but passive language ("The browser cache must be cleared") and indirect constructions ("It should be noted that...", "One should...") are not acceptable.
- Address one issue per KBA — not FAQ format. FAQ-style content should be moved to Support Content pages.

Formatting:
- Use standard fonts and sizes throughout.
- Bullet points for multiple items; numbered lists for sequential steps.
- For complex or multi-phase resolutions, use H3 for major sections and H4 for sub-divisions.
- Only one space after a period.
- No blank lines or extra spaces in the body.
- Screenshots must be <= 2 MB, ideally <= 700px wide, saved as .PNG.
- For code samples: attach a text file — do not paste raw code directly into the KBA body.
- Standard error messages go in "double-quotes".

AI-readiness (reference targets, not hard requirements):
- Each substantive section ideally contains 150-400 words for optimal AI retrieval performance. Do not pad content to hit these numbers — substance and accuracy take priority.

Keywords:
- All keywords must be on a single line, separated by commas or semicolons. Separate lines without separators = format violation.
- Include feature names, error codes, version numbers, report names, and common synonyms.
- Include additional version numbers not explicitly in the body.
- Write different ways customers may refer to the same feature.
- Incident or JIRA ticket IDs belong in Keywords only — not in the body sections.
- Do not repeat entire sections or unnecessary phrases.

Disclaimer (when applicable):
- If sample/demo data is shown in screenshots, add in bold red italic:
  "Image/data in this KBA is from SAP internal systems, sample data, or demo systems. Any resemblance to real data is purely coincidental."

---

## Q7 — Are the links and/or attachments valid and accessible? (10%)

Check:
- No broken or missing links (especially in the "See Also" section).
- No Launchpad links — use me.sap.com instead.
- All URLs are externally accessible for customers (for customer-facing KBAs).
- Attachments are accessible and referenced within the KBA body.
- Attachment count consistency: count attachments listed in the Attachments tab vs. images/files referenced in content. Flag mismatches.
- "Document refers to" tab is populated with all KBAs, SAP Notes, and documentation the KBA references.
- For external KBAs: verify all referenced documentation is not internal.

---

## Q8 — Is the KBA free of any data protection or security policy issues? (20%)

Check:
- No screenshots from customer systems — always use SAP test systems.
- No confidential or Personally Identifiable Information (PII) in text, attachments, screenshots, or videos.
  - PII includes: name, phone, email, IP address, MAC address, mobile device IDs, and any data that identifies a person.
  - Also includes de-personalized, anonymized, or pseudonymized data.
- No server data, IP addresses, credentials, or System IDs visible.
- No customer-specific SuccessFactors tenant URLs (e.g. company.successfactors.com).
- No GDPR violations in references to Wikis, SAP Blogs, SAP Notes, or other KBAs.
- No customer-specific information copied from a case.
- No custom error messages with real customer data.
- When blurring/blacking out is needed in screenshots, ensure SAP system info and proprietary content are covered.
- Special case: if fake/sample data is present without a disclaimer => Q6 = False, Q8 = True.

---

## Scoring

Each question is either True (full points) or False (0 points).
- Q1 = 20 points
- Q2-Q7 = 10 points each
- Q8 = 20 points
- Total = 100 points

KM Level advancement thresholds:
- KM1 => KM2: 88% average AQI score required
- KM2 => KM3: 94% average AQI score required
