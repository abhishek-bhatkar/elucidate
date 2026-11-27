# elucidate

AI responses often bury the lead, bloat specs with passive filler, drown beginners in jargon, or dump unorganized walls of text. **`elucidate`** fixes all four automatically—inferring your audience and goal from a natural prompt, with zero modes or flags required.

## Installation

### Via Skills CLI
```bash
npx skills add abhishek-bhatkar/elucidate
```

### Ask Your AI Agent
Paste this prompt into your AI coding assistant:
```text
Install the elucidate skill from https://github.com/abhishek-bhatkar/elucidate
```

---

## What It Handles Automatically

| Input | Without `elucidate` | With `elucidate` |
| :--- | :--- | :--- |
| **Tech spec, RFC, PR, or code review** | Passive, wordy prose that hides ownership and slows reviews | **30–50% fewer words** via Actor+Action phrasing and bold-lead-in bullets—**100% of decisions, thresholds, and edge cases preserved** |
| **Explanation, proposal, or pitch** | Buried conclusion, jargon overload, or forgettable buzzwords | **Answer first**, framed with context/analogies for non-experts and concrete examples that stick |
| **Book, paper, doc, or transcript** | Rambling chapter-by-chapter recap | **2–3 line bottom line**, 3–5 part structural skeleton, bolded insights, and action items |
| **Messy notes or research dump** | Unsearchable copy-pasted fragments | **Claim-titled atomic notes** in plain words, cross-linked and sorted by actionability (**PARA**) |

---

## Examples

Invoke with `$elucidate` or ask naturally:

* **Tighten a tech spec:** `"$elucidate rewrite this tech spec for fast review without dropping any constraints, TTLs, or edge cases."`
* **Sharpen code reviews:** `"$elucidate rewrite these code review comments so each one is crisp and actionable."`
* **Explain to a non-expert:** `"$elucidate explain how OAuth 2.0 works to a non-technical client."`
* **Summarize dense docs:** `"$elucidate summarize this design doc so I can skim the core argument in 30 seconds."`
* **Organize raw notes:** `"$elucidate turn these scattered meeting notes into clean, actionable notes."`

---

## Frameworks Behind It

### Tech Specs, PRs & Lossless Concision
1. ***Style: Lessons in Clarity and Grace*** *(Joseph M. Williams & Joseph Bizup)* — Actor+Action phrasing to eliminate passive, noun-heavy bloat.
2. ***Revising Prose*** *(Richard A. Lanham)* — *Paramedic Method* to strip filler without dropping facts.
3. ***Smart Brevity*** *(Jim VandeHei, Mike Allen & Roy Schwartz)* — Bold lead-ins and tight hierarchy for 10-second scanning.

### Explaining & Writing
4. ***The Pyramid Principle*** *(Barbara Minto)* — Conclusion first, SCQA framing, and non-overlapping MECE groups.
5. ***The Art of Explanation*** *(Lee LeFever)* — Context ("why") before mechanics, familiar analogies, A-to-G simplicity.
6. ***Made to Stick*** *(Chip & Dan Heath)* — Beat the *Curse of Knowledge* with one concrete, memorable core.

### Reading, Summarizing & Organizing
7. ***How to Read a Book*** *(Mortimer J. Adler & Charles Van Doren)* — Extract thesis unity, structural skeleton, and core claims.
8. ***How to Take Smart Notes*** *(Sönke Ahrens)* — Claim-titled atomic notes in your own words, linked by context.
9. ***Building a Second Brain*** *(Tiago Forte)* — Layered *Progressive Summarization* and *PARA* (*Projects, Areas, Resources, Archives*).

---

## Structure

```text
elucidate/
├── SKILL.md                  # XML-structured routing, invariants, and execution rules
├── references/
│   └── frameworks.md         # On-demand templates and diagnostics
└── README.md
```
