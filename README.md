# Idaho Courtwatch

**Idaho Fidelity Foundation**

A statewide rating system for Idaho judges, built from **public court records**, so voters can see where each judge is consistently strong and where the record is weak — by issue area, not by party label or news cycle.

The live collector (`courtwatch-scraper`) is **private** while records are being gathered and validated. This repo is the public project summary.

## Objective

Idaho voters get a name on the ballot and almost no structured information about how that judge has actually ruled. Courtwatch’s job is to close that gap:

1. Pull public case records for Idaho courts.
2. Structure them into a judge-level dataset (case type, outcomes, sentencing patterns, reversal/appeal signals, caseload).
3. Score each judge **per category** — for example criminal sentencing, civil procedure, family, juvenile — so a voter can see “strong here, weak there” instead of a single smear or a single endorsement.
4. Hold scores behind validation until the numbers reconcile. Nothing public until the data is auditable.

This is a **fact-first civic tool**, not an advocacy score. Categories and methods will be published with the first public release so anyone can challenge a number.

## What exists today

- Python collector against Idaho’s public court portal (Tyler Odyssey)
- Structured export of public case fields
- Operations notes for pacing, captcha handling, and post-run audits
- Explicit rule: the scraper has **no LLM dependency**. Model tools are not allowed to invent judge facts.

## What is not public yet (on purpose)

- Raw case HTML and working session state
- Unvalidated judge scores
- Collector credentials and portal session files

Those stay private until they are cleaned and the scoring methodology is locked.

## Related public work

- [Idaho Ledger](https://idaholedger.com) — bill and vote tracker
- [Idaho Scorecard](https://idahoscore.com) — elected-official scoring, including judges and sheriffs
- [Crime Clarity](https://github.com/idahofidelity/crime-clarity) — NIBRS race/ethnicity pipeline with reconciliation checks
