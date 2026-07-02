# Evals

The skill tells its users to build a 50-case eval set. This is the skill's own: 10 calibration cases with expected verdicts. Run them after any change to `SKILL.md`.

## How to run

For each case, invoke the skill with the case line as input and the instruction "assume the stated evidence is provided as [research]". Compare the verdict to the expected one.

Pass: ≥8/10 match. Hard fail: any strong↔weak inversion.

## Cases

| # | Case | Expected verdict | Why |
|---|------|------------------|-----|
| 1 | Restaurant phone answering + reservations (cf. Slang AI). Hosts on payroll, calls every hour, OpenTable/Yelp access | strong fit | Paycheck, hourly frequency, clear finish line, tool access — the episode's canonical example |
| 2 | Home-services dispatch + reception (cf. Same Day). Missed calls cost booked jobs, dispatcher on payroll | strong fit | Felt loss, paycheck, clear finish line |
| 3 | Auto-refunds under $50 for food delivery, written policy exists | strong fit | Bounded action, clear rules, clear finish line |
| 4 | Maintenance-request triage for property managers | strong fit | Episode example: high frequency, budget owner, learnable edge cases |
| 5 | Lead qualification + no-show recovery for med spas | strong fit | Episode example: paycheck (front desk), felt loss |
| 6 | General-purpose AI personal assistant "for everyone" | weak fit | No niche, no paycheck, no finish line |
| 7 | Fully autonomous "AI CEO" | weak fit | Pure judgment, no finish line — the Twitter-demo trap |
| 8 | Forward form submissions into a spreadsheet | weak fit | Too simple — basic automation does it, no judgment needed |
| 9 | AI therapy sessions replacing licensed therapists | weak fit | Pure human judgment plus regulatory risk; no learnable-in-v1 edge cases |
| 10 | Contract-clause negotiation for M&A deals | conditional | Huge paycheck, but edge cases are not learnable in v1; at best heavily-approved draft-and-approve |
