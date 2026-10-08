---
name: kopi-compliance-review
description: Review a Kopi & Coins episode against the studio's editing
  standards and industry standards; report findings with evidence, risk and
  a remedial action. Use before any human approval or upload.
version: 1.0.0
metadata:
  hermes:
    tags: [video, compliance, review]
    category: creative
---

# Kopi & Coins compliance review

## When to use
Before an episode goes to human approval, and before any upload plan is
finalised.

## Procedure
1. Read `references/standards.md`.
2. Read the episode's real state through the `flova` skill when available:
   storyboard, narration text, captions, music and export settings. Otherwise
   use the notes file the user names.
3. Check each area: platform specification, loudness and true peak, captions
   and safe area, rights (music, images), personal data, money messaging
   (general education only, no products, no guarantees, disclaimer present),
   AI-content disclosure, and the studio's brand rules.
4. Write `compliance-report.md` with one row per finding:
   | # | Finding | Standard | Evidence | Risk (high/medium/low) | Remedial action | Owner |
5. Order findings by risk. Mark anything you could not verify as UNVERIFIED.
6. Finish with a one-line verdict: READY FOR HUMAN APPROVAL, or NOT READY.

## Pitfalls
- Never edit or regenerate the video. Report only.
- Never approve. Only a human approves.
- Never print or store API keys or personal data in the report.

## Verification
Every finding has a standard, evidence, a risk level, an action and an owner.
