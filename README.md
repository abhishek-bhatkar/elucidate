# elucidate

Most AI answers either bury the point, drown beginners in jargon, or dump walls of unorganized text. **`elucidate`** fixes that—it automatically adapts how an AI agent explains ideas, summarizes dense material, and organizes messy notes so people grasp them fast and remember them.

You don't need to pick a mode or learn special flags. Ask naturally, and `elucidate` infers your audience and goal.

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

## What It Does Automatically

| What you give it | What goes wrong without it | What `elucidate` delivers |
| :--- | :--- | :--- |
| **Spec, email, or proposal for busy readers** | Bottom-up buildup; the main point is buried at the end | **Answer first**, framed with context and grouped into clean, non-overlapping points |
| **Technical concept for beginners or clients** | Jargon overload ("Curse of Knowledge") | **Big picture ("why") first**, anchored to a familiar analogy before details |
| **Pitch, talk, or change you want people to remember** | Abstract buzzwords people forget the next day | **One sharp core takeaway** backed by concrete, real-world examples |
| **Long book, paper, doc, or transcript** | Rambling chapter-by-chapter recap | **1-sentence core thesis**, structural outline, and skimmable layered highlights |
| **Messy notes, links, or research dump** | Copy-pasted fragments nobody can reuse later | **Self-contained atomic notes** in plain words, linked by topic and sorted for action |

---

## Usage Examples

Invoke it with `$elucidate` or just ask naturally:

* **Explain to a non-expert:** `"$elucidate explain how OAuth 2.0 works to a non-technical client."`
* **Write for decision-makers:** `"$elucidate rewrite this architecture proposal for my VP."`
* **Summarize dense material:** `"$elucidate summarize this design doc so I can skim the core argument in 30 seconds."`
* **Organize raw notes:** `"$elucidate turn these scattered meeting notes into clean, actionable notes."`
* **Make an idea stick:** `"$elucidate help me pitch our new CI workflow so the team actually adopts it."`

---

## The Frameworks Behind It

`elucidate` blends six classic communication and knowledge-management books under the hood:

### Explaining & Writing
1. ***The Pyramid Principle*** *(Barbara Minto)* — Put the main conclusion first, frame context crisply (Situation -> Complication -> Question -> Answer), and group supporting points with zero overlap (MECE).
2. ***The Art of Explanation*** *(Lee LeFever)* — Give the "why" before the "how," anchor new ideas to familiar analogies, and build intuition before edge cases.
3. ***Made to Stick*** *(Chip & Dan Heath)* — Overcome the *Curse of Knowledge* by stripping ideas down to one concrete, memorable core.

### Reading, Summarizing & Organizing
4. ***How to Read a Book*** *(Mortimer J. Adler & Charles Van Doren)* — Extract a work's 1-sentence thesis, structural skeleton, and core arguments instead of summarizing passively.
5. ***How to Take Smart Notes*** *(Sönke Ahrens)* — Rewrite ideas into standalone atomic notes in your own words, titled by insight and linked by context.
6. ***Building a Second Brain*** *(Tiago Forte)* — Layer summaries for fast skimming (*Progressive Summarization*) and sort knowledge by actionability (*Projects, Areas, Resources, Archives*).

---

## Structure

```text
elucidate/
├── SKILL.md                  # Agent instructions & automatic intent routing
├── references/
│   └── frameworks.md         # Templates, checklists, and anti-pattern fixes
└── README.md
```
