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

## How It Adapts Automatically

Just ask naturally—`elucidate` detects your goal and audience automatically:

| What You're Doing | What `elucidate` Applies Automatically |
| :--- | :--- |
| **Writing to decision-makers** (specs, emails, proposals) | SCQA intro, governing answer first, non-overlapping MECE groups |
| **Explaining to beginners or non-experts** | Context ("why") before details, familiar analogy, zero jargon |
| **Pitching or teaching something memorable** | Beat the Curse of Knowledge, one sharp core, concrete examples & stories |
| **Explaining complex topics to mixed audiences** | Context opening -> top-down Pyramid structure -> concrete examples |
| **Summarizing a book, paper, or long doc** | 1-sentence unity, structural skeleton, and layered progressive summary |
| **Organizing messy notes or research dumps** | Atomic own-words notes, context cross-links, and PARA categorization |

---

## Usage Examples

- *"Use `elucidate` to explain how OAuth 2.0 works to a non-technical client."*
- *"Use `elucidate` to rewrite this architecture proposal for leadership."*
- *"Use `elucidate` to summarize this design doc / article."*
- *"Use `elucidate` to organize these raw meeting notes."*
- *"Use `elucidate` to make this engineering pitch memorable."*

---

## Structure

```text
elucidate/
├── SKILL.md                  # Main agent instructions & automatic routing
├── references/
│   └── frameworks.md         # SCQA, MECE, SUCCESs, Adler, Smart Notes, PARA reference
└── README.md
```
