---
name: elucidate
description: >-
  Summarizes dense material, organizes scattered notes/knowledge, tightens verbose tech specs and
  code reviews without losing any decisions or constraints, and structures explanations for clarity
  using The Pyramid Principle, The Art of Explanation, Made to Stick, How to Read a Book, How to
  Take Smart Notes, Building a Second Brain, Style, Revising Prose, and Smart Brevity. Use when
  the user asks to explain a concept, summarize a book/article/doc, tighten a verbose spec/RFC/PR
  or code review concisely without dropping details, organize messy notes, or rewrite drafts.
---

# Elucidate

Turn complex information into clear understanding—automatically adapting to whether the user is **explaining** an idea, **tightening a tech spec/code review without losing facts**, **summarizing** dense material, or **organizing** scattered notes, without requiring them to specify a mode.

For deeper templates, checklists, and diagnostic rules, read [frameworks.md](./references/frameworks.md).

## Step 1: Infer Intent, Audience, and Bottleneck Automatically

From the user's request alone, silently determine what job they are asking for and apply the matching approach (combining approaches whenever helpful):

1. **Tightening dense technical writing (specs, tech specs, RFCs, PRs, code reviews)** -> apply **Part A** (*Lossless Technical Compression*).
2. **Explaining, writing, or rewriting for an audience** -> apply **Part B**:
   - Busy peers, managers, proposals, emails, postmortems -> **Top-Down Structure** (*The Pyramid Principle*)
   - Beginners, onboarding, non-technical or unfamiliar audience -> **Context & Analogies** (*The Art of Explanation*)
   - Persuading, pitching, or making an idea memorable -> **Concrete & Memorable** (*Made to Stick*)
   - Complex topic for a mixed or general audience -> **Stack all three automatically**
3. **Reading, summarizing, or organizing information** -> apply **Part C**:
   - Summarizing a book, article, paper, doc, or transcript -> **Skeleton & Layered Summary** (*How to Read a Book* + *Progressive Summarization*)
   - Cleaning up messy notes, brainstorms, links, or a knowledge base -> **Atomic Notes & PARA** (*How to Take Smart Notes* + *Building a Second Brain*)

---

## Part A: Tech Specs, PRs & Code Reviews (Lossless Compression)

