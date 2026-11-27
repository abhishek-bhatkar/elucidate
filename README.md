# elucidate

An AI Agent Skill (`SKILL.md`) for **summarizing dense material, organizing scattered knowledge, and structuring explanations** so humans grasp them fast and remember them.

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

Synthesizes six classic frameworks across two workflows:

**Explaining & Writing**
1. ***The Pyramid Principle*** (Barbara Minto) — Top-down conclusion first, SCQA framing, and MECE grouping.
2. ***The Art of Explanation*** (Lee LeFever) — Context before details ("Why" before "How"), familiar analogies, and A-to-G simplicity.
3. ***Made to Stick*** (Chip & Dan Heath) — Overcoming the Curse of Knowledge with concrete examples, curiosity gaps, and SUCCESs.

**Reading, Summarizing & Organizing**
4. ***How to Read a Book*** (Mortimer J. Adler & Charles Van Doren) — Structural outlining, 1-sentence unity, and extracting core arguments.
5. ***How to Take Smart Notes*** (Sönke Ahrens) — Atomic notes in your own words, insight-driven titles, and context-based linking.
6. ***Building a Second Brain*** (Tiago Forte) — Progressive Summarization layers and action-oriented PARA organization.

---

## Modes

| Mode | Best Audience / Situation | Core Technique |
| :--- | :--- | :--- |
| **Pyramid** | Decision-makers, engineering specs, emails, reviews | SCQA intro, governing answer first, non-overlapping MECE groups |
| **Bridge** | Beginners, onboarding, non-technical stakeholders | Context + familiar analogy, A-to-G Explanation Scale, zero jargon |
| **Sticky** | Pitches, talks, culture/process changes | Beat the Curse of Knowledge, one Simple core, Concrete examples & stories |
| **Stacked** *(Default)* | Complex topics for mixed audiences | Bridge opening -> Pyramid skeleton -> Sticky concrete examples |
| **Digest** | Books, long articles, papers, docs, transcripts | 1-sentence unity + structural skeleton + progressive summary layers |
| **Organize** | Messy notes, brainstorms, research dumps, knowledge bases | Atomic own-words notes, cross-links, and PARA categorization |

---

## Usage Examples

- *"Use `elucidate` to explain how OAuth 2.0 works to a non-technical client."*
- *"Use `elucidate` in Pyramid mode to rewrite this architecture proposal for leadership."*
- *"Use `elucidate` in Digest mode to summarize this design doc / article."*
- *"Use `elucidate` in Organize mode to turn these raw meeting notes into atomic notes sorted by PARA."*
- *"Use `elucidate` in Sticky mode to make this engineering pitch memorable."*

---

## Structure

```text
elucidate/
├── SKILL.md                  # Main agent instructions & mode router
├── references/
│   └── frameworks.md         # SCQA, MECE, SUCCESs, Adler, Smart Notes, PARA reference
└── README.md
```
