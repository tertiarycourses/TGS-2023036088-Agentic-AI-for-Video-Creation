# Lab 04 — Review and Refine the Edit

**Course:** Agentic AI for Video Creation (TGS-2023036088)  
**Day 2 · Topic 2 · about 60 minutes · slides 92–96 · K2, K3, A4, A5**  
**Agent:** Flova (Storyboard, Timeline, chat) + QC checklist  
**Features:** Scene-by-scene story review · technical QC · targeted fixes · regenerate one shot · auto captions · final export

## The story so far

The rough cut is in. Priya watched it once on her phone: "The story is nearly there, but something feels flat in the middle, and I could not hear the voice over the music." Review it properly, fix what matters, and export v2.

## Your goal

Review edited footage twice — once for story and emotion, once against technical parameters — then fix only what needs fixing.

## You'll produce

story-review.md, qc-report.md and EP01 v2 exported at 1080p

## What is in this folder

- `assets/story-review-template.md`
- `assets/qc-checklist.md`
- `assets/fix-log-template.md`
- `assets/sample/qc-report.md`
- `prompts.md` / `prompts.pdf` — every prompt, ready to paste
- `evidence/checklist.md` — what to capture as proof

## Why each step matters

- Two passes, two questions. The story pass asks "what does the viewer feel in this scene, and is it what we intended?" — the A4 skill. The technical pass asks "does this meet the parameter?" — the A5 skill.
- Watch on a phone first. Vertical video is judged on a phone, with thumbs ready to swipe; a laptop hides problems with caption size and pacing.
- Parameters are the measurable qualities of a video: resolution, aspect ratio, frame rate, duration, loudness and peaks, dialogue clarity, sync, caption accuracy and timing, colour and exposure consistency, and continuity (K3).
- Match each issue to a solution type (K2): regenerate one shot with locked references, re-time or trim on the timeline, lower the music under the voice, correct the captions, add a missing disclaimer, or replace an asset whose rights are unclear.
- Regenerate only the broken shot. Regenerating the whole episode spends credits and can break shots that were already right.

## Step by step

1. **Watch as a viewer** — Play v1 on your phone, full screen, sound on. Note where your attention drops.
2. **Review story and emotion** — Fill story-review.md scene by scene: intended feeling, actual feeling, proposed change.
3. **Check the parameters** — Work through qc-checklist.md: resolution, aspect ratio, frame rate, duration, loudness, captions, continuity.
4. **Choose three fixes** — Pick the three issues that matter most and the solution type for each.
5. **Fix in Flova** — Use Prompt A in the project chat; use the Timeline for timing and volume. Regenerate single shots only.
6. **Export v2** — Export at 1080p. Re-check the failed items and record the result in the fix log.

## The prompts

### PROMPT A — targeted fixes in Flova

> Make these three changes to the current cut and keep
> everything else exactly as it is:
>
> 1. Shot 4 drags. Shorten it to 8 seconds and add a quick
>    montage of three payday transfers.
> 2. The music is too loud under the narration. Duck the music
>    by about 8 dB whenever Rachel speaks.
> 3. In shot 5 Rachel's glasses are missing. Regenerate shot 5
>    only, using @Rachel exactly.
>
> Then regenerate the auto captions, check every caption against
> the narration, and show me the updated timeline.

### PROMPT B — ask the agent to check its work

> Before I export, list for this cut: total duration, aspect
> ratio, resolution, frame rate, whether captions are on every
> spoken line, and any shot where a character's look differs
> from their Element. Do not change anything — just report.

## Check your work

- [ ] story-review.md covers all six scenes with intended feeling, actual feeling and a proposed change.
- [ ] qc-report.md records a value and PASS or FAIL for every parameter.
- [ ] Each of your three fixes names its solution type.
- [ ] Only the broken shots were regenerated.
- [ ] v2 is 1080x1920, about 60 seconds, captions on, disclaimer on the end card.
- [ ] The fix log shows each failed item re-checked after the fix.

## If it goes wrong

- **Cannot measure loudness in Flova** — Use the Timeline volume and your ears for class; the trainer shows a loudness meter (for example ffmpeg loudnorm) on the projector.
- **The regenerated shot still differs** — Attach the Element image directly and repeat the five fixed traits in the prompt.

## Stretch

- Export a 15-second teaser from the same project for an Instagram Story.

> **Why it matters:** Review is where taste meets measurement. Fix the three things that matter, prove they are fixed, and stop.

## Next

Lab 05 — Hermes, Flova, Skills and a Compliance Review. Keep what you produced — the next lab starts from it.

## Safety

Use only this lab's fictitious characters and data and your own accounts. Never paste an API key, password or personal data into a prompt, a file you share or a screenshot. Nothing is uploaded publicly; upload plans stay private until a person approves.
