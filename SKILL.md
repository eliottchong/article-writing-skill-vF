---
name: grab-merchant-articles
description: >-
  Drafts or revises Grab merchant-facing Help Centre articles and aligned CDC drafts.
  Use when the user asks for Help Centre copy, CDC article updates, GrabMerchant or
  Grab Merchant Centre (GMC) guides, SG/regional rollout notices, FAQ accordions, or
  GrabFood/GrabMart merchant help content. Triggers on paths or mentions of help.grab.com/merchant,
  article IDs, Jira CDC/GSS tickets, or "Help Centre update". Do not use for non-Grab
  products, consumer-app-only UX (no merchant angle), legal sign-off as final authority,
  or languages/markets the user did not specify—ask for market and article type if missing.
  Default final deliverable is a locally saved .docx with clean Word-native styles unless
  the user explicitly requests markdown/plain text only.
metadata:
  category: content
---

# Grab merchant Help Centre articles

Behaviour guide for merchant-facing Help Centre (HC) and CDC-style drafts. Treat [REFERENCE.md](REFERENCE.md) for paste-in templates and term tables.

## Decision router

What did the user give you?

| Input | Action |
|-------|--------|
| Missing any of: **subject matter**, **context**, or **>=1 reference material** | **Do not draft yet.** Ask for the missing items and wait. |
| Path or paste of an **existing** draft | **Revise**: preserve CDC table, CMS markers (`\<Tap to expand\>`, hidden blocks), `![][imageN]`, `~~strikethrough~~` unless they ask to finalise/clean. |
| **Net-new** topic + specs (Jira, rollout, key facts) | **Draft**: open with CDC cover table (see REFERENCE), then body. |
| User references **Help Centre Update** files in Downloads | **Evidence first**: read those files (partial read; see below). |
| **FAQ / announcement / programme explainer** | Use accordion-style FAQ blocks only if the user or template expects them; otherwise use clear headings and `**> Question**` style FAQs like the MQP examples. |
| No output format specified | Produce article in **.docx** as the final local file. |
| User explicitly asks for markdown/plain text only | Follow requested plain format and skip docx packaging. |

If **market** (e.g. SG) or **article type** is unclear, ask one short question before writing long copy.

## Workflow

1. **Mandatory intake gate (always)**: before writing any article copy, verify the user has provided all three:
   - **Subject matter** (what the article is about)
   - **Context** (audience/use-case, rollout, or objective)
   - **At least 1 reference material** (file, link, ticket, or pasted source text)
   If any one is missing, **re-prompt for missing items only** and do not draft yet.
2. Confirm **audience**: default is **merchant** readers on the Help Centre unless the user says otherwise.
3. If the doc is CDC-tracked, **lead with the CDC metadata table** (REFERENCE template). Fill known cells from user/Jira; use placeholders for unknowns.
4. For **updates**, include the line: `**NEW CONTENT highlighted in yellow**` when the user is following that house style (omit if they say it is final/publish-ready).
5. **Body**: benefit-led, actionable steps, British English, sentence case for body copy. Define **Grab Merchant Centre (GMC)** on first use, then **GMC** is acceptable.
6. **Images**: do not delete or rewrite `![][imageN]` (or equivalent) unless the user asks. For new screenshots, note placeholders and suggest approved sources (templatised MEX comms KVs, icon stock library) in comments or a short "Assets" note if useful.
7. **Regulatory or policy claims**: only state what the user or linked Jira/spec provided. If unknown, say Grab will share more detail later—do not invent dates or legal obligations.
8. **Final packaging (default)**: save the final article locally as a `.docx` file for direct editing/publishing.
   - Use **Word-native heading styles** (`Heading 1`, `Heading 2`, `Heading 3`) instead of manual bold-only headings.
   - Apply **real table styling** for CDC metadata tables (header emphasis, borders, alignment, readable cell padding), not plain text tables.
   - Preserve links as clickable hyperlinks.
   - If a path is not provided, save under a predictable local path such as `outputs/<article-slug>.docx`.

## Evidence: reference drafts

When calibrating structure, tone, or CDC layout, use the **consolidated reference draft** first:

- `REF DRAFT FOR SKILL (1).md` (or the latest equivalent file the user provides)

Do not rely on a user-specific absolute path. Use the path provided in the current request, or search common locations (workspace/Downloads) when needed.

**Large files (embedded images):**

