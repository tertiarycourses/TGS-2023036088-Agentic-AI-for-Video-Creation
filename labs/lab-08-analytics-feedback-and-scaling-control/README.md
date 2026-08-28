# Lab 08 - Analyse Performance and Build the Scaling Control Plan

**Course:** Agentic AI for Video Creation (`TGS-2023036088`)
**Topic:** 3
**Goal:** Join synthetic platform performance to storyboard beats, identify one repair hypothesis and make a controlled scale decision.
**Deliverable:** performance-analysis.xlsx, next-test.json and scaling-scorecard.xlsx

## Workflow mechanism

`Manual Trigger -> Performance Events -> Normalize Metrics -> Join Storyboard Beats -> Score Experiment -> Human Scale Decision`

## Files in this folder

- `workflow.json` - importable n8n workflow; safe defaults and no credentials.
- `data/mock-data.xlsx` - styled synthetic inputs and validation contract.
- `prompts/Lab-08-Instructions-and-Prompts.pdf` - the instruction PDF and copy-ready bounded prompt.
- `starter/notes.md` - learner notes and run identifiers.
- `solution/expected-output.json` - structure of an acceptable checkpoint.
- `evidence/checklist.md` - evidence to retain before moving on.

## Detailed procedure

1. Open `data/mock-data.xlsx`; review the Mock Data and Validation sheets. Keep all values synthetic.
2. In n8n, create a workflow and use the top-right workflow menu to import `workflow.json` from this folder.
3. Open the Lab Contract sticky note and compare the required input, output and acceptance criterion with the workbook.
4. Open each node from left to right. Confirm that expressions read from item JSON and no live credential or secret is embedded.
5. Open `prompts/Lab-08-Instructions-and-Prompts.pdf` and paste the bounded prompt into the designated AI/tool adapter node when instructed.
6. Execute the workflow manually. Inspect each node's input/output data and save a screenshot of the final dry-run or checkpoint state under `evidence/output/`.
7. Test one failure condition by removing a required field or setting a status to BLOCKED; verify that the workflow does not cross its gate.
8. Restore the approved row, rerun, and complete `evidence/checklist.md`. Keep external publishing disabled unless the trainer explicitly authorizes a private demonstration.

## Prompt contract

> Act as a video performance analyst. Calculate 3-second hold, average percentage viewed and CTA rate from supplied synthetic rows. Link the largest retention drop to a storyboard beat, propose one testable edit, define a guardrail and recommend HOLD, ITERATE or SCALE. Do not claim causality.

## Acceptance check

Metrics reconcile to source rows, the hypothesis names one beat and one change, and a human owner records the final HOLD/ITERATE/SCALE decision.

## Troubleshooting

- **Import reports an unknown credential:** delete the credential reference and create an approved n8n credential; never paste a key into a node field captured in screenshots.
- **A node returns no items:** inspect the prior node's JSON keys and compare them with the expression; field names are case-sensitive.
- **The workflow reaches a release node after a failed check:** disable the release node, restore an explicit PASS/APPROVED condition, and rerun the blocked test.
- **A retry creates a duplicate:** compare the idempotency key and external/result ledger before any second side effect.

## Safety boundary

Use only synthetic or authorized content. External publishing is consequential: a named human must approve the exact hashed payload. Learner workflows remain dry-run/private unless the trainer authorizes a controlled demonstration.
