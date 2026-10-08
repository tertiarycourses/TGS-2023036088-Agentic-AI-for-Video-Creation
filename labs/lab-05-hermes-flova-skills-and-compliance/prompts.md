# Prompts — Lab 05: Hermes, Flova, Skills and a Compliance Review

Agent: Hermes Agent (Desktop or CLI) + Flova CLI. Paste each prompt as written; change only what the lab tells you to.

## COMMANDS — install Hermes (macOS / Linux / WSL2)

```
curl -fsSL https://hermes-agent.nousresearch.com/install.sh | bash
hermes setup          # choose a model provider and sign in
hermes doctor         # check the install
hermes skills list    # what skills are loaded
hermes plugins list   # what plugins are installed
```

## PROMPT A — connect Flova (paste into Hermes)

```
Please help me install Flova CLI:
https://cli.flova.ai/flovaCLI-setup.md

Link the Flova skill into ~/.hermes/skills/flova so Hermes can
use it. Open the browser for me to sign in. Never print, log or
save my API key. When you are done, show me that the flova
skill is listed.
```

## PROMPT B — run the compliance review

```
/kopi-compliance-review Review Episode 1 v2 of Kopi & Coins.
Use the notes in episode-01-v2-notes.md and, through the Flova
skill, read the real project state of "EP01 The Rainy-Day Tin":
its storyboard, captions, music and export settings.

Write compliance-report.md: one row per finding with the
standard it breaks, the evidence, the risk (high, medium, low)
and a proposed remedial action. Mark anything you could not
verify as UNVERIFIED. Do not change the video.
```
