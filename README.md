# elucidate

Most AI answers either bury the point, drown beginners in jargon, bloat tech specs with filler, or dump walls of unorganized text. **`elucidate`** fixes that—it automatically adapts how an AI agent tightens technical specs and code reviews, explains ideas, summarizes dense material, and organizes messy notes without losing a single decision or detail.

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
| **Verbose tech spec, RFC, PR, or code review** | Long, passive prose that hides ownership and slows reviewers down | **30–50% fewer words** with active actor+action phrasing, bold-lead-in bullets, and **100% of decisions & edge cases intact** |
| **Proposal, email, or postmortem for busy readers** | Bottom-up buildup; the main point is buried at the end | **Answer first**, framed with context and grouped into clean, non-overlapping points |
| **Technical concept for beginners or clients** | Jargon overload ("Curse of Knowledge") | **Big picture ("why") first**, anchored to a familiar analogy before details |
| **Pitch, talk, or change you want people to remember** | Abstract buzzwords people forget the next day | **One sharp core takeaway** backed by concrete, real-world examples |
| **Long book, paper, doc, or transcript** | Rambling chapter-by-chapter recap | **1-sentence core thesis**, structural outline, and skimmable layered highlights |
| **Messy notes, links, or research dump** | Copy-pasted fragments nobody can reuse later | **Self-contained atomic notes** in plain words, linked by topic and sorted for action |

---

## Usage Examples

Invoke it with `$elucidate` or just ask naturally:

* **Tighten a tech spec losslessly:** `"$elucidate rewrite this tech spec for fast review without dropping any constraints, TTLs, or edge cases."`
* **Sharpen a PR or code review:** `"$elucidate rewrite these code review comments so each one is crisp, actionable, and clear."`
* **Explain to a non-expert:** `"$elucidate explain how OAuth 2.0 works to a non-technical client."`
* **Summarize dense material:** `"$elucidate summarize this design doc so I can skim the core argument in 30 seconds."`
* **Organize raw notes:** `"$elucidate turn these scattered meeting notes into clean, actionable notes."`

---

## The Frameworks Behind It

`elucidate` blends nine classic communication, concision, and knowledge-management books under the hood:

### Tech Specs, PRs & Lossless Concision
1. ***Style: Lessons in Clarity and Grace*** *(Joseph M. Williams & Joseph Bizup)* — Replace passive, noun-heavy bloat with clear actors and verbs so precision goes up while reading time drops.
2. ***Revising Prose*** *(Richard A. Lanham)* — Apply the *Paramedic Method* to cut prepositional chains and filler without losing a single fact or decision.
3. ***Smart Brevity*** *(Jim VandeHei, Mike Allen & Roy Schwartz)* — Structure updates and specs for 10-second scanning using bold lead-ins and tight hierarchy.

### Explaining & Writing
4. ***The Pyramid Principle*** *(Barbara Minto)* — Put the main conclusion first, frame context crisply (Situation -> Complication -> Question -> Answer), and group supporting points with zero overlap (MECE).
5. ***The Art of Explanation*** *(Lee LeFever)* — Give the "why" before the "how," anchor new ideas to familiar analogies, and build intuition before edge cases.
6. ***Made to Stick*** *(Chip & Dan Heath)* — Overcome the *Curse of Knowledge* by stripping ideas down to one concrete, memorable core.

### Reading, Summarizing & Organizing
7. ***How to Read a Book*** *(Mortimer J. Adler & Charles Van Doren)* — Extract a work's 1-sentence thesis, structural skeleton, and core arguments instead of summarizing passively.
8. ***How to Take Smart Notes*** *(Sönke Ahrens)* — Rewrite ideas into standalone atomic notes in your own words, titled by insight and linked by context.
9. ***Building a Second Brain*** *(Tiago Forte)* — Layer summaries for fast skimming (*Progressive Summarization*) and sort knowledge by actionability (*Projects, Areas, Resources, Archives*).

---

## Structure

```text
elucidate/
├── SKILL.md                  # Agent instructions & automatic intent routing
├── references/
│   └── frameworks.md         # Templates, checklists, and anti-pattern fixes
└── README.md
```
