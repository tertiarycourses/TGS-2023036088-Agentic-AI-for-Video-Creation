# Evidence Checklist - Lab 07

- [ ] Imported `workflow.json` without embedding credentials.
- [ ] Preserved the original `data/mock-data.xlsx` and used synthetic values only.
- [ ] Captured a successful execution with all named nodes visible.
- [ ] Captured the blocked/failure-path test and the gate did not leak through.
- [ ] Confirmed: The n8n run reaches DRY_RUN_ACCEPTED once, records the SocialPost payload, blocks the duplicate key, and does not expose a credential or publish publicly.
- [ ] Stored final output or preview: end-to-end-workflow.json, publishing-queue.xlsx and socialpost-request-preview.json
- [ ] Recorded reviewer/owner and run ID.
