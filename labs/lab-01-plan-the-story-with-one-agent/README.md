# Lab 01 — Plan the Story with a Single AI Agent

**Course:** Agentic AI for Video Creation (TGS-2023036088)  
**Day 1 · Topic 1 · about 50 minutes · slides 45–51 · K1, A1**  
**Agent:** ChatGPT (or Claude / Gemini) — one AI agent  
**Features:** Creative brief · 60-second script · script review for edits · quality-issue forecast

## The story so far

Priya wants Episode 1, The Rainy-Day Tin, live in two weeks. Before anyone spends a credit on video, the story has to work on paper — and you need to know which edits and which quality risks each scene will bring.

## Your goal

Use one AI agent to turn an idea into a brief and a timed script, then review the script to decide the edits each scene needs.

## You'll produce

creative-brief.md, script-v1.md and script-review.md for Episode 1

## What is in this folder

- `assets/studio-brief.md`
- `assets/episode-01-idea.md`
- `assets/script-review-template.md`
- `assets/sample/script-v1.md`
- `assets/sample/script-review.md`
- `prompts.md` / `prompts.pdf` — every prompt, ready to paste
- `evidence/checklist.md` — what to capture as proof

## Why each step matters

- One agent is enough here. Planning is a single line of thought — brief, script, review — and a second agent would only repeat it. You will add agents in Topic 3, when the work splits into different jobs.
- Attach the two files rather than pasting them, so the agent can re-read them at every step. That is the agent's context.
- The brief comes before the script because it fixes the audience, the one message and the rules. A script written without a brief drifts into generic money tips.
- The script review is the A1 skill: reading a script and deciding which edits will deliver the creative vision — a match cut between the tin and the banking app, a montage for "six months later", a text overlay for the rule.
- Your decision step matters. The agent proposes; the producer decides. Record why you rejected a suggestion — that note is evidence of judgement.

## Step by step

1. **Open one agent** — Start a new chat in ChatGPT (or Claude or Gemini). Attach studio-brief.md and episode-01-idea.md.
2. **Brief first** — Paste Prompt A. Read the brief and correct anything that does not match the studio rules.
3. **Write the script** — Paste Prompt B: six timed scenes, voice-over, on-screen text and sound for 60 seconds.
4. **Review for edits** — Paste Prompt C. For every scene the agent names the edit types it needs and why.
5. **Forecast quality issues** — Paste Prompt D: the quality issues most likely in each scene and how to prevent them.
6. **Decide as the producer** — Accept or reject at least two of the agent's suggestions. Save the three files in a folder kopi-ep01.

## The prompts

### PROMPT A — creative brief

> You are a video producer for Kopi & Coins. Read the two
> attached files.
>
> Write a one-page creative brief for Episode 1, "The Rainy-Day
> Tin", as Markdown with these headings: audience, the one
> message, platform and format (9:16, 60 seconds), tone, story
> logline, characters, call to action, must include, must avoid.
>
> Rules: general money education only. No product names, no
> promised returns, no numbers we cannot source. Ask me up to
> three questions before you write if anything is unclear.

### PROMPT B — the 60-second script

> Using the approved brief, write the script for Episode 1.
>
> Six scenes, timed to exactly 60 seconds:
> hook (0-5s), set-up, turn, choice, payoff, end card (55-60s).
>
> For each scene give: time range, what we SEE, voice-over or
> dialogue, on-screen text, and sound (music cue or effect).
> Keep spoken lines short — under 140 words in total.
> End card: "Start your rainy-day tin this payday." plus the
> disclaimer from the studio brief.

### PROMPT C — script review for edits

> Review script-v1 as a video editor before production.
>
> Make a table, one row per scene: scene, what the scene must
> make the viewer feel, the edit types it needs (for example cut,
> cutaway or B-roll, match cut, montage, J or L cut, text
> overlay, speed ramp, transition, music cue), and why each edit
> serves the story.
>
> Then list two scenes where a different edit would be stronger,
> and say what you would change.

### PROMPT D — quality-issue forecast

> For the same six scenes, forecast the quality issues we are
> most likely to meet when an AI video agent makes this episode.
>
> Group them as: technical (picture and sound), AI generation
> (for example face drift, extra fingers, garbled text), story
> and continuity, and compliance (music rights, disclaimer,
> misleading money claims).
>
> For each issue give the scene, how we would notice it, and
> one way to prevent it in the prompt or the edit.

## Check your work

- [ ] The brief names one audience, one message and the must-avoid rules.
- [ ] The script has six scenes that add up to exactly 60 seconds.
- [ ] The end card carries the call to action and the disclaimer.
- [ ] script-review.md lists the edit types for every scene, with a reason for each.
- [ ] The quality forecast covers all four groups of issues.
- [ ] You accepted or rejected at least two suggestions and wrote why.

## If it goes wrong

- **The agent invents statistics** — Reply: "Remove every number you cannot source. Use general wording instead."
- **The script runs long** — Ask for a word count per scene and a 140-word cap; spoken English runs about 2.5 words a second.

## Stretch

- Ask the agent for a 30-second cut-down of the same script and compare which scenes survive.

> **Why it matters:** The cheapest place to fix a video is the script. Every edit you decide now is a regeneration you will not pay for later.

## Next

Lab 02 — Storyboard, Editing Standards and Work Plan. Keep what you produced — the next lab starts from it.

## Safety

Use only this lab's fictitious characters and data and your own accounts. Never paste an API key, password or personal data into a prompt, a file you share or a screenshot. Nothing is uploaded publicly; upload plans stay private until a person approves.
