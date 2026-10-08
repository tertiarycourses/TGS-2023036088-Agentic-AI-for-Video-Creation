# Lab 02 — Storyboard, Editing Standards and Work Plan

**Course:** Agentic AI for Video Creation (TGS-2023036088)  
**Day 1 · Topic 1 · about 60 minutes · slides 58–64 · A2, A3**  
**Agent:** ChatGPT (same chat) + a spreadsheet  
**Features:** Character bible · six-shot storyboard · editing standards and guidelines · post-production work plan

## The story so far

The script is approved. Before the video agent can make anything, the studio needs a character bible so Rachel looks the same in every shot, a storyboard, the editing rules every episode must follow, and a plan with dates.

## Your goal

Turn the approved script into the documents a production team — human or AI — works from.

## You'll produce

character-bible.md, storyboard.md, editing-standards.md and work-plan.csv

## What is in this folder

- `assets/character-bible-template.md`
- `assets/storyboard-template.md`
- `assets/editing-standards-template.md`
- `assets/work-plan-template.csv`
- `assets/sample/storyboard.md`
- `assets/sample/editing-standards.md`
- `prompts.md` / `prompts.pdf` — every prompt, ready to paste
- `evidence/checklist.md` — what to capture as proof

## Why each step matters

- A character bible lists the traits that must never change — face, hair, glasses, clothes, the prop. AI video models forget; repeating the same five traits in every shot prompt is how you keep Rachel recognisable.
- Storyboard in shots, not scenes. A shot has one size (close-up, medium, wide), one angle, one movement and one action. That is the unit a video model generates well.
- The continuity line tells the next shot what must stay the same: same cardigan, same tin, same light, Rachel moving left to right.
- Editing standards are the A2 skill: guidelines every editor (and every agent) follows, written against legal requirements — copyright, personal data, fair money messaging — and broadcasting or platform standards such as loudness, safe areas and captions.
- The work plan is the A3 skill: the post-production stages in order, each with an owner, a duration and a review gate, so the episode can hit its date.

## Step by step

1. **Lock the characters** — Prompt A builds the character bible: fixed visible traits for Rachel, Ah Ma and the blue tin.
2. **Storyboard six shots** — Prompt B: one row per shot — shot size, angle, movement, action, duration and a continuity line.
3. **Check the grammar** — Look for the 180-degree rule and screen direction between shots 2 and 3. Fix any jump.
4. **Write the standards** — Prompt C: the studio's editing standards and guidelines, legal and platform rules included.
5. **Plan the post-production** — Prompt D gives a work plan; paste it into work-plan.csv and set real dates.
6. **Peer review** — Swap storyboards with a partner. Each names one continuity risk in the other's board.

## The prompts

### PROMPT A — character bible

> Create a character bible for Kopi & Coins as Markdown.
>
> For Rachel Tan (29), Ah Ma (74) and the blue butter-cookie
> tin, give: role in the story, five visible traits that must
> never change (face, hair, clothing, accessories, colours), how
> they move and speak, and one reference-image prompt each
> (front view, neutral light, plain background).
>
> Rachel: shoulder-length black hair, round tortoiseshell
> glasses, mustard-yellow cardigan over a white T-shirt.
> Ah Ma: short silver permed hair, jade bangle, floral blouse.

### PROMPT B — six-shot storyboard

> Turn script-v1 into a six-shot storyboard as a Markdown table.
>
> Columns: shot, time, shot size (ECU, CU, MCU, MS, WS), camera
> angle, camera movement, action (one only), characters, sound,
> on-screen text, continuity line (what must stay the same as the
> previous shot).
>
> Keep 9:16 framing in mind: faces in the upper third, text clear
> of the bottom 20% of the frame. Respect the 180-degree rule in
> the video-call scene.

### PROMPT C — editing standards and guidelines

> Write editing-standards.md: the rules every Kopi & Coins
> episode must meet before it is published.
>
> Sections:
> 1. Brand: colours, fonts, logo position, end card.
> 2. Story: hook in the first 3 seconds, one message, pacing.
> 3. Captions: always on, accuracy, line length, safe area.
> 4. Audio: dialogue clarity, music under voice, loudness target.
> 5. Legal: music and image rights, no personal data, money
>    messaging (general education only, no promised returns,
>    disclaimer), labelling AI-generated content.
> 6. Platform: 9:16, 1080x1920, frame rate, duration limits.
>
> Make every rule checkable, with a number or a yes/no test.

### PROMPT D — post-production work plan

> Create a post-production work plan for Episode 1 as CSV with
> columns: stage, task, owner, start day, duration (hours),
> depends on, review gate, done when.
>
> Stages in order: references and elements, generation, assembly
> (rough cut), story review, fine cut, sound mix, captions,
> technical QC, compliance review, approval, export, publish.
>
> We have 10 working days. Put a human approval gate before
> publish, and allow one day for regenerating failed shots.

## Check your work

- [ ] The character bible fixes five visible traits each for Rachel, Ah Ma and the tin.
- [ ] The storyboard has six shots, each with one size, one angle, one movement and one action.
- [ ] Every shot has a continuity line.
- [ ] editing-standards.md covers brand, story, captions, audio, legal and platform — each rule checkable.
- [ ] work-plan.csv lists every stage with an owner, a duration and a review gate, and fits 10 working days.
- [ ] Your partner named one continuity risk and you fixed it.

## If it goes wrong

- **The storyboard has two actions per shot** — Split it. One shot, one action.
- **Loudness target unclear** — Use -14 LUFS integrated with true peak no higher than -1 dBTP for social platforms; note the broadcast standard (EBU R128, -23 LUFS) for comparison.

## Stretch

- Ask the agent to turn editing-standards.md into a yes/no checklist you can reuse in Lab 4.

> **Why it matters:** Standards written down are standards an agent can follow. Standards in your head are surprises at review time.

## Next

Lab 03 — Create Episode 1 with the Flova Video Agent. Keep what you produced — the next lab starts from it.

## Safety

Use only this lab's fictitious characters and data and your own accounts. Never paste an API key, password or personal data into a prompt, a file you share or a screenshot. Nothing is uploaded publicly; upload plans stay private until a person approves.
