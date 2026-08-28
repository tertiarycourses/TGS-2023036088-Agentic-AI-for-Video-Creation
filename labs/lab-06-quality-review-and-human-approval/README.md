# Lab 06 - Run Quality Review and Human-in-the-Loop Approval

**Course:** Agentic AI for Video Creation (`TGS-2023036088`)
**Topic:** 2
**Goal:** Evaluate technical, narrative, brand and compliance evidence, repair one finding and bind approval to the final payload hash.
**Deliverable:** review-register.xlsx, repair-log.json and approval-ledger.json

## Workflow mechanism

`Manual Trigger -> QA Evidence -> Score Review -> Create Approval Hash -> Wait for Human Decision -> Verify Hash and Route`

## Files in this folder

- `workflow.json` - importable n8n workflow; safe defaults and no credentials.
- `data/mock-data.xlsx` - styled synthetic inputs and validation contract.
- `prompts/Lab-06-Instructions-and-Prompts.pdf` - the instruction PDF and copy-ready bounded prompt.
- `starter/notes.md` - learner notes and run identifiers.
- `solution/expected-output.json` - structure of an acceptable checkpoint.
- `evidence/checklist.md` - evidence to retain before moving on.

## Detailed procedure

1. Open `data/mock-data.xlsx`; review the Mock Data and Validation sheets. Keep all values synthetic.
2. In n8n, create a workflow and use the top-right workflow menu to import `workflow.json` from this folder.
3. Open the Lab Contract sticky note and compare the required input, output and acceptance criterion with the workbook.
4. Open each node from left to right. Confirm that expressions read from item JSON and no live credential or secret is embedded.
5. Open `prompts/Lab-06-Instructions-and-Prompts.pdf` and paste the bounded prompt into the designated AI/tool adapter node when instructed.
6. Execute the workflow manually. Inspect each node's input/output data and save a screenshot of the final dry-run or checkpoint state under `evidence/output/`.
7. At the Wait node, copy the test resume URL, submit a reviewer decision with reviewer name and payload_hash, then verify that a changed payload is rejected.
8. Test one failure condition by removing a required field or setting a status to BLOCKED; verify that the workflow does not cross its gate.
9. Restore the approved row, rerun, and complete `evidence/checklist.md`. Keep external publishing disabled unless the trainer explicitly authorizes a private demonstration.

## Prompt contract

> Act as an independent video reviewer. Return timecoded findings for storytelling, technical compliance, captions, brand, rights and disclosure. Do not approve. After repairs, create an approval request with payload_hash and require a named human decision of APPROVE, REVISE or REJECT.

## Acceptance check

No high-severity finding remains open; reviewer, timestamp, decision and payload_hash are recorded; the hash is rechecked immediately before release.

## Troubleshooting

- **Import reports an unknown credential:** delete the credential reference and create an approved n8n credential; never paste a key into a node field captured in screenshots.
- **A node returns no items:** inspect the prior node's JSON keys and compare them with the expression; field names are case-sensitive.
- **The workflow reaches a release node after a failed check:** disable the release node, restore an explicit PASS/APPROVED condition, and rerun the blocked test.
- **A retry creates a duplicate:** compare the idempotency key and external/result ledger before any second side effect.

## Safety boundary

Use only synthetic or authorized content. External publishing is consequential: a named human must approve the exact hashed payload. Learner workflows remain dry-run/private unless the trainer authorizes a controlled demonstration.
