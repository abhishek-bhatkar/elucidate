# Elucidate Reference Templates & Diagnostics

Load this file only when rewriting large multi-section specs, summarizing long documents, or structuring big note dumps.

<templates>

## 1. Tech Spec / RFC / PR Template
```markdown
**Change / Decision:** <1 sentence: actor + action + scope>
**Why / Risk:** <1 sentence: problem prevented or outcome gained>

* **Rule / Flow:** <exact component + behavior + trigger>
* **Constraints / Limits:** <exact numbers, TTLs, quotas, permissions>
* **Failure / Edge cases:** <exact fallback, error code, retry, or rollback>
* **Trade-offs / Open questions:** <explicitly preserved caveats>
```

### Paramedic Compression Pass (Sentence Level)
Apply in order to shrink wordy sentences by 30–50% without dropping facts:
1. Cut slow wind-ups (`In order to ensure...`, `It should be noted that...`).
2. Replace `is/was + nominalization` (`performed a validation of`) with a direct verb (`validates`).
3. Move the actual component/owner into the subject slot.
4. Chain sentences `old context -> new detail` so each sentence flows immediately into the next.

## 2. Code Review Comment Template
- **Blocking:** `**<Risk / Bug>** — <what fails and when>. **Fix:** <exact change>.`
- **Non-blocking:** `nit: **<Topic>** — <concise suggestion + 1-line why>.`

## 3. SCQA & MECE Reference
- **SCQA:** *Situation* (shared baseline) -> *Complication* (what changed/broke) -> *Question* (what must be decided) -> *Answer* (governing recommendation).
- **MECE horizontal orders:** Pick one per group—*Chronological* (steps), *Structural* (components), *Ranking* (impact), or *Deductive* (premise -> conclusion). Cap each group at 3–5 bullets.

## 4. Document Digest Template
```markdown
**Bottom Line:** <1-sentence unity: core problem + thesis>

### Structural Skeleton
1. **<Part 1>** — <how it advances the thesis>
2. **<Part 2>** — <how it advances the thesis>

### Key Terms & Core Claims
* **<Term>:** <plain definition>
* **<Claim>:** **<core insight bolded>** — <supporting evidence>

### Actionable Takeaways
* <concrete action>
```

## 5. Atomic Notes & PARA Template
```markdown
### <Claim-based title stating the insight>
<2–4 lines in plain own words; self-contained without the source.>
* **Links:** `supports` [[Related Note]] | `contrasts` [[Other Note]]
* **PARA Bucket:** `Project` / `Area` / `Resource` / `Archive` — <target>
```

</templates>

<diagnostics>
| Symptom | Root Cause | Action |
| :--- | :--- | :--- |
| Spec/PR hides ownership & rules in dense prose | Nominalizations + passive voice | Run Paramedic pass; emit Actor + Action + bold-lead-in bullets |
| Review comment triggers debate or confusion | Buried ask or unclear severity | Split one issue per comment; add `nit:` when non-blocking |
| Reader asks *"So what?"* mid-way | Bottom-up buildup | Move conclusion to line 1; cap groups at 3–5 MECE bullets |
| Non-expert lost at sentence 2 | Curse of Knowledge / missing context | Open with "why" + 1 familiar analogy; cap depth at A-to-G |
| Pitch/doc feels forgettable | Abstract nouns | Replace buzzwords with sensory, human-scale examples |
| Summary reads like random quotes | Missing structural unity | Lead with 1-sentence thesis + 3–5 part skeleton |
| Notes unsearchable/unusable later | Filed by source instead of insight | Split into claim-titled atomic notes; sort into PARA |
</diagnostics>
