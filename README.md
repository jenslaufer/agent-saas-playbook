# Agent SaaS Playbook

Greg Isenberg's ["AI Agents are the new SaaS"](https://www.youtube.com/watch?v=83fWzQSWB10) playbook as an installable agent skill. Works in **Claude Code** and **OpenAI Codex** — one skill, two manifests.

The core idea: SaaS sells software. Agent SaaS sells work — the product is the job. This skill turns that episode into a repeatable validation workflow you run *before* building an agent business.

## What it does

Give it a niche or an idea. It walks the full playbook:

1. Finds the paycheck — who gets paid for this work today (your pricing anchor)
2. Lists up to 20 candidate workflows and scores each on 5 traits (frequency, pain cost, clear finish line, software access, budget owner)
3. Returns a verdict: **strong fit / conditional / weak fit** — honestly
4. Plans the human-shadowing phase (10–20 real cases)
5. Writes the 7-part agent spec (trigger, context, tools, actions, approvals, escalation, success)
6. Picks the minimal useful agent shape: draft-and-approve, triage, coordinator, or bounded action
7. Plans the trust wrapper and a 50-case eval set
8. Anchors pricing against labor cost, with a path to outcome pricing
9. Sketches distribution via workflow teardowns
10. Produces a 30-day zero-to-100 plan

## Install

### Claude Code

```
/plugin marketplace add jenslaufer/agent-saas-playbook
/plugin install agent-saas@agent-saas-playbook
```

### OpenAI Codex

```
codex plugin marketplace add jenslaufer/agent-saas-playbook
codex plugin add agent-saas
```

## Use

Ask naturally:

- "Validate my agent idea: an AI receptionist for physiotherapy practices"
- "Could this be an agent business? Invoice intake for tax offices"
- "Run the agent-saas playbook on the home-services niche"

The skill stops and asks when inputs are missing — it never guesses who pays for the work today.

## Example run

Input: *"Could this be an agent business? Missed-call handling for physical therapy clinics"*

The skill asks for the paycheck first. Front-desk staff at ~$20/hr handle the phone today (`[research]`: job postings). Then it scores 20 candidate workflows. Top three:

| Workflow | Frequency | Pain cost | Finish line | Software access | Budget owner | Total |
|---|---|---|---|---|---|---|
| Missed-call answering + booking | 5 | 5 | 5 | 3 `[hypothesis]` | 5 | 23 |
| Insurance eligibility checks | 4 | 5 | 4 | 3 `[hypothesis]` | 4 | 20 |
| No-show recovery | 3 | 4 | 5 | 4 | 4 | 20 |

**Verdict: conditional.** Paycheck and pain are evidenced (`[research]`: job postings, clinic-owner forum threads). The software-access score is a `[hypothesis]` until 10 clinics confirm their phone and practice-management stack — that shadowing evidence would upgrade the verdict to strong fit.

The output continues with the 7-part agent spec, the MUA pick (draft-and-approve on call summaries and bookings), the wrapper and 50-case eval plan, pricing anchored at ~$1,200/month against ~$3,400/month labor cost, the 30-day plan — and the closing move: name 3 clinics, book the conversations this week.

## Evals

The skill preaches a 50-case eval set. It eats its own cooking: [evals/](evals/README.md) holds 10 calibration cases with expected verdicts. Run them after any change to the skill.

## Credit

The playbook is Greg Isenberg's, from The Startup Ideas Podcast, ep. 348 (July 2026): [AI Agents are the new SaaS](https://www.youtube.com/watch?v=83fWzQSWB10). This plugin distills it into a skill. Watch the episode.

## License

MIT
