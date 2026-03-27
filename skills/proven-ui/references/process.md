# PROVEN UI — Page Build Process

Step-by-step workflow for designing and building PROVEN web pages. Every gate is a hard stop — do not proceed until approved. For single components or quick edits, skip this file entirely.

**Prerequisite:** Read the hub `SKILL.md` first.

---

## PM Handoff — What This Process Expects

**Input:** A PRD from `proven-pm` containing:

- **Audience** — which customer archetype(s), traffic source
- **Conversion goal** — single action
- **Emotional arc** — what the visitor feels arriving, what must be true to move forward, section by section
- **Information hierarchy** — what lands first viewport vs. below fold vs. supporting
- **Success metrics** — what good looks like
- **Constraints** — anything mandated or prohibited

If no PRD exists, request one before proceeding. Do not extract a brief from a conversation — the PM skill produces structured PRDs.

---

## The Workflow

```
PRD received
  → Step 1: Extract Design Brief
  → Step 2: Read Skills
  → Step 3: Map PRD to Section Vocabulary
  → Step 4: Section Architecture    ← Gate 1: approve before copy
  → Step 5: Copy by Section         ← Gate 2: approve before build
  → Step 6: HTML Build
  → Step 7: Brand QA                ← Gate 3: fix all failures before ship
  → Step 8: Fix by Section
```

---

### Step 1 — Extract a Design Brief from the PRD

Pull three things from the PRD before any design work:

- **Information hierarchy** — what lands first viewport vs. below fold vs. supporting
- **Emotional states per section** — what the visitor feels arriving, what must be true to move forward
- **Design constraints** — anything the PRD mandates or prohibits

---

### Step 2 — Read the Skills

Read in this order. No output until all are read.

1. `SKILL.md` (design rules, color, typography, principles, section vocabulary)
2. `references/tokens.md`
3. `references/frontend.md`
4. `proven-voice/SKILL.md`

---

### Step 3 — Map PRD Requirements to Section Vocabulary

Match every PRD requirement to a section type from the Section Vocabulary in `SKILL.md`. If a requirement doesn't map to an existing section type, flag it before building — do not invent new patterns without justification.

---

### Step 4 — Section Architecture (Gate 1)

Produce a section-by-section outline. No copy. No code. Each entry specifies:

- Section type (from section vocabulary)
- Evidence type (from evidence library)
- Emotional job (one sentence)
- Surface treatment (warm / cool / dark-warm / dark-cool / white)
- **Photography category + shot type** (from photography spectrum — e.g. "People Without Product · SKIN band · expression variant B" or "Catalog Product · CHROME band · Hero shot" or "None — interactive UI mockup")
- Headline direction (angle only, not final copy)
- Density tag (sparse / medium / dense)

The photography column is how images get produced. It tells the builder (or `proven-creative`) exactly what to generate. If it says "None," the section uses a designed object or rich typography instead.

Check before approving:
- Warm/cool rhythm — never stack more than two consecutive sections in the same register
- Photography variety — at least 3 different categories, no two adjacent sections using the same category
- Density alternation — no two adjacent sections with the same density tag
- Evidence variety — at least 5 distinct evidence types on landing pages

**Gate 1: Approve the architecture before writing any copy.**

---

### Step 5 — Copy by Section (Gate 2)

Write one section at a time using the `proven-voice` skill for tone and cadence. Approve each section before moving to the next. Apply the copy budget ceilings from `SKILL.md` — if a section needs more words, fix the visual, don't add copy.

**Gate 2: Approve all copy before the HTML build begins.**

---

### Step 6 — Build the HTML

Follow `references/frontend.md` for grid, breakpoints, component patterns, and animation implementation. Follow `references/tokens.md` for exact CSS values — type scale, spacing, gradients, glass, buttons, motion. Use only approved color tokens and component patterns from `SKILL.md`. Do not add elements or copy not in the approved architecture.

---

