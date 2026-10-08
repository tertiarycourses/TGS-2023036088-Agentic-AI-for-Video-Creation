# Lab 06 — A Multi-Agent Video Studio on Kanban

**Course:** Agentic AI for Video Creation (TGS-2023036088)  
**Day 2 · Topic 3 · about 50 minutes · slides 128–133 · K5, A7**  
**Agent:** Hermes (profiles, Kanban, dashboard, cron) + Flova skill  
**Features:** kanban-video-orchestrator · five profiles · dependency chain · human approval gate · paused schedule · adoption plan

## The story so far

Episode 1 is approved. Priya wants Episode 2, Daniel's Bonus, made by a team of agents — producer, scriptwriter, director, reviewer and publisher — with her approval as the last gate. Then she wants a plan for rolling this out to the whole studio.

## Your goal

Coordinate several Hermes agents on a Kanban board to produce Episode 2, and plan how the studio adopts the new technology.

## You'll produce

Five profiles, a Kanban board with the Episode 2 dependency chain, an EP02 draft in Flova, a paused weekly schedule and adoption-plan.md

## What is in this folder

- `assets/profiles/producer/SOUL.md`
- `assets/profiles/scriptwriter/SOUL.md`
- `assets/profiles/director/SOUL.md`
- `assets/profiles/reviewer/SOUL.md`
- `assets/profiles/publisher/SOUL.md`
- `assets/episode-02-brief.md`
- `assets/kanban-commands.md`
- `assets/adoption-plan-template.md`
- `prompts.md` / `prompts.pdf` — every prompt, ready to paste
- `evidence/checklist.md` — what to capture as proof

## Why each step matters

- One agent became a team because the work split into jobs with different skills and different points of view. The reviewer must not be the agent that made the video.
- Each profile is a separate Hermes home with its own SOUL.md (personality and rules), memory, skills and keys. The Director is the only one that needs the Flova skill.
- Kanban makes the order visible and durable: a child task stays in todo until every parent is done, crashed work can be retried, and a human can comment on any card. Publishing waits for your approval card.
- Scheduling is the last step, not the first. Run the pipeline by hand once, inspect every handoff, then create the schedule — and keep it paused until the owner approves.
- Adoption is the A7 skill: a pilot with a baseline, measures (time per episode, credits per episode, rework rate, compliance pass rate), training, governance and a decision point to scale.

## Step by step

1. **Install the orchestrator** — hermes skills install official/creative/kanban-video-orchestrator
2. **Create the team** — Create five profiles and copy each SOUL.md from assets/profiles/<name>/ into ~/.hermes/profiles/<name>/.
3. **Build the board** — Prompt A asks the producer to brief, design the board and create the tasks with dependencies.
4. **Run and watch** — Start the gateway (it runs the dispatcher) and open the dashboard. Watch cards move.
5. **Approve as a human** — When the review card is done, read the report and comment APPROVED — or send it back.
6. **Schedule, paused** — Create the weekly schedule, then pause it until Priya signs off.
7. **Plan the adoption** — Prompt B drafts adoption-plan.md; edit the pilot, metrics and risks yourself.

## The prompts

### COMMANDS — create the studio team

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

### PROMPT A — to the producer

> /kanban-video-orchestrator Produce Episode 2 of Kopi & Coins,
> "Daniel's Bonus", from episode-02-brief.md: 60 seconds, 9:16,
> same characters and style as Episode 1.
>
> Team: producer (you, never renders), scriptwriter, director
> (uses the flova skill), reviewer (uses kopi-compliance-review,
> never edits), publisher.
>
> Write brief.md and wait for my confirmation. Then create the
> Kanban tasks in this order, each depending on the one before:
> script -> storyboard -> Flova draft -> compliance and story
> review -> human approval (assigned to me) -> private upload
> plan. The publisher must not start until I comment APPROVED.

### PROMPT B — the adoption plan

> Draft adoption-plan.md for rolling out Hermes and Flova
> across the Kopi & Coins studio. Include:
> - the problem it solves and today's baseline (time, cost,
>   rework per episode - use our Episode 1 log)
> - a four-week pilot: scope, team, success measures
> - the metrics we will track every week
> - training and support for two editors and a producer
> - governance: approval gates, API keys, credit limits,
>   compliance checks, AI-content labelling
> - risks and how we reduce them
> - the decision point to scale, stop or change.

## Check your work

- [ ] Five profiles exist, each with its own SOUL.md.
- [ ] The board shows the six tasks with parent dependencies.
- [ ] The reviewer and the director are different profiles.
- [ ] Publishing stayed blocked until you commented APPROVED.
- [ ] The weekly schedule exists and is paused.
- [ ] adoption-plan.md has a baseline, pilot measures, governance and a decision point.

## If it goes wrong

- **Cards never start** — The dispatcher runs in the gateway: check hermes gateway status, and that assignees match profile names exactly.
- **Flova draft is still generating at the end** — Fine for class — screenshot the card and the Flova progress; the pipeline is the evidence.
- **A worker loops** — Block the card with a comment and re-scope the task.

## Stretch

- Connect Telegram to the gateway so Priya can approve from her phone.

> **Why it matters:** Agents scale the work; Kanban keeps it in order; the approval card keeps a person responsible.

## Next

You have finished the labs. Bring your evidence to the Practical Performance assessment.

## Safety

Use only this lab's fictitious characters and data and your own accounts. Never paste an API key, password or personal data into a prompt, a file you share or a screenshot. Nothing is uploaded publicly; upload plans stay private until a person approves.
