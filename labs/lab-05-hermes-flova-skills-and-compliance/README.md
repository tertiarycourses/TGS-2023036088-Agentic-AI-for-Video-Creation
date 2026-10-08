# Lab 05 — Hermes, Flova, Skills and a Compliance Review

**Course:** Agentic AI for Video Creation (TGS-2023036088)  
**Day 2 · Topic 3 · about 60 minutes · slides 113–118 · K4, A6**  
**Agent:** Hermes Agent (Desktop or CLI) + Flova CLI  
**Features:** Install Hermes · connect Flova · hub skills · plugins · a custom compliance skill · remedial action plan

## The story so far

Kopi & Coins wants to publish two episodes a week. Priya cannot review every one herself, and one non-compliant money video could cost the studio its reputation. Set up Hermes as the studio's agent, connect it to Flova, and give it a compliance skill.

## Your goal

Give an always-on agent the tools (Flova), skills (compliance review) and plugins it needs, then use it to find and fix non-compliance in Episode 1.

## You'll produce

Hermes with Flova connected, the kopi-compliance-review skill, and compliance-report.md with remedial actions for EP01 v2

## What is in this folder

- `assets/skills/kopi-compliance-review/SKILL.md`
- `assets/skills/kopi-compliance-review/references/standards.md`
- `assets/episode-01-v2-notes.md`
- `assets/remedial-action-template.md`
- `assets/sample/compliance-report.md`
- `prompts.md` / `prompts.pdf` — every prompt, ready to paste
- `evidence/checklist.md` — what to capture as proof

## Why each step matters

- Hermes Agent (Nous Research) is an open-source agent that runs on your computer or a server, remembers across sessions and can stay on all day — that is the "AI agent" in this course's sense.
- Flova publishes an Agent CLI with a skill that tells other agents how to drive it. Hermes reads that skill, so it can create Flova projects, read real progress and export videos for you.
- A skill is instructions (SKILL.md plus references) loaded when the task matches. A plugin is code that adds tools, hooks or commands to Hermes. MCP connects an outside server. Use the lightest one that does the job.
- The compliance skill turns the studio's standards into a repeatable review: platform specs, loudness, captions, copyright, personal data, money messaging and AI-content labelling (K4).
- A finding is only useful with a remedy. The remedial action plan is the A6 skill: for each non-compliance, the standard it breaks, the risk, the corrective action, the owner and the due date.

## Step by step

1. **Install Hermes** — Download Hermes Desktop, or run the install command in a terminal. Then run hermes setup to choose a model.
2. **Connect Flova** — Paste the Flova setup prompt into Hermes. Sign in when the browser opens. Never paste the key into a file.
3. **Check the skills** — Run hermes skills list. Confirm flova is there; install youtube-content if it is missing.
4. **Look at plugins** — Run hermes plugins list. Enable the plugin the trainer names; note how a plugin differs from a skill.
5. **Add the compliance skill** — Copy the folder assets/skills/kopi-compliance-review into ~/.hermes/skills/. Start a new chat so Hermes loads it.
6. **Run the review** — Prompt B runs /kopi-compliance-review on Episode 1 v2 and writes compliance-report.md.
7. **Plan the remedies** — Check every finding. Complete the remedial action plan: owner, action, due date.

## The prompts

### COMMANDS — install Hermes (macOS / Linux / WSL2)

```
curl -fsSL https://hermes-agent.nousresearch.com/install.sh | bash
hermes setup          # choose a model provider and sign in
hermes doctor         # check the install
hermes skills list    # what skills are loaded
hermes plugins list   # what plugins are installed
```

### PROMPT A — connect Flova (paste into Hermes)

> Please help me install Flova CLI:
> https://cli.flova.ai/flovaCLI-setup.md
>
> Link the Flova skill into ~/.hermes/skills/flova so Hermes can
> use it. Open the browser for me to sign in. Never print, log or
> save my API key. When you are done, show me that the flova
> skill is listed.

### PROMPT B — run the compliance review

> /kopi-compliance-review Review Episode 1 v2 of Kopi & Coins.
> Use the notes in episode-01-v2-notes.md and, through the Flova
> skill, read the real project state of "EP01 The Rainy-Day Tin":
> its storyboard, captions, music and export settings.
>
> Write compliance-report.md: one row per finding with the
> standard it breaks, the evidence, the risk (high, medium, low)
> and a proposed remedial action. Mark anything you could not
> verify as UNVERIFIED. Do not change the video.

## Check your work

- [ ] hermes doctor passes and a model answers in chat.
- [ ] hermes skills list shows flova and kopi-compliance-review.
- [ ] You can explain the difference between a skill, a plugin and MCP.
- [ ] compliance-report.md has evidence and a risk rating per finding.
- [ ] Every finding has a remedial action, an owner and a due date.
- [ ] No API key appears in any file, prompt or screenshot.

## If it goes wrong

- **hermes: command not found** — Open a new terminal, or add ~/.local/bin to your PATH, then run hermes doctor.
- **The Flova login does not open** — Generate an Agent API key on flova.ai/en/agent-cli and give it to the agent when it asks — never in a file you share.
- **The skill does not appear** — Check the folder name matches the name in SKILL.md, then start a new session.

## Stretch

- Ask Hermes to fix one low-risk finding in Flova (for example the caption line length) and re-run the review.

> **Why it matters:** Standards protect the studio only when they are applied every time. A skill makes the review repeatable; the remedy plan makes it useful.

## Next

Lab 06 — A Multi-Agent Video Studio on Kanban. Keep what you produced — the next lab starts from it.

## Safety

Use only this lab's fictitious characters and data and your own accounts. Never paste an API key, password or personal data into a prompt, a file you share or a screenshot. Nothing is uploaded publicly; upload plans stay private until a person approves.
