# Lab 07 - Orchestrate the End-to-End SocialPost and YouTube Release

**Course:** Agentic AI for Video Creation (`TGS-2023036088`)
**Topic:** 3
**Goal:** Connect the approved production stages into an n8n parent workflow and prepare an idempotent SocialPost YouTube upload.
**Deliverable:** end-to-end-workflow.json, publishing-queue.xlsx and socialpost-request-preview.json

## Workflow mechanism

`Manual Trigger -> Research Sub-workflow -> Content Sub-workflow -> QA and Approval Gate -> Build SocialPost Payload -> Dry-Run Publication Log`

## Files in this folder

- `workflow.json` - importable n8n workflow; safe defaults and no credentials.
- `data/mock-data.xlsx` - styled synthetic inputs and validation contract.
- `prompts/Lab-07-Instructions-and-Prompts.pdf` - the instruction PDF and copy-ready bounded prompt.
- `starter/notes.md` - learner notes and run identifiers.
- `solution/expected-output.json` - structure of an acceptable checkpoint.
- `evidence/checklist.md` - evidence to retain before moving on.

## Detailed procedure

1. Open `data/mock-data.xlsx`; review the Mock Data and Validation sheets. Keep all values synthetic.
2. In n8n, create a workflow and use the top-right workflow menu to import `workflow.json` from this folder.
3. Open the Lab Contract sticky note and compare the required input, output and acceptance criterion with the workbook.
4. Open each node from left to right. Confirm that expressions read from item JSON and no live credential or secret is embedded.
5. Open `prompts/Lab-07-Instructions-and-Prompts.pdf` and paste the bounded prompt into the designated AI/tool adapter node when instructed.
6. Execute the workflow manually. Inspect each node's input/output data and save a screenshot of the final dry-run or checkpoint state under `evidence/output/`.
7. Open https://socialmediapost.tertiaryinfotech.com/ in a browser to understand the upload contract. Keep `Live SocialPost Upload (Disabled)` disabled; use the generated request preview for learner evidence.
8. Test one failure condition by removing a required field or setting a status to BLOCKED; verify that the workflow does not cross its gate.
9. Restore the approved row, rerun, and complete `evidence/checklist.md`. Keep external publishing disabled unless the trainer explicitly authorizes a private demonstration.

## Prompt contract

> Act as a release-orchestration controller. Continue only when QA status is PASS and approval_hash matches the current payload. Build a multipart SocialPost request for POST /api/upload with Authorization: Apikey <CREDENTIAL>, video, title, user and platform[]=youtube. Keep dry_run true for learner execution and never embed credentials.

## Acceptance check

The n8n run reaches DRY_RUN_ACCEPTED once, records the SocialPost payload, blocks the duplicate key, and does not expose a credential or publish publicly.

## Troubleshooting

- **Import reports an unknown credential:** delete the credential reference and create an approved n8n credential; never paste a key into a node field captured in screenshots.
- **A node returns no items:** inspect the prior node's JSON keys and compare them with the expression; field names are case-sensitive.
- **The workflow reaches a release node after a failed check:** disable the release node, restore an explicit PASS/APPROVED condition, and rerun the blocked test.
- **A retry creates a duplicate:** compare the idempotency key and external/result ledger before any second side effect.

## Safety boundary

Use only synthetic or authorized content. External publishing is consequential: a named human must approve the exact hashed payload. Learner workflows remain dry-run/private unless the trainer authorizes a controlled demonstration.