### Step 7 — Brand QA (Gate 3)

Run the full test suite below against the built page. Then run `proven-brand-qa` for Brand Lock Core checks and competitive testing.

**Gate 3: All failures fixed before the page ships.**

---

### Step 8 — Fix by Section

Fix failures one section at a time with targeted `str_replace` edits. Never rewrite the full page to address a section-level problem.

---

## Test Suite

For each test: pass or fail. If fail, name the element and the fix.

**Run in two phases.** Brand tests (1, 3, 4, 6–11, 13, 14) first. Fix all brand failures before running web-specific tests (2, 5, 12, 15).

1. **Principles test.** Does the page pass each of the 7 design principles? Run them as a checklist — remove-until-it-breaks, visual before verbal, copy budget, signal hierarchy. If any section fails a principle, fix the section — don't bend the principle.
2. **Hero test.** Does the hero follow the hero layout guide? One visual asset, one headline, one CTA, maximum negative space. If it has a subheadline that restates the headline, a second CTA, or no photography — fix it before reviewing anything else. Every page with a hero must implement one of the three Hero Layout Specifications (Layout A, B, or C) defined in `references/frontend.md` — not a freeform layout that approximates a hero. If the hero doesn't map cleanly to A, B, or C, that's the fix.
3. **Two-second test.** What does someone remember after two seconds? If nothing specific — typography isn't bold enough.
4. **Deletion test.** Remove an element. Still works? Remove it. Repeat until something breaks.
5. **Scroll test.** Does scrolling feel like turning pages in a story, or scrolling a webpage? If it feels like scrolling, the section pacing and visual variety aren't doing enough — add a breathing section or redistribute content density.
6. **Recognition test.** Does the reader feel *understood*, or *marketed to*?
7. **Brand test.** Could any competitor use this page? Start over.
8. **Data test.** Is every data point living inside a moment the user recognizes — not floating in its own section? And is it user-facing rather than brand-facing? If data is about PROVEN, flip it to be about the user.
9. **Squint test.** Squint at the page. If a card grid looks like a patchwork of colors, simplify to one card background.
10. **Readability test.** Check every text/background pair against WCAG AA (4.5:1 small, 3:1 large). If any muted text is below threshold, bump opacity by 0.1. Never sacrifice readability for aesthetics.
11. **Color count test.** Count non-text colors in any single section. If more than two, remove until two or fewer. The page should feel clean at a glance.
12. **Scan test.** Cover all body copy. Can a visitor understand what PROVEN does, why it's different, and what to do next — from headlines, numbers, and visual hierarchy alone? If no, the page is relying on words to do design's job. Add the visual. Cut the copy.
13. **Poster test.** If each section were a poster, would it work? One headline, one visual, nothing competing. If a section can't pass this test, something is present that shouldn't be. Remove it until the section has one job and one job only.
14. **Image test.** Are images present throughout the page, not clustered in one section and absent from others? No image-free stretch should leave the page feeling like a document. Chrome, skin, and ingredient photography carry material confidence — if a section feels flat or weightless, it needs a visual, not more copy.
15. **Mobile test.** Does the page work as a complete experience at mobile scale — not just technically, but holistically? Layout, hierarchy, pacing, and the recognition moment must all hold at 390px. If the page loses its character, feels cramped, or the hero doesn't land — rethink the layout, not just the breakpoints.

---

## Brief Template

```
PRD reference: [link or file]
Traffic source: [ad / email / organic / referral]
Conversion goal: [single action]
Proof points: [exact KB stats]
Avoid: [anything to flag]

Design brief (extracted from PRD):
- Information hierarchy: [first viewport → below fold → supporting]
- Emotional states: [by section — what visitor feels arriving, what must be true to move forward]
- Design constraints: [mandates / prohibitions]

Read in order: SKILL.md, tokens.md, frontend.md, proven-voice/SKILL.md.
Present section architecture only. Do not write copy or build until architecture is approved.
```
