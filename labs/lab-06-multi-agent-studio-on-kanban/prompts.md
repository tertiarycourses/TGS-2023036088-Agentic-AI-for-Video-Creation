# Prompts — Lab 06: A Multi-Agent Video Studio on Kanban

Agent: Hermes (profiles, Kanban, dashboard, cron) + Flova skill. Paste each prompt as written; change only what the lab tells you to.

## COMMANDS — create the studio team

```
hermes skills install official/creative/kanban-video-orchestrator
hermes profile create producer
hermes profile create scriptwriter
hermes profile create director
hermes profile create reviewer
hermes profile create publisher
# copy assets/profiles/<name>/SOUL.md to ~/.hermes/profiles/<name>/
hermes kanban init
hermes gateway start      # runs the Kanban dispatcher
hermes dashboard          # opens the board in your browser
```

## PROMPT A — to the producer

```
/kanban-video-orchestrator Produce Episode 2 of Kopi & Coins,
"Daniel's Bonus", from episode-02-brief.md: 60 seconds, 9:16,
same characters and style as Episode 1.

Team: producer (you, never renders), scriptwriter, director
(uses the flova skill), reviewer (uses kopi-compliance-review,
never edits), publisher.

Write brief.md and wait for my confirmation. Then create the
Kanban tasks in this order, each depending on the one before:
script -> storyboard -> Flova draft -> compliance and story
review -> human approval (assigned to me) -> private upload
plan. The publisher must not start until I comment APPROVED.
```

## PROMPT B — the adoption plan

```
Draft adoption-plan.md for rolling out Hermes and Flova
across the Kopi & Coins studio. Include:
- the problem it solves and today's baseline (time, cost,
  rework per episode - use our Episode 1 log)
- a four-week pilot: scope, team, success measures
- the metrics we will track every week
- training and support for two editors and a producer
- governance: approval gates, API keys, credit limits,
  compliance checks, AI-content labelling
- risks and how we reduce them
- the decision point to scale, stop or change.
```