### 1. Lossless Technical Rewriting (*Style* + *Paramedic Method* + *Smart Brevity*)
**Apply automatically for:** Specs, tech specs, RFCs, architecture decisions, API contracts, PR descriptions, and code review comments.
1. **Inventory every non-negotiable fact first:** Before cutting a word, identify every decision, owner/component, threshold, constraint, failure mode, and edge case. **Never drop, soften, or generalize any of them.**
2. **Name Actor + Action (*Williams' Style* + *Paramedic Method*):**
   - Convert nominalizations and passive voice (*"An invalidation of the token cache is performed upon..."*) into explicit **component/owner + active verb** (*"AuthService invalidates the token cache when..."*).
   - Strip prepositional chains, slow wind-ups (*"In order to ensure that..."*), and filler qualifiers—while keeping exact normative terms (`must`, `never`, exact limits/codes).
3. **Format for 10-second scanning (*Smart Brevity*):**
   - Lead with **Change / Decision** (1 line) and **Why / Risk** (1 line).
   - Group constraints, invariants, failure modes, and trade-offs into **bold-lead-in bullets** (e.g., `**Conflict behavior:** ...`, `**Rollback:** ...`).
   - For **code reviews**, structure comments as: **Issue / Risk -> Exact fix or question -> Brief why** (one clear point per comment).

---

## Part B: Explaining & Writing Playbook

### 2. Top-Down Structure (*The Pyramid Principle* — Barbara Minto)
**Apply automatically for:** Decision-makers, engineering proposals, emails, postmortems, status updates.
1. **Open with SCQA** briefly when context is needed (*Situation -> Complication -> Question -> Answer*); otherwise jump straight to the Answer.
2. **Lead with the governing conclusion** in the first 1–2 sentences (top-down, not bottom-up).
3. **Group supporting points using MECE** (*Mutually Exclusive, Collectively Exhaustive*): 2–5 distinct, non-overlapping buckets that cover the answer completely.
4. **Enforce vertical and horizontal logic:** Every parent claim summarizes its children; sibling points share one logical order (chronological, structural, or ranked by impact).

### 3. Context & Analogies (*The Art of Explanation* — Lee LeFever)
**Apply automatically for:** Beginners, onboarding, cross-functional/non-technical stakeholders, tutorials, demos.
1. **Answer "Why does this matter?" before "How does it work?"** Show the picture on the puzzle box before handing out puzzle pieces.
2. **Anchor on the listener's side:** Connect the new idea to something familiar via a simple analogy before introducing technical mechanics.
3. **Stay on the left side of the Explanation Scale (A to G, not A to Z):** Trade edge-case precision for intuitive understanding and translate unavoidable jargon immediately.

### 4. Concrete & Memorable (*Made to Stick* — Heath & Heath)
**Apply automatically for:** Pitches, talks, culture/process change, persuasive writing, lessons people must remember and repeat.
1. **Defeat the Curse of Knowledge:** Spell out what feels obvious to you so the listener hears the "music," not isolated taps.
2. **Find the single Simple core:** One sharp, prioritized takeaway.
3. **Make it Concrete & Unexpected:** Replace abstract buzzwords with sensory objects, real actions, or a curiosity gap.
4. **Use Stories or Human-Scale Proof:** Show someone navigating the idea in action rather than dry numbers alone.

### 5. Combined Default (for Complex or Mixed Explanations)
1. **Opening:** 1–2 sentences of shared context + a familiar analogy if needed.
2. **Skeleton:** Main takeaway upfront, backed by 2–4 clean MECE points.
3. **Proof / Examples:** Ground each abstract point with one concrete, memorable example.

---

## Part C: Summarizing & Organizing Playbook

### 6. Skeleton & Layered Summary (*How to Read a Book* + *Progressive Summarization*)
**Apply automatically when summarizing** books, long articles, technical docs, videos, or transcripts:
1. **One-Sentence Unity (*Adler*):** State what the entire piece is about and the core problem it tries to solve in 1–2 sentences.
2. **Skeleton Outline (*Adler*):** Break the source into its 3–5 major structural parts and show how they fit together to answer the core problem.
3. **Key Terms & Core Claims (*Adler*):** Define the author's pivotal terms plainly and list the main propositions/evidence supporting their conclusion.
4. **Progressive Layers (*Tiago Forte*):** Format so a reader can skim at three depths:
   - **Executive Summary:** 2–3 sentence bottom line at the very top.
   - **Bolded Core:** Highlight the single most important takeaway inside each section.
   - **Actionable Takeaways:** Concrete ideas the user can apply immediately.

### 7. Atomic Notes & PARA (*How to Take Smart Notes* + *Building a Second Brain*)
**Apply automatically when organizing** scattered notes, research dumps, bookmarks, or project ideas:
1. **Rewrite into Atomic Notes (*Zettelkasten / Smart Notes*):**
   - Split multi-topic dumps into **one self-contained idea per note/block**, expressed in plain, own words (not copy-pasted fragments).
   - Give each atomic note a clear claim-based title (e.g., *"Lead with conclusions because working memory is small"* instead of *"Writing notes"*).
2. **Link by Context, Not Just Source (*Smart Notes*):** Group and cross-link notes by the question or topic where they will be useful, noting *why* two ideas connect (supports, contrasts, or extends).
3. **Organize by Actionability with PARA (*Building a Second Brain*):** When structuring folders, tasks, or workspaces, sort items by where they will be used next:
   - **Projects:** Active goals with a deadline/outcome.
   - **Areas:** Ongoing responsibilities to maintain (no end date).
   - **Resources:** Reference topics of ongoing interest.
   - **Archives:** Inactive items from the other three.

---

## Step 2: Self-Check Before Responding

- **Zero-loss check (especially for specs & reviews):** Did every original decision, number, constraint, owner, and edge case survive unchanged?
- **Lead clarity:** Can a busy reader grasp the main point or change from the first two lines?
- **No Curse of Knowledge:** Is every unfamiliar term defined or anchored in plain language?
- **Clean structure (MECE / Atomic):** Are points non-overlapping and free of filler?
