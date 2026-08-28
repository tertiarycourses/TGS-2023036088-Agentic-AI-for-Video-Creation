# Agentic AI for Video Creation

Build a governed, end-to-end agentic video-production workflow—from evidence-backed research and generative content to human approval, SocialPost/YouTube release, and performance feedback.

| Course detail | Information |
|---|---|
| Course code | `TGS-2023036088` |
| Programme | WSQ |
| TSC | `MED-MPN-4005-1.1 — Video Editing-4` |
| Duration | 2 days / 16 training hours, plus 2 hours of assessment |
| Registration | [View course details and register](https://www.tertiarycourses.com.sg/wsq-agentic-ai-for-video-creation.html) |
| Funding | Up to 70% course-fee support may apply. Eligibility and terms apply; verify the current course page before enrolment. |
| Courseware version | v2.0 — 29 August 2026 |

## About the course

This technical course treats video creation as a controlled production system rather than a chain of unverified prompts. Learners use n8n to preserve evidence and state across research, scripting, storyboard generation, generative-media requests, assembly, quality review, human approval, dry-run publishing, and analytics.

The lab scenario uses synthetic data and safe defaults. External publishing remains disabled or in dry-run/private mode unless a trainer authorises a controlled demonstration.

## Learning outcomes

By the end of the course, learners can:

1. Develop editing strategies and work plans that translate creative intent into a controlled agentic video-production contract.
2. Assess AI-generated and edited footage against storytelling, technical, brand, provenance, and platform-compliance evidence.
3. Develop remedial actions, approval controls, and n8n automations that support safe adoption of emerging video technologies.

## Topics covered

### 1. Creative strategy and end-to-end production

- Production contracts, finish conditions, run state, and idempotency
- Evidence research, source scoring, claim provenance, and bounded prompts
- Timed scripts, storyboards, shot grammar, continuity, routing, cost, and latency controls
- Coordinator, specialist-agent, deterministic-validator, and human-owner boundaries

### 2. AI-assisted editing, storytelling, and quality assurance

- Generative video, image-to-video, avatar, voice, music, and caption contracts
- Asset manifests, rights status, checksums, and immutable versions
- FFmpeg assembly, WebVTT captions, brand overlays, and ffprobe technical checks
- Narrative QA, timecoded repair, and payload-hash human approval

### 3. Workflow optimisation, compliance, and publishing

- n8n triggers, expressions, sub-workflows, retries, timeouts, and secret isolation
- SocialPost multipart upload contract and YouTube private-release controls
- Synthetic-media disclosure, rights, privacy, observability, and publication reconciliation
- Retention analysis, controlled experiments, and human `HOLD`, `ITERATE`, or `SCALE` decisions

## Labs

Complete the labs in order. Every folder contains a detailed README, an importable `workflow.json`, a styled synthetic `mock-data.xlsx`, an instruction-and-prompts PDF, starter notes, expected output, and an evidence checklist.

1. [Create the Video Production Contract and Research Backlog](labs/lab-01-production-contract-and-research-backlog/README.md)
2. [Run Evidence Research and Build the Claim Register](labs/lab-02-evidence-research-and-claim-register/README.md)
3. [Generate the Script, Storyboard and Video Prompts](labs/lab-03-research-to-script-storyboard/README.md)
4. [Build the Generative Video, Voice and Music Asset Pack](labs/lab-04-generative-asset-request-pack/README.md)
5. [Assemble and Probe the Captioned Vertical Video](labs/lab-05-assemble-captioned-vertical-video/README.md)
6. [Run Quality Review and Human-in-the-Loop Approval](labs/lab-06-quality-review-and-human-approval/README.md)
7. [Orchestrate the End-to-End SocialPost and YouTube Release](labs/lab-07-end-to-end-socialpost-youtube-release/README.md)
8. [Analyse Performance and Build the Scaling Control Plan](labs/lab-08-analytics-feedback-and-scaling-control/README.md)

The connected path is:

```text
contract → research → script/storyboard → generative assets → assembly
         → QA and human approval → SocialPost/YouTube dry-run → analytics
```

## Public package

- [Learner Guide in Markdown](LG-Agentic%20AI%20for%20Video%20Creation.md)
- [Eight self-contained lab folders](labs/)
- Sanitised n8n workflow exports with no live credential values
- Synthetic Excel data, bounded prompt PDFs, solution structures, and evidence checklists

The editable slide deck, rendered course documents, and learner assessment papers are distributed through the authorised course Drive/LMS channels.

## Distribution boundary

This public repository intentionally excludes:

- assessment answer keys and marking guides;
- `.env` files, credentials, tokens, or private connection details;
- source/reference material with restricted distribution;
- build tooling, QA renders, archives, and trainer-private resources.

Do not add live API keys to n8n JSON, prompts, workbooks, screenshots, issues, or pull requests. Configure approved credentials inside the target n8n environment.

## Provider

Developed by **Tertiary Infotech Academy Pte Ltd** (UEN `201200696W`).

- [Course registration and current funding information](https://www.tertiarycourses.com.sg/wsq-agentic-ai-for-video-creation.html)
- [SocialPost platform](https://socialmediapost.tertiaryinfotech.com/)
