# Explanation Frameworks Reference

Use this reference when you need deeper structure templates, examples, or diagnostic rules from the three core books.

---

## 1. *The Pyramid Principle* (Barbara Minto)

### SCQA Opening Pattern
Use SCQA to frame the introduction in 2–4 crisp sentences before presenting the pyramid:
- **Situation:** An uncontroversial, shared fact about the current state.
- **Complication:** What changed, broke, or created tension.
- **Question:** The natural question this tension raises for the reader.
- **Answer:** Your main governing recommendation or conclusion (the top of the pyramid).

*Example:*
- **S:** Our API serves 95% of mobile traffic.
- **C:** Latency spikes during peak hours are causing checkout timeouts.
- **Q:** How should we stabilize peak performance without a full rewrite?
- **A:** Cache read-heavy catalog endpoints at the edge and decouple analytics writes asynchronously.

### MECE Grouping Orders
Every group of sibling points beneath a parent claim should be:
- **Mutually Exclusive:** No two points overlap in meaning.
- **Collectively Exhaustive:** Together, they cover the whole parent claim without big gaps.

Pick one consistent horizontal order per group:
1. **Deductive:** Major premise -> Minor premise -> Conclusion (use sparingly; good for logic proofs).
2. **Chronological:** Step 1 -> Step 2 -> Step 3 (processes, timelines).
3. **Structural:** Part A / Part B / Part C (architecture, regions, teams).
4. **Ranking / Degree:** Most impactful -> Least impactful (reasons, recommendations).

### Guardrails
- Avoid "empty" umbrella headers like *"Three reasons why..."* without stating the actual takeaway in the summary sentence.
- Keep each group to **3–5 items** (never a flat dump of 12 bullets).

---

## 2. *The Art of Explanation* (Lee LeFever)

### The Explanation Scale (A to Z)
- **A** = Zero knowledge; **Z** = Deep expert mastery.
- Most explanations fail because experts try to take listeners from **A to Z** in one sitting.
- Aim for **A to G** first: enough context and big-picture shape that the listener feels confident and curious to ask about H–Z later.

### Building an Effective Analogy
1. Identify the *core relationship* in your concept (e.g., an API is an intermediary taking orders between two sides that don't speak directly).
2. Pick something universally familiar with the same relationship (a restaurant waiter taking orders between the table and the kitchen).
3. Map only the key parts—stop before the analogy breaks down on edge cases.

### Context Checklist
Before explaining *how* something works, make sure the listener knows:
- **Who/What** this affects.
- **Why** it exists (the problem it solves).
- **Where** it fits in the bigger system ("the picture on the puzzle box").

---

## 3. *Made to Stick* (Chip & Dan Heath)

### The Curse of Knowledge
Once you know something well, your brain hears the whole symphony (mental models, edge cases, history), while your listener only hears isolated taps on a table. Always ask: *"If someone knew nothing about this, what word or leap would lose them?"*

### SUCCESs Checklist
- **S — Simple:** Find the single core idea (*Commander's Intent*). Prioritizing one clear truth beats listing five mediocre ones.
- **U — Unexpected:** Break expectations, then open a *curiosity gap* (highlight what they don't know yet before filling it).
- **C — Concrete:** Use physical, sensory, observable details instead of corporate or technical abstractions.
  - *Abstract:* "Improve onboarding velocity."
  - *Concrete:* "Get a new developer from `git clone` to their first merged PR in under 30 minutes."
- **C — Credible:** Use vivid, human-scale comparisons or testable claims (*"try it right now"*).
- **E — Emotional:** Connect to real human stakes, identity, or pain—not just percentages.
- **S — Stories:** Show real cause-and-effect in action (challenge -> struggle -> resolution) so the listener mentally simulates the concept.

---

## 4. Quick Anti-Pattern Lookup

| Symptom in Draft | Root Problem | Fix |
| :--- | :--- | :--- |
| Reader asks *"So what?"* halfway through | Bottom-up buildup; buried lead | Move the conclusion to sentence 1 (**Pyramid**) |
| Reader glazes over at sentence 2 | Missing big picture / jargon overload | Add "why" context + a familiar analogy (**Bridge**) |
| Reader nods politely, forgets it next day | Too abstract; no concrete anchor | Replace abstractions with one concrete example/story (**Sticky**) |
| Bullet list feels messy or repetitive | Overlapping categories | Re-group into 3 non-overlapping MECE buckets (**Pyramid**) |
