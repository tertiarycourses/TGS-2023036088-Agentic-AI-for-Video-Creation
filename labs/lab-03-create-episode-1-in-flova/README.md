# Lab 03 — Create Episode 1 with the Flova Video Agent

**Course:** Agentic AI for Video Creation (TGS-2023036088)  
**Day 1 · Topic 2 · about 75 minutes · slides 78–82 · K2, A4 (preparation)**  
**Agent:** Flova (flova.ai) — an AI video agent  
**Features:** Elements · Creative Brief · checkpoints · Storyboard · generation · Timeline · export

## The story so far

Planning is done. Priya has opened a Flova account for the studio. Your job today: get a first cut of Episode 1 that follows your storyboard and keeps Rachel, Ah Ma and the tin consistent from shot to shot.

## Your goal

Direct a video agent through brief, storyboard, generation and assembly — confirming at each checkpoint instead of hoping.

## You'll produce

Flova project "EP01 The Rainy-Day Tin" with three Elements, an approved storyboard and rough cut v1 exported

## What is in this folder

- `assets/flova-prompts.md`
- `assets/element-prompts.md`
- `assets/checkpoint-log-template.md`
- `prompts.md` / `prompts.pdf` — every prompt, ready to paste
- `evidence/checklist.md` — what to capture as proof

## Why each step matters

- Flova calls itself an all-in-one video agent: one chat that writes, storyboards, generates images, video, voice and music, and edits the timeline. You stay the director.
- Elements are Flova's reusable characters and props. Building them first, from your character bible, is what keeps Rachel the same person in shot 1 and shot 5.
- The Creative Brief card asks for project name, video type, target audience, output language, aspect ratio, duration, narrative driver, visual style and sound tonality. These are the same decisions you made in Lab 1.
- Choose to pause at key checkpoints rather than run everything in one pass. A checkpoint costs you a minute; a wrong generation costs credits.
- Generation runs in parallel and uses credits by model, length and resolution. Export the first cut at 720p; you will export the final at 1080p in Lab 4.

## Step by step

1. **Sign in** — Go to flova.ai and sign up or sign in. Check your credits; use the trainer's team account if you are short.
2. **Create Elements** — In Element, create Rachel, Ah Ma and the blue tin from your character bible (element-prompts.md).
3. **Start the project** — Projects → Create new. Mention the three Elements with @ and paste Prompt A.
4. **Fill the Creative Brief** — Set 9:16, 60 seconds, English, your audience and style. Choose to pause at key checkpoints.
5. **Check the storyboard** — Compare Flova's storyboard with yours. Prompt B corrects shots that differ.
6. **Approve the look** — At the visual-assets checkpoint, check every face against the Elements before you confirm.
7. **Rough cut and export** — Let Flova assemble the rough cut. Export v1 at 720p. Log every checkpoint decision.

## The prompts

### PROMPT A — start the project in Flova

> Create Episode 1 of Kopi & Coins, "The Rainy-Day Tin": a
> 60-second vertical (9:16) money story for young working adults
> in Singapore. Use @Rachel, @AhMa and @BlueTin as the cast and
> prop, and keep their look exactly as in the Elements.
>
> Follow this storyboard (attached as storyboard.md): six shots -
> the dead laptop and the $1,400 repair quote, the video call
> with Ah Ma, the blue tin full of labelled envelopes, Rachel
> setting up three savings buckets on payday, six months later
> paying calmly for a cracked phone, and the end card.
>
> Warm, hopeful, slice-of-life; soft natural light; Singapore
> HDB home. Narration in Rachel's voice, gentle piano music.
> Burn-in captions. End card: "Start your rainy-day tin this
> payday." and "For general education only. Not financial
> advice."
>
> Pause at each key checkpoint so I can review before you
> continue.

### PROMPT B — correct the storyboard

> Before generating, change the storyboard to match mine:
> - Shot 2 is a medium shot. Keep Rachel on the left of frame
>   and Ah Ma on the right for the whole call.
> - Shot 3 is a close-up insert of the tin. The lid opens to
>   show three envelopes labelled RAINY DAY, ANG PAO, HOLIDAY.
> - Shot 4 needs the on-screen text "Rule 1: rainy day first."
> Keep every other shot. Show me the revised storyboard.

## Check your work

- [ ] Rachel, Ah Ma and the blue tin exist as Elements.
- [ ] The Creative Brief is set to 9:16, 60 seconds and English.
- [ ] You paused at the storyboard and visual-asset checkpoints.
- [ ] The storyboard matches your six shots (or you recorded why not).
- [ ] Rachel looks the same in every shot of the rough cut.
- [ ] v1 is exported and your checkpoint log is saved.

## If it goes wrong

- **Not enough credits** — Make a 30-second version with three shots, or use the trainer's team account.
- **A face changes between shots** — Reply in the chat: "Shot 4: regenerate using @Rachel exactly; keep everything else."
- **Generation is slow** — It runs in parallel and can take several minutes. Move on to the checkpoint log while it works; do not restart the job.

## Stretch

- Ask Flova to save your workflow as a Skill so Episode 2 can reuse the brief and style.

> **Why it matters:** A video agent multiplies your decisions. Clear direction at the checkpoints is what turns credits into a usable cut.

## Next

Lab 04 — Review and Refine the Edit. Keep what you produced — the next lab starts from it.

## Safety

Use only this lab's fictitious characters and data and your own accounts. Never paste an API key, password or personal data into a prompt, a file you share or a screenshot. Nothing is uploaded publicly; upload plans stay private until a person approves.
