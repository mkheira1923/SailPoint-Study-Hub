# Changelog

## v2 — enhancement pass

Everything from v1 is still here and nothing was removed. This pass verified the exam-recall
section against its source documents, deepened every study page, roughly halved the gap between
what the blueprints cover and what the hub covers, and added navigation that makes 1,600+ items
findable.

### At a glance

| | v1 | v2 | change |
|---|---:|---:|---:|
| Practice questions | 322 | **482** | +160 |
| — IdentityIQ | 164 | 235 | +71 |
| — Identity Security Cloud | 158 | 247 | +89 |
| Flashcards | 191 | **297** | +106 |
| Field review items | 183 | **195** | +12 |
| Reference tables | 7 | **14** | +7 |
| Glossary terms | 61 | **82** | +21 |
| Sources cited | 21 | **43** | +22 |
| Study-page key facts | 226 | **294** | +68 |
| Searchable items | — | **1,685** | new |

---

### 1. Field Review verified against its source documents

This was the priority. The section is meant to reproduce what was actually in the exam-recall
notes, so it was audited mechanically rather than by sampling.

- Every bullet in `IdentityNowExamQuestions.docx` was extracted and scored against the shipped
  content: **174 of 175 covered** (the one exception is a Quizlet URL, not a fact).
- The same audit was run against the IdentityIQ recall sections: **complete**, no gaps.
- **Twelve items added** that v1 had missed or under-covered:
  - What "asynchronous" means in a password sync group *(tagged Open — the source note says it was never settled)*
  - The pass-through-is-the-authoritative-source screenshot question *(Open)*
  - Ordering the access request flow
  - The oddly-worded access profile definition *(Open)*
  - Where the password policy is displayed, upstream vs downstream *(SailPoint-confirmed)*
  - The Create Unique Account ID generator and its pattern variables
  - Standard service 443 inbound/outbound on the network diagram
  - ISC tenant updates released up to 60 times a week
  - A full vanity-URL drill using the exact examples from the notes
  - **New "Exam Strategy" group**, capturing three things the notes recorded but v1 did not surface:
    what it means when a NO gets no follow-up option; the preparation advice from the top of the
    file (get tenant access, do *all* the Quick Learns); and how to attack DOMC ordering questions
- Nothing that was already there was reworded or "improved" — the wording stays faithful to the source.

### 2. Corrections

Four facts in v1 were out of date or incomplete against current documentation:

| Was | Now | Source |
|---|---|---|
| IdentityIQ lifecycle events have 4 trigger types | **7** — Create, Manager Transfer, Attribute Change, Rule, **Native Change**, **Alert**, **Rapid Setup** | documentation.sailpoint.com |
| Role change propagation runs at 8:00 PM | **6:00 PM** tenant time (the 8:00 PM figure is older course material — both are noted) | documentation.sailpoint.com |
| Deep packet inspection is unsupported on the VA | VAs **can** be configured to trust a private root CA for TLS inspection | documentation.sailpoint.com |
| Entitlement role type described generically | It exists for **backward compatibility with 5.x and earlier** and is not recommended for new installations | documentation.sailpoint.com |

### 3. Research

- **20+ additional sources** consulted this pass, on top of v1's 15+. All 43 are listed in the app
  with a line on what each contributed.
- Nine remaining project documents were mined in full, including the consolidated ISC study guide,
  the IdentityNow Professional guide, the Binod engineer notes, the Essentials series, the Rules
  course notes, the Knowledge Check question bank, Scoping in IdentityIQ, the IQService install
  guide and the Phase 1 ISC release document.
- Nothing was added unless it was confirmed against documentation or SailPoint's own material.

### 4. Content depth

**New territory that v1 did not cover at all:**

- ISC numeric limits — segment caps, attribute sync retries, delete threshold range, event trigger
  subscriber limits, search retention and indexing lag, notification thresholds
- VA toolbox (`tb`) commands, expected connectivity responses per endpoint, certificate handling,
  the four VA statuses, `keyPassphrase` constraints, the shared-passphrase recommendation
- ISC search syntax in full — nested arrays, the `@access(A) AND @access(B)` vs `@access(A AND B)`
  distinction, range and timestamp syntax, where wildcards fail
- Event triggers, Configuration Hub, the Fairness Algorithm, Zero Knowledge Encryption, feature flags
- IdentityIQ API depth — exact method signatures, the 8.0 Hibernate change, locking, metering,
  `retryableErrors`, `universalManager`, the two status enumerations
- IdentityIQ scoping in depth — the full precedence order, rule signatures, and the real limits of
  what scope restricts
- Certification lifecycle detail on both platforms — campaign reports, due-date behaviour,
  self-certification handling, force-completion semantics

**Quality fixes:** 13 questions where every option was correct got a real distractor; one short
explanation was expanded; zero duplicate questions, flashcards or review items across the whole bank.

### 5. Usability — layout unchanged

Everything below is additive. No page moved, no page was removed, the visual design is the same.

- **Global search** (`/` or the icon in the top bar) across all 1,685 items, ranked, with highlighted
  matches, arrow-key navigation, and jump-to-item that switches exam automatically when needed
- **Targeted practice** on the Practice page: *Retry what you missed*, *Your starred questions*,
  *Questions you have not tried*
- **Weak-area callout** on the dashboard — the domains below 70%, worst first, each a one-click drill
- **Starring** on practice questions, flashcards and review items, with a starred filter on each
- **Flashcard confidence** — "Didn't know" / "Got it" advances the card and updates the known state
- **Study streak and session stats** on the dashboard
- **Keyboard shortcuts** — `/` search, `1`–`9` pages, `X` switch exam, `T` theme, `E` expand all,
  `Space` flip card, `←` `→` card navigation, `Y`/`N` in the DOMC drill, `Esc` close
- **Expand all** and **Print this domain** on study pages, with a print stylesheet that opens every
  accordion so a domain prints as a clean cheat sheet
- **Progress export / import / reset** on the Glossary page, so progress can move between machines

### 6. Verification

Headless browser run over both exams and all eleven pages: no JavaScript errors, no console errors,
no horizontal scroll at 390px, both mocks draw exactly 60, search returns and navigates correctly,
stars persist, targeted tiles appear, flashcard confidence and starred filters work, light and dark
both clean. Content linting found no doubled words, no product-name inconsistencies, no unbalanced
brackets, no broken HTML entities and no spelling errors outside technical vocabulary.

---

## v1 — initial build

Two exams in one self-contained page with an exam switcher: 322 questions, 191 flashcards,
183 field review items, 17 study pages, 33 bridge mappings, 7 reference tables, 61 glossary terms,
a DOMC drill, timed mock exams, and light/dark theming. Built from both official blueprints,
15+ online sources and the project's study material.

### Reverting

`index.html` is a single self-contained file with no dependencies. To go back to v1, restore the
previous `index.html` from git history — nothing else in the repository is required.
