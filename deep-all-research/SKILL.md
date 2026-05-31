---
name: deep-all-research
description: End-to-end bilingual deep web research workflow that turns a user-provided research object into a local Obsidian-ready knowledge folder with multiple Markdown notes, source links, credibility assessment, original downloadable attachments, synthesis, impact analysis, and verification. Use when the user asks to comprehensively research, collect, organize, investigate, map, analyze, or build a knowledge base about any topic, entity, event, technology, policy, product, person, company, market, controversy, or emerging concept. Search in both Chinese and English by default for broader international perspective, while producing the final report in the user's language unless requested otherwise.
---

# Deep All Research

## Outcome

Given only a research object from the user, produce a polished local research pack:

- A topic folder in the user's Obsidian vault when discoverable, otherwise in the current workspace.
- Multiple focused Markdown notes, not one giant report.
- Online webpage sources as direct URLs in notes.
- Local attachments only for source files that are naturally document artifacts: PDF, PPT/PPTX, DOC/DOCX, XLS/XLSX, CSV, datasets, images, audio/video when relevant.
- No saved HTML webpage files unless the user explicitly asks for offline webpage archives.
- A source inventory with credibility, bias, and evidence strength.
- A clear synthesis that separates verified facts, source claims, interpretations, disputes, impacts, and open questions.
- A bilingual collection process by default: search Chinese and English sources for broader international perspective, then synthesize them into one integrated report instead of separating by language.
- A final verification pass before reporting completion.

## Completion Criteria

Before final response, verify all of the following:

1. The output folder exists in the intended location.
2. Markdown notes exist and are non-empty.
3. Source links are present as clickable URLs.
4. The source inventory includes both Chinese and English search coverage unless the topic is language-specific or sources genuinely do not exist in one language.
5. There are no local `.html` or `.htm` webpage archives unless explicitly requested.
6. Attachments are only suitable artifact files, and referenced local attachments exist.
7. The notes include: overview, source/original-material map, concept explanation, multi-dimensional analysis, external evaluation/disputes, impact analysis, open questions, and source list.
8. The final answer tells the user what was created, where it is, what was verified, and any limitations.

## Workflow

### 1. Establish Target And Output Location

Infer the research object from the user request. Do not ask clarifying questions unless the object or destination is genuinely ambiguous.

Find the Obsidian vault:

- Prefer a user-specified path.
- Otherwise search likely home locations for `.obsidian`.
- Prefer a resource/technical-resource directory when it exists, such as `06.资源库/技术资源`, `资源库-技术资源`, `Resources/Technical`, or similar.
- If multiple plausible vaults exist, choose the most recently relevant one only if confident; otherwise ask one concise question.
- If no vault is found, create the research pack under the current working directory.

Create a topic folder with a clear, filesystem-safe name. Use subfolders:

```text
<topic>/
  00-index-and-overview.md
  01-what-it-is.md
  02-technical-or-domain-breakdown.md
  03-primary-sources-and-timeline.md
  04-external-evaluations-disputes-and-misreadings.md
  05-impact-map.md
  06-key-judgments-and-open-questions.md
  07-source-inventory-and-credibility.md
  attachments/
  primary-materials/
  reference-materials/
```

Localize filenames to the user's language when appropriate. For Chinese users, use Chinese note titles.

### 2. Form The Research Map

Do an initial broad bilingual search to answer:

- What exactly is the object?
- What names, aliases, spellings, translations, abbreviations, or mistaken names exist in Chinese and English?
- What date range matters?
- Which sources are primary, authoritative, secondary, commentary, market reaction, or low-quality?
- Which dimensions matter for this topic?

Build queries in both Chinese and English by default. Use translated names, official English names, romanizations, abbreviations, and likely international terminology. Do not present the final notes as separate "Chinese sources" and "English sources" sections unless that distinction is analytically important; integrate evidence by theme and cite sources naturally.

Then create a research matrix. Use the relevant dimensions only:

- Definition and origin.
- Timeline.
- Official or primary source claims.
- Technical/domain mechanism.
- Stakeholders and incentives.
- External evaluations.
- Criticism, disputes, misreadings, and misinformation.
- Market, industry, policy, social, academic, or operational impacts.
- Evidence gaps and future watchpoints.

### 3. Use Parallel Research When Allowed

