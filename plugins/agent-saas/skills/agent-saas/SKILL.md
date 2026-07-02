---
name: agent-saas
description: Validates and specs an AI-agent business idea using the "Agents are the new SaaS" playbook (Greg Isenberg) — scores candidate workflows on 5 traits, writes the 7-part agent spec, picks the minimal useful agent shape, anchors pricing against labor cost, and produces a 30-day plan. Use when the user wants to build or evaluate an agent business, asking "agent saas / agent business / validate my agent idea / sell agents / isenberg playbook / could this be an agent business".
---

The agent-business check, built on one principle: **SaaS sells software. Agent SaaS sells work — the product is the job.** You compete with labor cost, not software budgets.

Run this BEFORE building. You earn the software by doing the work first.

## Mandatory workflow — do every step in order

1. **Gather inputs.** Ask the user only for what is missing:
   - Niche (or idea) + target customer
   - **Who gets paid for this work today?** (employee, agency, freelancer — role + rough cost). This is the pricing anchor and the proof of willingness to pay.
   - What software the niche already runs on (inbox, phone system, CRM, Stripe, …)
   Stop and ask if any is unknown — never guess the paycheck silently.

2. **List candidate workflows.** Up to 20 jobs people in the niche complain about (or the ones the user names). List them all — no silent skipping.

3. **Score each workflow** on the 5 traits, as a table (1–5 each + total):
   - **Frequency** — hourly beats daily beats weekly
   - **Pain cost** — the buyer feels the loss (missed calls, dropped leads, expensive humans on low-value coordination)
   - **Clear finish line** — job booked, ticket categorized, refund approved
   - **Software access** — touches tools an agent can use and context it can read
   - **Budget owner** — someone already pays for this and can sign
   Sweet spot: repetitive with enough judgment that AI helps. Too simple → basic automation suffices; pure human judgment → version 1 breaks. Flag both.

4. **Verdict** for the top workflow: **strong fit / conditional / weak fit**. Name the binding constraint (frequency? paycheck? tool access?). Label every assumption with its source (user data vs. estimate).

5. **Shadow plan.** Before any prompt or code: watch a human do the job 10–20 real cases (screen recording, narrating). Specify what to extract: what they check before deciding, where mistakes happen, what makes a case easy vs. weird. The hidden detail IS the product. Note: operators can be paid for this.

6. **Agent spec — all 7 parts:** trigger (what wakes it), context it needs, tools it may use, actions it may take alone, approval points, escalation rules, success criterion.

7. **Pick the MUA shape.** Smallest useful agent, one of four — with a one-line rationale:
   - **Draft-and-approve** — drafts reply/quote/summary, human approves (risk or creativity involved)
   - **Triage** — classifies inbound work and routes it
   - **Coordinator** — moves work between systems and people (availability, reminders, missing info)
   - **Bounded action** — acts alone under clear rules ("refunds under $50")
   Principle (Anthropic guidance): start as a predictable workflow; earn autonomy by adding judgment only where it creates value. One workflow + one promise is enough for day one.

8. **Wrapper + eval plan.** The agent does the work; the wrapper creates the trust that makes it SaaS. Name the control-room contents for this workflow (logs, approvals, handoff rules, analytics, test-before-live). Plan the eval set: 50 real cases with correct answers marked; every prompt/model/tool change re-runs against it. It doubles as a sales asset ("tested on 50 of your old tickets: 42 right, 6 escalated, 2 mistakes + how we fixed them").

9. **Pricing.** Anchor against today's labor cost from step 1. Start simple: setup fee + flat monthly per workflow (reference: ~$1,500 setup + $1,000/month). Move to usage/outcome pricing only once the value is understood (e.g. $30 per qualified appointment, $3,000/month up to 500 tickets). Pilot: 3 customers in ONE niche, same workflow, sold as the outcome ("we answer and qualify your missed calls"). Exact price matters less than learning what the customer values, where the agent breaks, and what they'd miss.

10. **Distribution sketch.** Workflow teardowns: show the painful old way vs. the agent way — owners feel that pain. One platform, checklists/benchmarks/~50 posts on the workflow, paid ads behind the winners. If a channel-evaluation skill is available (e.g. `channel-fit`), recommend running it for the full distribution feasibility check — don't duplicate it here.

11. **Output.** One document containing: scoring table, verdict, pricing-anchor math, agent spec, MUA recommendation, wrapper + eval plan, pricing proposal, and the 30-day plan:
    - **Week 1:** pick niche → interview 10 operators (screen-share) → pick workflow → write spec → run the job manually with AI (tests whether AI helps before building software) → build the MUA → eval set from 50 real cases
    - **Week 2:** sell 2 pilots in the same niche
    - **Week 3:** build the wrapper (logs, approvals, settings, analytics)
    - **Week 4:** publish teardowns, turn pilots into proof
    - Audience building runs from day 1.
    Save to `{project}/marketing/strategy/agent-saas_{slug}.md` if a project context exists, else present in-chat.

## Notes

- This skill validates and specs; it does not build the agent. Hand the spec to your implementation workflow (task spec, backend, frontend).
- Be honest: say **weak fit** plainly when the scoring shows it. No talking an idea into fitness.
- Source: Greg Isenberg, Startup Ideas Podcast, "AI Agents are the new SaaS" (July 2026), https://www.youtube.com/watch?v=83fWzQSWB10
