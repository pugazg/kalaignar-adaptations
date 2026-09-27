# தாய் காவியம் — Archival Guidelines

This is the work-specific operating guide for `works/thaai-kaaviyam/`.

## 1. Controlling-source rule

> **The rendered source scan is the controlling source.**

The repository is a preservation layer, not a corrected or normalized edition.

Never silently:

- correct spelling, punctuation, names, numbers or lineation from another edition;
- modernize historical forms;
- reconstruct unclear letters from context;
- treat OCR, parsed text, external translations or model memory as source authority;
- merge printed text with handwriting, library stamps, bleed-through or scanner artefacts.

Use `needs-review`, `partial` or `blocked` rather than guessing.

## 2. Source identity and split-PDF rule

The supplied work is one bibliographic source represented operationally by **three split PDFs** because the original PDF is approximately **983.1 MB**.

Each split PDF is a provenance/access unit only.

Repository `scan_page` always means the **overall physical scan number across the complete work** and never restarts in a later split. `part_page` records the local page number inside that split.

Known now:

| Part | Local pages | Overall scans | State |
|---|---:|---:|---|
| 001 | 135 | 1–135 | supplied / intake complete |
| 002 | unknown until supplied | unknown until supplied | not supplied |
| 003 | unknown until supplied | unknown until supplied | not supplied |

Do not invent Part 002/003 filenames, local-page counts, printed-page boundaries, content, illustrations, continuity or final global extent before those files are supplied.

## 3. Source PDFs are not stored in GitHub

The split PDFs are controlling working sources and are not committed unless the user explicitly changes that policy.

Archive transcription, metadata, indexes, verification/audit records and project-created translation layers in GitHub.

## 4. Image-only / no-text-layer handling

Part 001 exposes no usable parsed text layer in the supplied file environment.

- inspect rendered page images directly;
- OCR may be a disposable aid only, never authority;
- do not fill unclear print from language knowledge or context;
- final source verification must compare repository text against rendered scans.

## 5. Page-aligned Tamil archive

Every physical scan must receive one page record, including covers, title/imprint matter, prefaces, illustrations, blank source-side pages and body pages.

Core status vocabulary:

- `not-started`
- `needs-review`
- `partial`
- `verified`
- `blocked`

Meaningful visual fidelity is tracked separately through `visual_fidelity`.

## 6. Work-specific fidelity

Preserve, when source-supported:

- poetic line breaks, stanza/block structure and deliberate spacing;
- section/chapter numbering and headings;
- dialogue/quotation marks and punctuation;
- running headers and printed page numbers as page furniture;
- illustration/text order and relationships;
- continuation across physical page boundaries;
- prefaces, signatures and publication matter as distinct page functions;
- handwriting, stamps and library marks separately from printed body text.

Do not convert the source into prose or silently smooth verse lineation.

## 7. Mandatory per-Part closure workflow

Finish the complete required workflow for the currently supplied Part before beginning the next Part:

1. **Source intake** — confirm local page count, overall scan range, source identity and visible boundaries.
2. **Pass 1: physical capture / transcription** — create the complete page-aligned Tamil record set.
3. **Pass 2A: direct textual verification** — compare wording, punctuation, lineation and metadata against rendered scans.
4. **Pass 2B: independent lexical-fidelity re-read** — only after Pass 2A covers the whole Part.
5. **Pass 3: meaningful visual-text verification** — headings, block relationships, page furniture, illustration/text relationships and continuations.
6. **Part audit** — physical coverage, continuity, source limits and supplied boundaries.
7. **Final metadata/status synchronization**.
8. **Documentation synchronization**.
9. **Tamil archival-ready checkpoint**.
10. **Project-created English workflow, when maintained**, only from audited Tamil records.
11. **Final Part closure** before the next Part begins.

A page is not finally source-verified merely because Pass 2A completed.

## 8. Cross-Part boundaries

The outgoing Part boundary is checked only when the adjacent Part source becomes available.

A boundary witness may be inspected to classify continuity, but witness text must not be captured into the wrong Part.

Use source-supported classifications such as:

- `CLEAN`
- `GENUINE CONTINUATION`
- `SOURCE-LIMITED`

Part 001 scan 135 is currently an unresolved outgoing boundary because Part 002 has not yet been supplied.

## 9. Batch discipline

Unless the user overrides it, use **10 physical scans per normal source-dependent iteration**, with a shorter final remainder.

For every batch:

1. fetch live `main`;
2. resolve the exact split PDF;
3. inspect source images directly;
4. fetch existing target records before writing;
5. transcribe/correct only source-supported visible material;
6. preserve overall scan numbering;
7. commit sequentially;
8. inspect the changed-file set;
9. synchronize progress, handover and next-chat frontier.

A workflow batch boundary never implies a narrative or verse boundary.

## 10. English layer

Any project-created English translation must be produced only from audited Tamil records and declare:

```yaml
translation_type: "project_translation"
```

Do not repair source uncertainty in English.

## 11. Current frontier

### Part 001 — scans 1–135

- source intake — **COMPLETE / PASS**;
- parsed text — **unusable / image-only handling**;
- scans 1–19 — front matter;
- scan 20 — main poetic body begins at printed page 1;
- scan 135 — printed page 116;
- outgoing 135→next — **UNRESOLVED pending Part 002**;
- Pass 1 — **NOT STARTED**.

### Exact next activity

**Part 001 Pass 1 — scans 1–10.**