If subagents are available and the user explicitly allows or requests parallel work, dispatch independent research subtasks. Good splits:

- Primary/original sources and downloadable artifacts.
- Chinese-language media commentary and public debate.
- English-language/international commentary and terminology.
- Impact analysis by industry, policy, market, technology, or stakeholder.

Each subagent should return links, dates, source type, summary, credibility, bias risk, and download recommendations. Do not let subagents write into the final folder unless you deliberately assign disjoint files.

### 4. Source Collection Rules

Always browse the web for current or source-sensitive research. Search in both Chinese and English unless the user explicitly restricts language or the topic is inherently single-language. Prioritize:

1. Official websites, filings, standards, papers, laws, reports, docs, conference pages.
2. Original speeches, interviews, transcripts, papers, slides, PDFs, datasets.
3. Reputable newsrooms and specialist media.
4. Expert commentary with named author and evidence.
5. Social media, forums, and anonymous commentary only as examples of discourse, not as core evidence.

For each important source capture:

- Title.
- Date.
- Author or organization.
- URL.
- Source type.
- Key claim.
- Evidence strength.
- Bias or limitation.
- Language and jurisdiction/region when relevant.

Use direct URLs for webpages in Markdown. Do not save webpages as local HTML files by default.

### 5. Download Rules

Download only durable source artifacts that are useful offline:

- PDF reports, papers, official notices, filings.
- PPT/PPTX presentations.
- DOC/DOCX documents.
- Spreadsheets, CSVs, datasets.
- Images or media when they are source evidence or primary assets.

Do not download ordinary web articles as HTML. If a webpage has a print/PDF version, prefer the PDF. If downloading fails, keep the source URL and note the limitation.

Name attachments with source, date, and short title:

```text
primary-materials/2026-05-25-Huawei-Tau-Scaling-Law.pdf
reference-materials/2026-05-28-Broker-Industry-Commentary.pdf
```

### 6. Write The Note Set

Use clear Markdown for Obsidian:

- Add short YAML frontmatter with `created`, `topic`, and `tags`.
- Use wiki links for local notes and attachments.
- Use direct Markdown/autolink URLs for webpages.
- Prefer tables for source inventories and comparison matrices.
- Keep claims traceable. Do not blend source claims with your conclusions.

Minimum note purposes:

1. **Index and overview**: reading order, one-paragraph thesis, key local attachments, key online links.
2. **What it is**: names, aliases, definition, origin, what it does and does not mean.
3. **Breakdown**: technical/domain mechanics in plain language plus deeper structure.
4. **Primary sources and timeline**: chronological source-backed account.
5. **External evaluations**: supportive, neutral, critical, market/public reactions, misreadings.
6. **Impact map**: effects by stakeholder and dimension.
7. **Judgments and open questions**: what is likely true, what is uncertain, what to track next.
8. **Source inventory**: all major sources with credibility and bias risk.

Add extra notes when the topic deserves them, but keep the pack navigable.

### 7. Analysis Standards

Use careful epistemic labeling:

- **Verified fact**: directly supported by primary or multiple reliable sources.
- **Source claim**: stated by a source but not independently verified.
- **Inference**: your reasoned conclusion from evidence.
- **Open question**: important but not yet answerable.
- **Misreading**: a common claim that overstates or distorts the evidence.

Explicitly separate:

- What happened.
- Who said it.
- What evidence supports it.
- How credible the evidence is.
- What remains unproven.

Avoid hype. Avoid flattening all sources into equal weight. Do not treat market reaction, PR, or commentary as technical validation.

### 8. Verification Pass

Run checks appropriate to the environment:

- List the folder tree.
- Count Markdown notes and attachments.
- Search for unfinished-work markers before delivery.
- Search for accidental local `.html`/`.htm` files.
- Search Markdown for links to local HTML files.
- Check that locally linked attachments exist.
- Spot-check major notes for source URLs and core claims.

If any check fails, fix it and rerun the check before final response.

### 9. Final Response

Respond in the user's language. For Chinese users, default to Chinese. Keep it concise and plain.

Include:

- The folder path or main index file.
- The number and type of notes created.
- The number and type of attachments saved.
- The most important conclusion or caveat.
- That bilingual Chinese/English source collection was included, or why one side was limited.
- What was verified.
- Any limitations, such as blocked downloads or unavailable primary materials.

Do not mention low-level implementation details unless the user asks.
