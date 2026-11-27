# Knowledge, Summarization, Concision & Explanation Frameworks Reference

Use this reference for deeper templates, checklists, and diagnostic rules across all nine source books.

---

## Part A: Tech Specs, PRs & Code Reviews (Lossless Compression)

### 1. *Style: Lessons in Clarity and Grace* (Joseph M. Williams & Joseph Bizup)

#### Core Diagnostic: Characters & Actions
Dense technical writing becomes slow when real actions are turned into abstract nouns (**nominalizations**) and the actual component/person doing the work disappears:
- *Bloated:* "A determination of retry eligibility is made by the worker upon receipt of a 5xx response."
- *Clear:* "The worker retries whenever it receives a `5xx` response."

Rules for sentence-level clarity without losing precision:
1. **Put the doer in the subject** (e.g., `AuthService`, `the client`, `migration 004`).
2. **Put the real action in the verb** (avoid `perform`, `conduct`, `facilitate`, `utilize`).
3. **Flow old -> new:** Start each sentence with familiar context from the previous sentence, and place the new technical detail at the end.

---

### 2. *Revising Prose* — The Paramedic Method (Richard A. Lanham)

Run this 5-step surgical pass on any bloated spec paragraph or review comment (typically cuts 30–50% of words with zero lost meaning):
1. **Spot prepositions** (`of`, `in`, `by`, `for`, `with`, `to`) — chains of prepositions signal buried structure.
2. **Spot weak `to be` verbs** (`is`, `was`, `are`, `will be`) paired with passive participles.
3. **Find the real action** and promote it into a strong active verb.
4. **Put the actor first** ("Who does this?").
5. **Cut the slow wind-up** (`In order to...`, `It is important to note that...`, `The fact that...`).

---

### 3. *Smart Brevity* (Jim VandeHei, Mike Allen & Roy Schwartz)

#### Spec / RFC / PR Structure (Fast Scan, Zero Dropped Edge Cases)
```markdown
**Change / Decision:** <1 crisp sentence stating what changes or is decided>
**Why / Risk:** <1 sentence on the problem prevented or value gained>

* **Rule / Flow:** <exact actor + action + condition>
* **Constraints / Limits:** <exact numbers, TTLs, quotas, permissions>
* **Failure / Edge cases:** <exact fallback, status code, or rollback>
```

#### Code Review Comment Structure
Keep every review comment fast to parse and unambiguous:
- **Blocking vs. non-blocking:** Prefix optional thoughts with `nit:` or `optional:` so authors know immediately what blocks merge.
- **Format:** `**<Issue or risk>** — <exact behavior/bug>. **Fix:** <concrete suggestion>.`

---

## Part B: Explaining & Writing

### 4. *The Pyramid Principle* (Barbara Minto)

#### SCQA Opening Pattern
Frame introductions in 2–4 crisp sentences before presenting the pyramid:
- **Situation:** An uncontroversial, shared fact about the current state.
- **Complication:** What changed, broke, or created tension.
- **Question:** The natural question this tension raises for the reader.
- **Answer:** Your governing recommendation or conclusion (the top of the pyramid).

#### MECE Grouping Orders
Every group of sibling points beneath a parent claim should be **Mutually Exclusive** (no overlap) and **Collectively Exhaustive** (no major gaps). Pick one consistent horizontal order per group:
1. **Deductive:** Major premise -> Minor premise -> Conclusion.
2. **Chronological:** Step 1 -> Step 2 -> Step 3.
3. **Structural:** Part A / Part B / Part C.
4. **Ranking / Degree:** Most impactful -> Least impactful.

Guardrails: Keep each group to **3–5 items** and avoid empty headers like *"Three reasons why..."* without stating the actual takeaway.

---

### 5. *The Art of Explanation* (Lee LeFever)

#### The Explanation Scale (A to Z)
- **A** = Zero knowledge; **Z** = Deep expert mastery.
- Aim for **A to G** first: enough context ("the picture on the puzzle box") and big-picture shape so the listener understands *why it matters* before learning edge cases (H–Z).

