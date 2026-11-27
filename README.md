# elucidate

An AI Agent Skill (`SKILL.md`) for structuring explanations, technical concepts, docs, emails, and presentations so humans understand them fast and remember them.

Synthesizes three classic communication frameworks:
1. ***The Pyramid Principle*** (Barbara Minto) — Top-down conclusion first, SCQA framing, and MECE grouping.
2. ***The Art of Explanation*** (Lee LeFever) — Context before details ("Why" before "How"), familiar analogies, and A-to-G simplicity.
3. ***Made to Stick*** (Chip & Dan Heath) — Overcoming the Curse of Knowledge with concrete examples, curiosity gaps, and SUCCESs.

---

## Modes

| Mode | Best Audience / Situation | Core Technique |
| :--- | :--- | :--- |
| **Pyramid** | Decision-makers, engineering specs, emails, reviews | SCQA intro, governing answer first, non-overlapping MECE groups |
| **Bridge** | Beginners, onboarding, non-technical stakeholders | Context + familiar analogy, A-to-G Explanation Scale, zero jargon |
| **Sticky** | Pitches, talks, culture/process changes | Beat the Curse of Knowledge, one Simple core, Concrete examples & stories |
| **Stacked** *(Default)* | Complex topics for mixed audiences | Bridge opening -> Pyramid skeleton -> Sticky concrete examples |

---

## Installation

### Via Skills CLI
```bash
npx skills add abhishek-bhatkar/elucidate
```

### Manual
Copy `SKILL.md` and `references/` into your agent's skills directory:
- **Cross-agent (`~/.agents/skills/elucidate`):** works with compatible coding agents.
- **Antigravity (`~/.gemini/config/skills/elucidate`):** global Antigravity discovery path.
- **Project-specific (`.agents/skills/elucidate`):** scoped to a single repository.

---

## Usage Examples

- *"Use `elucidate` to explain how OAuth 2.0 works to a non-technical client."*
- *"Use `elucidate` in Pyramid mode to rewrite this architecture proposal for leadership."*
- *"Use `elucidate` in Sticky mode to make this engineering pitch memorable."*
- *"Use `elucidate` to critique and rewrite my onboarding doc."*

---

## Structure

```text
elucidate/
├── SKILL.md                  # Main agent instructions & mode router
├── references/
│   └── frameworks.md         # SCQA, MECE, Explanation Scale, SUCCESs reference
└── README.md
```
