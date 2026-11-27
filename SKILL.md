---
name: elucidate
description: >-
  Auto-use whenever the user asks to rewrite, tighten, shorten, clarify, explain, summarize,
  digest, or organize text, specs, or notes. Losslessly compresses verbose tech specs, RFCs, PRs,
  and code reviews without dropping decisions or constraints; explains concepts tailored to the
  audience; summarizes books/articles/docs/transcripts; and organizes messy notes into atomic,
  actionable (PARA) structure. Do not use for writing application code, debugging, or simple
  factual lookups.
---

# Elucidate

Transform dense, scattered, or jargon-heavy input into high-signal output tailored to the reader.

<invariants>
1. Infer the task and audience directly from the request; never ask the user to choose a mode or framework.
2. When rewriting specs, RFCs, PRs, or code reviews, inventory every decision, owner/component, threshold, constraint, failure mode, and edge case first—preserve 100% of them unchanged.
3. Keep normative terms (`must`, `never`, exact limits, status codes, TTLs) exact; never soften requirements into vague prose.
4. Load [frameworks.md](./references/frameworks.md) only when handling long multi-part specs, full document summaries, or large note restructures.
</invariants>

<routing>
Select the matching workflow (stack them if a request spans multiple jobs):

1. **Tighten tech specs, RFCs, PRs, or code reviews** -> run `<lossless_tech_rewrite>`
2. **Explain concepts, write proposals, emails, or pitches** -> run `<audience_explanation>`
3. **Summarize books, docs, papers, or transcripts** -> run `<skeleton_digest>`
4. **Organize messy notes, brainstorms, or research dumps** -> run `<atomic_organize>`
</routing>

<execution_rules>

<lossless_tech_rewrite>
*(Style + Paramedic Method + Smart Brevity)*
1. Extract a mental checklist of every fact, constraint, owner, and edge case from the source.
2. Rewrite sentences using **explicit Actor + strong Action verb**; eliminate passive voice, nominalizations, and prepositional wind-ups.
3. Structure output for a 10-second scan:
   - `**Change / Decision:**` (1 line) and `**Why / Risk:**` (1 line).
   - Group rules, limits, failure modes, and trade-offs into **bold-lead-in bullets**.
4. For code review comments, emit one point per comment: `**Issue / Risk** — <exact behavior>. **Fix:** <concrete change>.` Prefix non-blocking items with `nit:` or `optional:`.
</lossless_tech_rewrite>

<audience_explanation>
*(Pyramid Principle + Art of Explanation + Made to Stick)*
Match delivery to the listener's bottleneck:
- **Decision-makers / peers / proposals:** Lead with the governing conclusion (or brief SCQA framing), then group 2–5 non-overlapping (MECE) points in consistent order.
- **Beginners / non-technical stakeholders:** State why it matters before how it works; anchor to one familiar analogy; explain at intuitive depth (A-to-G) and translate unavoidable jargon immediately.
- **Persuasive pitches / talks:** Strip to one core message; defeat the Curse of Knowledge by replacing abstractions with concrete, sensory examples or a short story.
- **Mixed or complex audience (default):** Open with 1–2 sentences of context/analogy -> state the top-down conclusion and MECE points -> ground each abstract point with one concrete example.
</audience_explanation>

<skeleton_digest>
*(How to Read a Book + Progressive Summarization)*
1. **Executive Summary:** State the source's core thesis/problem and answer in 2–3 sentences at the top.
2. **Structural Skeleton:** Map the 3–5 major parts and how they advance the core argument.
3. **Key Terms & Claims:** Define pivotal terms plainly and list supporting propositions/evidence.
4. **Skimmable Emphasis:** **Bold** the sharpest takeaway inside each section and end with concrete action items.
</skeleton_digest>

<atomic_organize>
*(How to Take Smart Notes + PARA)*
1. Split multi-topic dumps into **atomic notes** (one self-contained idea per block), rewritten in clear own words.
2. Give each note a **claim-based title** (insight, not generic topic) and link related notes with relationship labels (`supports`, `contrasts`, `extends`).
3. When organizing folders, tasks, or workspaces, sort by actionability using **PARA**: `Projects` (active deadline) -> `Areas` (ongoing responsibility) -> `Resources` (reference) -> `Archives` (inactive).
</atomic_organize>

</execution_rules>

<verification>
Before responding, confirm:
- **Zero loss:** Every original decision, metric, constraint, and edge case survived intact.
- **Front-loaded:** A busy reader gets the main conclusion or change in the first two lines.
- **Zero filler:** No throat-clearing, overlapping bullets, or unexplained jargon for the target reader.
</verification>
