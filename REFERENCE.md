# Reference: Grab merchant HC drafts

## CDC cover table (template)

Copy and fill. Row set aligns with common SG Help Centre update drafts; drop or rename rows if the user’s template differs (e.g. BCRS uses **Localised screenshots** / **Regional stakeholder review details**—merge into the closest row).

```markdown
**(To be filled out by CDC) Template**
**Please include this table in the first page of your document.**

| Jira link |  |  |
| ----- | :---- | :---- |
| **Brand** |  |  |
| **Article ID**  |  |  |
| **Title** |  |  |
| **Category \> Section** |  |  |
| **Type of article** |  |  |
| **Article link (for existing articles)** |  |  |
| **Rollout countries & dates** |  |  |
| **Resources** |  |  |
| **Regional stakeholder review** |  |  |
| **Initial draft** |  |  |
| **Final draft** |  |  |
```

Optional rows seen in some drafts: **Localised screenshots**, **Initial draft** / **Final draft** as two stakeholder columns.

## FAQ / accordion markers (CMS-style)

When the source draft uses expandable sections, **preserve verbatim** unless the user asks to strip CMS syntax:

```markdown
**➤**Section title \<Tap to expand hidden content\>
...content...
\<End of hidden content\>
```

MQP-style inline FAQs often use:

```markdown
**\> What is the programme?**
Answer paragraph…
```

## Consumer vs customer (enforced)

| Meaning | Term |
|---------|------|
| Person who orders on Grab / uses consumer apps | **Consumer** / **consumers** |
| Grab restaurant or store on the platform | **Merchant** / **merchants** / Merchant-Partner |
| Verbatim quote or non-Grab legal text | Leave unchanged only if user requires verbatim |

**Never** use **customer** for Grab end users in drafted or revised HC copy. If the source draft says "customer", rewrite to **consumer** when producing output.

## Style quick reference

- **British English** throughout for SG (and other UK-English markets).
- **Dates:** `12 Mar 2026` not `12th Mar 2026`.
- **Times:** `10AM-11AM`, `3PM-5.30PM` (no `2000h`; consistent AM/PM casing per slide).
- **Discount line (promo):** `70% OFF`.
- **First mention:** Grab Merchant Centre (GMC), then GMC.

## Word-native output format (default)

For final delivery, save a local `.docx` with native Word styling (not markdown-like formatting pasted into Word).

- **Heading styles:** apply `Heading 1` for article title, `Heading 2` for major sections, `Heading 3` for subsection FAQs where needed.
- **Body style:** use normal paragraph style for running copy with clean spacing.
- **CDC metadata table:** use a real Word table with visible borders, consistent cell padding, left alignment, and a distinct header row style.
- **Lists:** use Word bullet/number list styles (do not fake with manual symbols).
- **Links:** keep URLs as clickable hyperlinks.

Suggested filename pattern: `<country>-<article-id>-<short-title>.docx`.

## Primary reference draft file

Use this consolidated source first for structure calibration and house style:

- `REF DRAFT FOR SKILL (1).md`

Path handling rules:

- Prefer the exact path provided by the user in the current request.
- Avoid hardcoding user-specific absolute paths.
- If the file is large, use Grep / partial Read (offset + limit) before deep edits.

## Comms send timing (merchant notifications)

If the user asks about **when to send** pushes/WA/EDM (not HC article body): prefer **non-peak** windows such as **10AM–11AM** and **3PM–5PM** where that guidance applies.