#### Building an Effective Analogy
1. Identify the *core relationship* (e.g., an API passes requests between two sides that don't talk directly).
2. Pick a universally familiar match (a waiter passing orders between the table and the kitchen).
3. Map only the key parts—stop before edge cases break the analogy.

---

### 6. *Made to Stick* (Chip & Dan Heath)

#### The Curse of Knowledge
Once you know something well, your brain hears the whole symphony, while your listener only hears isolated taps on a table. Always check: *"If someone knew nothing about this, what word or leap would lose them?"*

#### SUCCESs Checklist
- **S — Simple:** One sharp core truth (*Commander's Intent*), not five diluted bullets.
- **U — Unexpected:** Break expectations and open a *curiosity gap* before answering it.
- **C — Concrete:** Sensory, observable specifics instead of vague abstractions (*"clone to first merged PR in 30 minutes"* instead of *"improve onboarding velocity"*).
- **C — Credible:** Human-scale numbers or testable claims.
- **E — Emotional:** Connect to real human stakes or pain.
- **S — Stories:** Cause-and-effect in action so the listener mentally simulates the concept.

---

## Part C: Reading, Summarizing & Organizing

### 7. *How to Read a Book* (Mortimer J. Adler & Charles Van Doren)

#### Analytical Skeletonizing (4 Rules for Summarizing Any Source)
1. **Classify:** State what kind of work it is (theoretical vs. practical, guide, architecture proposal, research paper).
2. **State the Unity:** Express the whole work's core thesis or problem in a single short paragraph (or 1–2 sentences).
3. **Outline the Parts:** List the major structural divisions and show how each part advances the whole.
4. **Define Problems & Propositions:** Identify the specific questions the author set out to answer, their key terms, and which questions were actually answered.

---

### 8. *How to Take Smart Notes* (Sönke Ahrens)

#### Zettelkasten Principles for Organizing Thoughts
1. **Write in your own words:** Copying quotes creates an illusion of understanding; rewriting forces comprehension.
2. **Keep notes atomic:** One idea per note, self-contained enough to make sense months later without re-reading the original source.
3. **Title by insight, not topic:**
   - *Weak:* `Caching notes`
   - *Strong:* `Edge caching cuts tail latency only when cache keys exclude per-user headers`
4. **File by future context, not source:** Ask *"In which project or topic will I want to stumble across this?"* and link directly to related notes (`supports`, `contradicts`, `example of`).

---

### 9. *Building a Second Brain* (Tiago Forte)

#### Progressive Summarization (Layered Skimmability)
Make summaries useful for both a 10-second scan and a 5-minute read:
- **Layer 1 (Captured):** Key raw passages or facts.
- **Layer 2 (Bolded):** Bold the essential phrases within those passages.
- **Layer 3 (Highlighted):** Call out the single sharpest line per section.
- **Layer 4 (Executive Summary):** A short top-level summary in your own words at the top.

#### PARA Organization System
Organize notes, folders, and knowledge bases by **actionability**:
- **P — Projects:** Active efforts with a clear outcome and deadline.
- **A — Areas:** Ongoing responsibilities with standards to maintain.
- **R — Resources:** Reference topics collected for future use.
- **A — Archives:** Completed or inactive items from P, A, or R.

---

## Quick Anti-Pattern Lookup

| Symptom | Root Problem | Fix |
| :--- | :--- | :--- |
| Spec/PR feels long & tiring, hard to spot rules | Nominalizations, passive voice, prose walls | Actor+action + Smart Brevity bullets (*Style + Paramedic + Smart Brevity*) |
| Code review comment starts an argument or confusion | Vague critique or buried ask | State risk -> exact change -> optional `nit:` (*Smart Brevity*) |
| Reader asks *"So what?"* halfway through | Buried lead / bottom-up buildup | Move conclusion to sentence 1 (*The Pyramid Principle*) |
| Reader glazes over at sentence 2 | Missing big picture / jargon overload | Add "why" context + analogy (*The Art of Explanation*) |
| Reader forgets it the next day | Too abstract | Add one concrete example or story (*Made to Stick*) |
| Summary feels like a list of random quotes | No structural skeleton | State 1-sentence unity + major parts (*How to Read a Book*) |
| Notes are impossible to find or reuse | Filed by source instead of use | Rewrite as atomic notes + sort with PARA (*Smart Notes + PARA*) |
