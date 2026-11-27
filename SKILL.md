---
name: elucidate
description: >-
  Structures explanations, technical concepts, docs, emails, and presentations for maximum clarity
  using The Pyramid Principle, The Art of Explanation, and Made to Stick. Use when the user asks
  to explain a concept to someone, simplify complex ideas, structure a doc/proposal/update,
  overcome jargon, or rewrite an explanation to be clearer, more logical, or more memorable.
---

# Elucidate

Turn complex, scattered ideas into clear, audience-tailored explanations by choosing or stacking three proven frameworks: **The Pyramid Principle** (structure), **The Art of Explanation** (accessibility), and **Made to Stick** (memorability).

For deeper templates, examples, and checklists, read [frameworks.md](./references/frameworks.md).

## Step 1: Identify Audience, Context, and Goal

Before writing or rewriting, determine (from the prompt, or infer reasonably):
1. **Who is listening?** (Busy decision-maker, peer engineer, beginner/non-expert, skeptical room, or mixed audience)
2. **What is the bottleneck?**
   - Too disorganized / buried lead -> **Pyramid**
   - Missing context / too much jargon -> **Bridge** (*Art of Explanation*)
   - Forgettable / abstract / low urgency -> **Sticky** (*Made to Stick*)
   - Complex topic for a mixed or unfamiliar group -> **Stacked** (default)
3. **Explicit user override:** If the user names a mode (`pyramid`, `bridge`/`analogy`, `sticky`, or `stacked`), follow that directly.

## Step 2: Apply the Selected Mode

### Mode A: Pyramid (*The Pyramid Principle* — Barbara Minto)
**Best for:** Decision-makers, engineering specs, RFCs, emails, postmortems, status updates, proposals.
1. **Open with SCQA** (briefly when context is needed): *Situation -> Complication -> Question -> Answer*. If context is already shared, jump straight to the Answer.
2. **Lead with the governing conclusion** in the first 1–2 sentences. Never build bottom-up to a surprise ending unless the audience is actively hostile to the premise.
3. **Group supporting points using MECE** (*Mutually Exclusive, Collectively Exhaustive*): 2–5 distinct, non-overlapping buckets that cover the answer completely.
4. **Enforce vertical and horizontal logic:** Every parent claim summarizes its children; sibling points share one logical order (chronological, structural/component, or ranked by impact).

### Mode B: Bridge (*The Art of Explanation* — Lee LeFever)
**Best for:** Beginners, onboarding, cross-functional/non-technical stakeholders, tutorials, demos.
1. **Answer "Why does this matter?" before "How does it work?"** Give the picture on the puzzle box before handing over puzzle pieces.
2. **Anchor on the listener's side:** Connect the unfamiliar idea to something they already know via a simple analogy before introducing technical mechanics.
3. **Stay on the left side of the Explanation Scale (A to G, not A to Z):** Trade edge-case precision for intuitive understanding. Strip jargon or translate it immediately into plain language.

### Mode C: Sticky (*Made to Stick* — Heath & Heath)
**Best for:** Pitches, talks, culture/process change, persuasive writing, lessons people must remember and repeat.
1. **Defeat the Curse of Knowledge:** Assume the listener cannot "hear the song in your head"—spell out what is obvious to you.
2. **Find the single Simple core:** One sharp, prioritized takeaway (not ten diluted bullets).
3. **Make it Concrete & Unexpected:** Replace abstract nouns (*scalability, synergy, optimization*) with sensory objects, real actions, or a surprising gap that creates curiosity.
4. **Use Stories or Human-Scale Proof:** Show someone navigating the problem/solution rather than relying on dry statistics alone.

### Mode D: Stacked (Default for Complex or Mixed Explanations)
Combine all three cleanly in layers:
1. **Opening (Bridge):** 1–2 sentences of shared context + a familiar analogy if the topic is unfamiliar.
2. **Skeleton (Pyramid):** State the single main takeaway upfront, supported by 2–4 clean MECE points.
3. **Proof / Examples (Sticky):** Ground each abstract point with one concrete, memorable example.

## Step 3: Self-Check Before Responding

Verify the draft passes these checks:
- **Lead clarity:** Can a busy reader state the main point after reading only the first two sentences?
- **No Curse of Knowledge:** Is every unavoidable technical term explained or anchored in familiar terms?
- **No overlap/bloat:** Are supporting bullets distinct (MECE) and free of filler?
- **Right tone for the situation:** No forced stories in a quick operational spec; no cold jargon dump for a beginner.

If the user asked to **rewrite or critique** their own draft, output:
1. Brief diagnosis of the main bottleneck (missing context, buried lead, jargon, or abstraction).
2. The rewritten version using the best-fit mode.
