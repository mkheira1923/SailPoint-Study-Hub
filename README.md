# SCIP Study Hub — SAVIGA-C01

Interactive study hub for the **Saviynt Certified IGA Professional** exam, built directly from
Saviynt's official Exam Preparation Guide.

**Live site:** https://mkheira1923.github.io/scip-study-hub/

## What's in it

- **The blueprint, verbatim** — all 6 sections, 28 objectives and 95 numbered sub-topics reproduced
  exactly as Saviynt publishes them, plus their three official sample questions
- **Study material for every objective** — 171 key facts with the exact UI paths, job names and
  configuration values, each with its common trap and a hands-on drill
- **210 practice questions**, every one tagged to its objective, with an explanation and a source
- **146 flashcards** across all 28 objectives
- **Per-section quizzes** that report by *objective* — a wrong answer tells you to reread 1.3
  Application Onboarding, not just "section 1"
- **Full mock exam to spec** — 70 questions drawn to the official 15/15/10/10/15/5 weighting,
  2-hour clock, question navigator with flagging, scored on the real 50–500 scale with a 350 pass mark
- **SailPoint bridge** — 28 concepts explained then mapped side by side, with the place each
  analogy breaks down
- **Corrections page** — 12 documented factual errors circulating in third-party material
- Glossary, 20 sources, light/dark, works offline, progress saved in your browser

## The blueprint

| # | Section | Questions | Weight |
|---|---|---|---|
| 01 | Building Identity Warehouse | 15 | 21.4% |
| 02 | Access Request System (ARS) | 15 | 21.4% |
| 03 | Rules and Policies *(detailed heading: Rules Engineering)* | 10 | 14.3% |
| 04 | Segregation of Duties (SoDs) | 10 | 14.3% |
| 05 | Attestation *(detailed heading: Access Reviews)* | 15 | 21.4% |
| 06 | Analytics | 5 | 7.1% |
| | **Total** | **70** | |

SAVIGA-C01 · 70 questions · 120 minutes · scaled 50–500 · pass at 350 · ProctorU · L100 training required.

## Two things worth knowing

**Segregation of Duties is a trap.** The L100 training has no SoD module and no SoD lab, yet SoD is
10 exam questions with 6 objectives and 23 sub-topics. Section 4 here is written to close that gap.

**Two facts in circulation are stale.** The exam moved from Examity to **ProctorU**, and
**Scenario-Based** questions were added as a third question type — the 2021 edition of the blueprint
lists only two.

## Sources

Anchored to the official [SCIP Exam Preparation Guide](https://saviynt.com/hubfs/Saviynt%20Certified%20IGA%20Professional%20(SCIP)%20Exam%20Preparation%20Guide%20(1).pdf?hsLang=en),
the Saviynt IGA L100 training materials, the [EIC Administration Guide](https://docs.saviyntcloud.com/),
[Saviynt's REST API reference](https://developers.saviynt.com/), and
[Saviynt's own Terraform provider](https://github.com/Saviynt/terraform-provider-saviynt).
Full list with provenance notes on the Sources page.

Where a fact could not be verified from an official source, the app says so rather than guessing.
Where Saviynt's own documents disagree, both readings are shown.

Not affiliated with or endorsed by Saviynt. Study aid only.

## Running it

One self-contained HTML file. No dependencies, no build step, no network calls.
Open `index.html` in any browser, or serve the folder with anything static.
