# Lab 05 - Assemble and Probe the Captioned Vertical Video

**Course:** Agentic AI for Video Creation (`TGS-2023036088`)
**Topic:** 2
**Goal:** Assemble approved or placeholder media with FFmpeg and generate machine-readable technical evidence.
**Deliverable:** vertical-master-v1.mp4, captions.vtt, edit-decision-list.xlsx and ffprobe.json

## Workflow mechanism

`Manual Trigger -> Approved Asset Manifest -> Build FFmpeg Plan -> Run Assembly Adapter -> FFprobe Master -> Technical Gate`

## Files in this folder

- `workflow.json` - importable n8n workflow; safe defaults and no credentials.
- `data/mock-data.xlsx` - styled synthetic inputs and validation contract.
- `prompts/Lab-05-Instructions-and-Prompts.pdf` - the instruction PDF and copy-ready bounded prompt.
- `starter/notes.md` - learner notes and run identifiers.
- `solution/expected-output.json` - structure of an acceptable checkpoint.
- `evidence/checklist.md` - evidence to retain before moving on.

## Detailed procedure

1. Open `data/mock-data.xlsx`; review the Mock Data and Validation sheets. Keep all values synthetic.
2. In n8n, create a workflow and use the top-right workflow menu to import `workflow.json` from this folder.
3. Open the Lab Contract sticky note and compare the required input, output and acceptance criterion with the workbook.
4. Open each node from left to right. Confirm that expressions read from item JSON and no live credential or secret is embedded.
5. Open `prompts/Lab-05-Instructions-and-Prompts.pdf` and paste the bounded prompt into the designated AI/tool adapter node when instructed.
6. Execute the workflow manually. Inspect each node's input/output data and save a screenshot of the final dry-run or checkpoint state under `evidence/output/`.
7. Test one failure condition by removing a required field or setting a status to BLOCKED; verify that the workflow does not cross its gate.
8. Restore the approved row, rerun, and complete `evidence/checklist.md`. Keep external publishing disabled unless the trainer explicitly authorizes a private demonstration.

## Prompt contract

> Act as a render-plan validator. Inspect the edit decision rows and return a deterministic FFmpeg plan. Require 1080x1920, 30 fps, H.264 video, AAC audio, yuv420p and exactly 30 seconds. Return BLOCKED for gaps, overlaps or unapproved assets.

## Acceptance check

ffprobe reports one H.264 video stream, one AAC audio stream, 1080x1920, 30 fps and duration from 29.5 to 30.5 seconds.

## Troubleshooting

- **Import reports an unknown credential:** delete the credential reference and create an approved n8n credential; never paste a key into a node field captured in screenshots.
- **A node returns no items:** inspect the prior node's JSON keys and compare them with the expression; field names are case-sensitive.
- **The workflow reaches a release node after a failed check:** disable the release node, restore an explicit PASS/APPROVED condition, and rerun the blocked test.
- **A retry creates a duplicate:** compare the idempotency key and external/result ledger before any second side effect.

## Safety boundary

Use only synthetic or authorized content. External publishing is consequential: a named human must approve the exact hashed payload. Learner workflows remain dry-run/private unless the trainer authorizes a controlled demonstration.
