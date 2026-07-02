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

## Credit

The playbook is Greg Isenberg's, from The Startup Ideas Podcast, ep. 348 (July 2026): [AI Agents are the new SaaS](https://www.youtube.com/watch?v=83fWzQSWB10). This plugin distills it into a skill. Watch the episode.

## License

MIT
