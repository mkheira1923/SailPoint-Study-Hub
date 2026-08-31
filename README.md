# SailPoint Engineer Study Hub

Interactive study hub for **both** SailPoint engineer certifications, in one self-contained page.

- **SailPoint Certified IdentityIQ Engineer**
- **SailPoint Certified Identity Security Engineer** — the exam formerly called *IdentityNow Engineer*

**Live site:** https://mkheira1923.github.io/SailPoint-Study-Hub/

## What's in it

- **482 practice questions** — 235 IdentityIQ, 247 ISC — every one with an explanation and a source
- **297 flashcards** across all seventeen domains
- **195 field review items** — topics recalled straight after sitting both exams, reconstructed as questions with the answer worked out and tagged by confidence (138 ISC, 57 IdentityIQ)
- **DOMC drill** — the real exam format. One option at a time, in random order, yes or no, no going back
- **Timed mock exams** — 60 questions in 90 minutes per exam, drawn in proportion to each blueprint's objective weighting
- **Study pages per domain** — key facts, the traps that cost marks, and the exact UI paths, object names, log files and commands
- **Global search** — press `/` anywhere to search all 1685 indexed items: questions, flashcards, review items, study notes, glossary, bridge and reference tables
- **Targeted practice** — retry what you missed, work through what you starred, or drill only what you have not seen
- **IdentityIQ ↔ ISC bridge** — 33 concept mappings for anyone crossing between the two products
- **14 reference tables** — every transform operation, every rule type and where it runs, ISC numbers and limits, VA toolbox commands and expected connectivity responses, ISC search syntax, IdentityIQ predefined tasks and rule signatures, scoping in depth, and the certification content rules
- 82-term glossary, full source list, keyboard shortcuts, printable study pages, light/dark, works offline, progress saved in your browser and exportable

## The blueprints

### SailPoint Certified IdentityIQ Engineer

Seven subject areas, 50 objectives. 90 minutes, DOMC format. The seven areas correspond to the score report you receive immediately after the exam.

| # | Subject area | Objectives |
|---|---|---|
| 1 | IdentityIQ Installation, Build and Deployment | 7 |
| 2 | IdentityIQ Lifecycle Manager | 7 |
| 3 | IdentityIQ Identity Governance | 7 |
| 4 | IdentityIQ Development | 10 |
| 5 | IdentityIQ Application Onboarding | 6 |
| 6 | IdentityIQ Debugging and Troubleshooting | 6 |
| 7 | IdentityIQ Data and Access Modeling | 7 |
| | **Total** | **50** |

### SailPoint Certified Identity Security Engineer

Ten domains, 70 objectives. 90 minutes, DOMC format. USD 400, two attempts included, 364 days to schedule, minimum one year of hands-on experience expected.

| # | Domain | Objectives |
|---|---|---|
| 1 | Identity and Lifecycle Management | 8 |
| 2 | Provisioning | 9 |
| 3 | Access Management | 3 |
| 4 | Virtual Appliances (VA) | 12 |
| 5 | Sources | 7 |
| 6 | General Knowledge for Identity Security Engineer | 7 |
| 7 | Platforms | 10 |
| 8 | Supporting Governance | 5 |
| 9 | Architecture | 5 |
| 10 | Rules and Transforms | 4 |
| | **Total** | **70** |

Both blueprints are reproduced verbatim on the Blueprint page and every question is tagged to its objective.

## A note on the format

Both exams use **Discrete Option Multiple Choice**. You are not shown four options and asked which is right. You are shown options **one at a time, in random order**, and asked **yes** or **no** to each. There is no back, no skip, no review, and no changing an answer.

That changes how you should study, so the hub includes a dedicated DOMC drill mode alongside the conventional multiple-choice practice. The single most useful habit it trains: **judge the statement in front of you**. An option that is true but incomplete is still true — reject only what is actually wrong.

## Sources

Built from SailPoint's published exam study guides, the public product documentation at `documentation.sailpoint.com`, the developer documentation at `developer.sailpoint.com`, the Compass technical whitepapers, the IdentityIQ 8.5 release notes, and SailPoint's own course material. Every source is listed in the app with a note on what it contributed.

The **Field Review** section is different in kind: it reconstructs topics recalled immediately after sitting both exams. Every item carries a confidence tag —

- **SailPoint** — answered directly by SailPoint
- **Documented** — verified against product documentation
- **Field** — recalled and reasoned
- **Open** — still uncertain, worth confirming before you rely on it

Nothing in this repository reproduces live exam items. Practice questions are written from the documented behaviour of the products against the published objectives.

Not affiliated with or endorsed by SailPoint. Study aid only.

## Running it

One self-contained HTML file. No dependencies, no build step, no network calls. Open `index.html` in any browser, or serve the folder with anything static.

```
python3 -m http.server 8000
```

Progress — answered questions, known flashcards, starred items, study streak and best mock score — is stored in your own browser and never leaves it. Use the buttons on the Glossary page to copy it to another machine or keep a backup.

## Keyboard shortcuts

| Key | Action |
|---|---|
| `/` | Search everything |
| `1`–`9` | Jump to a page |
| `X` | Switch exam |
| `T` | Toggle theme |
| `E` | Expand or collapse every accordion on the page |
| `Space` | Flip the current flashcard |
| `←` `→` | Previous / next flashcard |
| `Y` / `N` | Answer in the DOMC drill |
| `Esc` | Close search |