1. **Grep** first for: `Jira link`, `Article ID`, headings, `NEW CONTENT`, `Tap to expand`, `![][image`.
2. **Read** with **offset + limit** for the prose sections you need.
3. Never assume you saw the full file if Read was partial—cite that you sampled lines N–M if relevant.
4. If the consolidated reference file is missing, ask the user for the correct file path before drafting.

## Mandatory: consumer vs customer (end users)

- **End users** of the Grab marketplace (people who place orders or use the consumer experience): always **consumer** / **consumers**. **Never** **customer** / **customers** for that meaning.
- **Merchants** remain **merchant** / **merchants** / **Merchant-Partner** per comms guidance.
- **Exceptions (rare):**
  - Verbatim **legal or third-party** quoted text the user forbids changing.
  - **B2B** sense: the merchant’s own shop **customers** as a generic business term—prefer rephrasing to avoid confusion (e.g. "your guests" / "dine-in patrons") where Grab **consumers** are not meant.

When revising legacy drafts that say "customer" for end users, **rewrite to consumer** in all new or edited sentences and list any unchanged quoted lines separately if needed.

## Style constraints (Grab MEX comms alignment)

| Area | Rule |
|------|------|
| Tone | Clear, plain language; actionable steps; benefit-led; friendly, professional. |
| English | **British** (e.g. prioritise, organisation, programme). |
| Addressing partners | **Merchant-Partner**, **Delivery-Partners**; product names: **GrabMerchant App**, **GrabMerchant Portal**. |
| End users | **Consumers** only (see above). |
| Dates | `1 Jan 2023` style—not `1st Jan 2023`. |
| Times | `8AM-8.30AM`—not `8.00`, `2000h`, or lowercase `8am`. |
| Discounts in promo-style copy | `70% OFF`—not `70% off`. |
| Body headings | **Sentence case** for running copy; table-driven titles can follow CDC. |

## Anti-patterns

- Generating article content before collecting **subject matter + context + >=1 reference**.
- **Customer** for Grab end users.
- US spelling in SG (or other UK-English markets) copy unless the user specifies US English for that market.
- **MEX** / **DAX** in **merchant-facing** article body—use approved partner-facing terms instead.
- Stripping `~~…~~`, accordion markers, or image refs during a "light edit".
- Fabricating rollout dates, commission rules, or regulatory detail.

## Done when (quality bar)

- [ ] Intake gate passed: subject matter, context, and >=1 reference material are provided.
- [ ] CDC table present when applicable; placeholders only where data is truly unknown.
- [ ] British English; approved product/partner naming.
- [ ] **No "customer/customers" for Grab end users** in produced copy (grep your own output mentally).
- [ ] Clear next steps for merchants where the topic requires action.
- [ ] CMS/special markers preserved when editing existing drafts.
- [ ] No invented policy; assumptions called out or omitted.
- [ ] Final output is saved locally as a **.docx** (unless user requested non-docx output).
- [ ] Heading hierarchy uses Word heading styles; metadata table uses proper Word table formatting.

## Worked example (synthetic fragment)

**Input:** "SG Help Centre update: new toggle in GrabMerchant App to pause breakfast items. Jira GSS-9999. Article 40009999. Category Help Centre > GrabMart > Manage Catalogue."

**Output (excerpt):**

```markdown
**(To be filled out by CDC) Template**
**Please include this table in the first page of your document.**

| Jira link | https://grabtaxi.atlassian.net/browse/GSS-9999 |  |
| ----- | :---- | :---- |
| **Brand** |  |  |
| **Article ID**  | 40009999 |  |
| **Title** | *How to pause breakfast items on GrabMart* |  |
| **Category \> Section** | *Help Centre \> GrabMart \> Manage Catalogue* |  |
| **Type of article** |  |  |
| **Article link (for existing articles)** |  |  |
| **Rollout countries & dates** | *Singapore* |  |
| **Resources** |  |  |
| **Regional stakeholder review** |  |  |
| **Initial draft** |  |  |
| **Final draft** |  |  |

**NEW CONTENT highlighted in yellow**

**How to pause breakfast items**

You can temporarily hide breakfast SKUs from **consumers** during lunch and dinner hours so your catalogue stays accurate. Open the **GrabMerchant App**, go to [relevant menu path], and switch **Breakfast availability** to off for the hours you choose. Changes apply after you save.

If a **consumer** has already started an order containing a breakfast-only item, [complete with policy from your ticket—do not invent].
```

Note: bracketed instructions remind the agent not to invent policy.
