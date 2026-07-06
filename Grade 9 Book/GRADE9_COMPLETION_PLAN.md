# Grade 9 (2026秋 PEP) — Completion Plan

Source: `26秋人教英语9上清晰彩版(1).pdf` (140 pp, scanned).  
Book page ≈ PDF page − 8.

## Status snapshot (2026-07-06)

| Area | Status |
|------|--------|
| Vocabulary Units 1–8 | ✅ ~45–76 words/unit, examples + audio |
| Listening scripts | ✅ Units 1–8 conversations + TTS audio |
| Listening MC questions | ✅ Units 1–8 graded/open prompts |
| Listening fill-table / blanks | ✅ Units 1, 3–7 fill exercises; U8 T/F MC |
| Unit titles | ✅ Textbook names U1–8 |
| word-links derivations | ✅ 160 families (20/unit) |
| word-links compounds | ✅ U1–8 (~34 entries) |
| Grammar sections | ✅ passive / object / relative clauses |
| Reading Plus | ❌ not in app |
| Essential (appendix **bold**) | 🔄 U1 calibrated; U2–8 pending |
| PDF tooling / source map | ✅ `_source_map.json` + `grade9:pdf-pages` |

---

## Phase 0 — Source of truth ✅

- [x] `_source_map.json` — PDF path, page map, unit metadata
- [x] `scripts/grade9-pdf-pages.mjs` — render book pages to `.tmp/grade9-pdf/`
- [x] PDF on Desktop (not in git)

## Phase 1 — Align metadata ✅

- [x] Unit titles → textbook names in `Unit_XX.json` + `grade9-vocab-3-8-data.mjs`

## Phase 2 — Listening structured exercises ✅

App: optional **Action** column on `fill_table`; new **`fill_blanks`** type.

| Unit | Conversation | Textbook | Exercise type | Status |
|------|--------------|----------|---------------|--------|
| 1 | 2b/2c (id 3) | p.3 Past/Action/Present | fill_table 3-col | ✅ |
| 2 | 2c (id 3) | p.13 word-choice notes | graded MC | ⏭️ optional |
| 3 | 4 (id 4) | p.23 club chart 2b | fill_blanks | ✅ |
| 4 | 3 (id 3) | p.33 Professor 2c | fill_blanks | ✅ |
| 5 | 3 (id 3) | p.43 3D printer 2b | fill_blanks | ✅ |
| 6 | 2 (id 2) | p.53 Life in Space 2c | fill_blanks | ✅ |
| 7 | 2 (id 2) | p.63 Chinese Dragon 2c | fill_blanks | ✅ |
| 8 | 4 (id 4) | p.73 relay 2c | graded T/F MC (6 items) | ✅ |

Scripts: `grade9-listening-fill-exercises.mjs` merged by `grade9-listening-*.mjs`.

## Phase 3 — Vocabulary audit (in progress)

Textbook marks 重点词汇 in **bold**, not `*`.

- [x] Render appendix PDF pages 107–122 → `.tmp/grade9-pdf/`
- [x] OCR → `.tmp/grade9-vocab-ocr/` (tesseract eng)
- [x] `scripts/audit-grade9-vocab.mjs` — JSON vs OCR headword coverage
- [x] Unit 1: no missing headwords; `essential` calibrated from appendix bold
- [x] Scripts: `grade9-essential-data.mjs` + `apply-grade9-essential.mjs`
- [ ] Units 2–8: calibrate `essential` from appendix bold
- [ ] Regenerate audio only if headwords added

## Phase 4 — word-links compounds ✅

- [x] Curate `Unit_XX.compounds.json` for transparent compounds
- [x] Scripts: `grade9-compounds-data.mjs` + `npm run grade9:compounds`
- Coverage: U1 (8, existing) · U2 (2) · U3 (7) · U4 (5) · U5 (3) · U6 (2) · U7 (3) · U8 (4)

## Phase 5 — Expand derivations ✅

- [x] Grow `grade9-derivations-data.mjs` to 20 families/unit (160 total)
- [ ] Prioritise remaining essential headwords without families (ongoing polish)

## Phase 6 — Optional / later

- [ ] Reading Plus (p.81+) as optional reading mode
- [ ] Grammar inline practice tied to textbook page refs
- [ ] Mobile nav polish, PWA update QA

---

## Execution order

**Done:** P0–P2, P4, P5 · P3 OCR + Unit 1 essential  
**Next:** Finish P3 essentials for U2–8 · optional Reading Plus
