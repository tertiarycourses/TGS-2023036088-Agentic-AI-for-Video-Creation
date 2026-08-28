# Agentic AI for Video Creation
**Course Code:** TGS-2023036088
**Version:** v2.0
**TSC:** MED-MPN-4005-1.1 - Video Editing-4
## Learning outcomes
- LO1: Develop editing strategies and work plans that translate creative intent into a controlled agentic video-production contract.
- LO2: Assess AI-generated and edited footage against storytelling, technical, brand, provenance and platform-compliance evidence.
- LO3: Develop remedial actions, approval controls and n8n automations that support safe adoption of emerging video technologies.

## End-to-end architecture
1. Governed production contract and evidence backlog
2. Source scoring and immutable claim register
3. Timed script, storyboard and generative-media request pack
4. Assembly, captions and ffprobe technical QA
5. Timecoded review, repair and payload-hash approval
6. Dry-run SocialPost/YouTube release with idempotency
7. Performance feedback and human scale decision

## Topic 1: Creative Strategy and End-to-End Video Production with Agentic AI

LO1 - translate creative vision into a bounded, evidence-backed production plan

### Production contract schema

**Mechanism:** Brief intake → Normalize constraints → Assign owners → Freeze approval gates
**Fields:** run_id, audience, channel, approval_policy
**Measure:** contract completeness = required fields / 18
**Control:** Reject incomplete contracts and assign a named owner before any generator call.
**Evidence:** production-contract.json validates and status becomes READY.

### Creative objective to video specification

**Mechanism:** Business objective → Viewer action → Narrative promise → Measurable output
**Fields:** objective, primary_cta, duration_s, aspect_ratio
**Measure:** spec coverage = approved decisions / required decisions
**Control:** Translate objective into one observable action and one video constraint.
**Evidence:** specification.xlsx contains one owner and one acceptance threshold per decision.

### Audience-signal ingestion

**Mechanism:** Collect signals → Normalize taxonomy → Score relevance → Create insight queue
**Fields:** signal_id, source, segment, relevance_score
**Measure:** signal acceptance rate = accepted / reviewed
**Control:** Weight relevance, recency and evidence quality separately.
**Evidence:** audience-signals.xlsx retains source URL, score and reviewer decision.

### Source-evidence scoring

**Mechanism:** Discover source → Check authority → Check recency → Approve claim use
**Fields:** source_id, publisher, published_at, evidence_score
**Measure:** evidence score = authority x relevance x recency
**Control:** Block script generation when a factual claim lacks an approved source_id.
**Evidence:** source-register.xlsx maps every factual claim to a current URL.

### Research-agent retrieval loop

**Mechanism:** Form query → Retrieve candidates → Extract evidence → Stop or refine
**Fields:** query, top_k, citation, stop_reason
**Measure:** precision at k = relevant sources / retrieved sources
**Control:** Cap iterations and stop when evidence coverage reaches the contract threshold.
**Evidence:** research-result.json records queries, citations and stop_reason.

### Claim register and provenance

**Mechanism:** Draft claim → Attach evidence → Classify risk → Approve wording
**Fields:** claim_id, statement, source_id, risk_level
**Measure:** claim coverage = sourced claims / factual claims
**Control:** Use immutable claim_id values through script and caption transformations.
**Evidence:** claim-register.xlsx shows zero unsupported high-risk claims.

### B-R-I-E-F prompt contract

**Mechanism:** Background → Role → Inputs → Execution and format
**Fields:** authoritative_inputs, allowed_tools, constraints, finish_condition
**Measure:** schema validity = valid outputs / attempts
**Control:** Validate structured output before it reaches the next node.
**Evidence:** prompt-contract.pdf and parser evidence show all required keys.

### Shot grammar and camera constraints

**Mechanism:** Select shot purpose → Set framing → Specify motion → Declare continuity
**Fields:** shot_size, camera_motion, subject_action, continuity_token
**Measure:** usable-shot rate = accepted clips / generated clips
**Control:** One dominant action and one camera move per timed shot.
**Evidence:** shot-list.xlsx carries purpose, duration and continuity token.

### Timed storyboard model

**Mechanism:** Allocate hook → Sequence beats → Assign shots → Check total time
**Fields:** beat_id, start_s, end_s, visual_prompt
**Measure:** timeline variance = storyboard duration - target duration
**Control:** Derive end_s from narration pace and reserve transition headroom.
**Evidence:** storyboard.xlsx totals 30.0 seconds with no overlaps.

### Continuity bible

**Mechanism:** Lock identity → Lock palette → Lock environment → Track deviations
**Fields:** character_token, wardrobe, palette_hex, location_rules
**Measure:** continuity defect rate = mismatches / reviewed shots
**Control:** Use reference tokens and a deviation log reviewed before assembly.
**Evidence:** continuity-bible.json and contact sheet show approved invariants.

### Model and tool routing

**Mechanism:** Classify task → Match capability → Check policy → Choose fallback
**Fields:** task_type, model_id, max_cost, fallback_tool
**Measure:** routing success = accepted outputs / routed calls
**Control:** Route by required modality, rights position, cost and deterministic fallback.
**Evidence:** tool-registry.xlsx records capability, permission and fallback.

### Cost and latency budgets

**Mechanism:** Estimate calls → Reserve retries → Set ceiling → Record actuals
**Fields:** estimated_cost, max_retries, timeout_s, actual_cost
**Measure:** budget variance = actual - approved budget
**Control:** Enforce per-stage budgets and escalate instead of infinite retry.
**Evidence:** run-ledger.xlsx shows cost and latency within approved ceilings.

### Run state and idempotency

**Mechanism:** Create run key → Persist state → Check prior action → Commit once
**Fields:** run_id, stage, idempotency_key, status
**Measure:** duplicate rate = duplicate actions / action attempts
**Control:** Check idempotency_key before every costly or external side effect.
**Evidence:** run ledger shows one committed output per key.

### Orchestration boundaries

**Mechanism:** Coordinator → Specialist agent → Deterministic validator → Human owner
**Fields:** input_schema, tool_scope, handoff_status, owner
**Measure:** handoff pass rate = accepted handoffs / total handoffs
**Control:** Separate reasoning, deterministic validation and consequential approval.
**Evidence:** n8n sub-workflow graph shows explicit contracts at each boundary.

## Topic 2: AI-Assisted Video Editing, Storytelling and Quality Assurance

LO2 - assess generated and edited footage using observable storytelling and technical evidence

### Hook-beat-CTA script structure

**Mechanism:** Pattern interrupt → Problem evidence → Value beat → Viewer action
**Fields:** hook, beat_seconds, claim_ids, cta
**Measure:** retained message coverage = approved beats / planned beats
**Control:** Bind claims to claim_ids and keep the CTA proportional to the evidence.
**Evidence:** script.json contains timed beats and approved claim references.

### Text-to-video prompt contract

**Mechanism:** Describe subject → Declare action → Set camera → Add exclusions
**Fields:** subject, action, camera, negative_constraints
**Measure:** prompt yield = accepted clips / generation attempts
**Control:** Use one shot purpose, one action, and explicit must-not-change rules.
**Evidence:** generation-manifest.xlsx links prompt version to each returned clip.

### Image-to-video keyframe control

**Mechanism:** Approve keyframe → Define motion → Generate transition → Compare end frame
**Fields:** start_frame, end_frame, motion_strength, seed
**Measure:** keyframe drift = visual mismatch score
**Control:** Constrain motion strength and compare end frame against continuity invariants.
**Evidence:** keyframe-review.json records drift score and decision.

### Avatar and lip-sync contract

**Mechanism:** Approve likeness → Prepare phonemes → Render avatar → Inspect sync
**Fields:** avatar_id, consent_ref, audio_uri, sync_score
**Measure:** lip-sync pass rate = passed segments / reviewed segments
**Control:** Require consent_ref and route low sync scores to re-render or human edit.
**Evidence:** avatar-manifest.xlsx and review evidence show consent and sync results.

### Voiceover timing and SSML

**Mechanism:** Normalize script → Insert pauses → Synthesize voice → Measure duration
**Fields:** voice_id, rate, break_ms, duration_s
**Measure:** timing error = actual narration - target narration
**Control:** Tune rate and pauses against the timed storyboard before assembly.
**Evidence:** voiceover-report.json is within +/- 0.5 seconds per beat.

### Music, SFX and ducking

**Mechanism:** Set loudness target → Place cues → Apply sidechain → Measure mix
**Fields:** music_uri, duck_db, integrated_lufs, true_peak_db
**Measure:** speech intelligibility pass rate
**Control:** Use measured loudness and a narration-driven ducking envelope.
**Evidence:** audio-QA report shows target LUFS and peak thresholds.

### Asset manifest and checksums

**Mechanism:** Register asset → Record provenance → Compute checksum → Approve version
**Fields:** asset_id, uri, sha256, rights_status
**Measure:** manifest integrity = verified hashes / manifest rows
**Control:** Approval binds to the checksum, not the human-readable filename.
**Evidence:** asset-manifest.xlsx verifies all hashes and rights_status values.

### FFmpeg filtergraph assembly

**Mechanism:** Ingest media → Scale and pad → Overlay and mix → Encode master
**Fields:** filter_complex, video_codec, audio_codec, pix_fmt
**Measure:** render success = valid masters / render attempts
**Control:** Normalize scale, fps, sample rate and timestamps before concat.
**Evidence:** ffprobe.json confirms H.264/AAC MP4 and intended dimensions.

### WebVTT captions and safe area

**Mechanism:** Tokenize narration → Create cues → Check timing → Burn or attach
**Fields:** cue_id, start, end, text
**Measure:** caption coverage = captioned speech / narration duration
**Control:** Use safe-area guides and cue timing checks before final encode.
**Evidence:** captions.vtt passes chronology and reading-speed checks.

### Brand overlay package

**Mechanism:** Load brand tokens → Place lockup → Apply color → Inspect contrast
**Fields:** logo_uri, safe_margin_px, brand_hex, min_contrast
**Measure:** brand compliance = passed checks / applicable checks
**Control:** Use safe margins, contrast tests and one approved overlay template.
**Evidence:** frame samples show correct placement and contrast evidence.

### Technical QC probe

**Mechanism:** Probe container → Inspect streams → Check duration → Gate release
**Fields:** width, height, avg_frame_rate, sample_rate
**Measure:** technical pass rate = passed checks / total checks
**Control:** Automate ffprobe checks and fail closed on missing streams or bounds.
**Evidence:** technical-qc.json contains observed values and pass/fail rules.

### Narrative QA rubric

**Mechanism:** Evaluate hook → Trace claims → Score coherence → Review CTA
**Fields:** criterion, score, finding, severity
**Measure:** weighted QA score = sum(score x weight)
**Control:** Use a weighted rubric and record evidence at timecodes.
**Evidence:** review-rubric.xlsx contains timecoded findings and owner decisions.

### Human approval with payload hash

**Mechanism:** Freeze payload → Compute hash → Request decision → Verify before release
**Fields:** approval_id, payload_hash, reviewer, decision
**Measure:** approval integrity = decision hash == current hash
**Control:** Recompute the hash immediately before the publish branch.
**Evidence:** approval-ledger.xlsx proves reviewer, time, hash and decision.

### Repair loop and versioned evidence

**Mechanism:** Open finding → Assign repair → Render new version → Close with evidence
**Fields:** finding_id, severity, asset_version, resolution
**Measure:** repair effectiveness = closed findings / reopened findings
**Control:** Write immutable versions and re-run the complete affected check set.
**Evidence:** repair-log.xlsx links finding, change, new hash and re-test result.

## Topic 3: Workflow Optimisation, Industry Compliance and Emerging Video Technologies

LO3 - implement resilient automation, publishing controls and evidence-led remediation

### n8n trigger and webhook boundary

**Mechanism:** Receive event → Authenticate → Normalize payload → Start run
**Fields:** http_method, path, auth_mode, response_code
**Measure:** valid trigger rate = accepted requests / received requests
**Control:** Authenticate, validate schema and deduplicate before work begins.
**Evidence:** execution log records accepted and rejected trigger evidence.

### Node contracts and expressions

**Mechanism:** Read item JSON → Transform fields → Validate output → Hand off
**Fields:** $json, expression, required_keys, status
**Measure:** node contract pass rate
**Control:** Use explicit Code/Set validation and fail with a named error code.
**Evidence:** workflow execution data shows stable keys between nodes.

### Sub-workflow orchestration

**Mechanism:** Parent dispatch → Child execute → Return status → Commit checkpoint
**Fields:** workflow_id, input, result, checkpoint_uri
**Measure:** stage success rate = successful stages / attempted stages
**Control:** Branch only on explicit SUCCESS and persist checkpoint evidence.
**Evidence:** orchestrator ledger shows one status per stage.

### Retry, timeout and backoff

**Mechanism:** Classify failure → Check retryability → Wait with backoff → Escalate
**Fields:** error_code, retryable, attempt, next_retry_at
**Measure:** recovery rate = successful retries / retry attempts
**Control:** Retry only transient classes with capped exponential backoff.
**Evidence:** error ledger distinguishes recovered, dead-letter and escalated runs.

### Credential and secret isolation

**Mechanism:** Reference credential → Call service → Redact logs → Rotate key
**Fields:** credential_name, scope, secret_ref, rotation_due
**Measure:** secret exposure count = 0
**Control:** Use n8n credentials and template placeholders; never embed live values.
**Evidence:** repository scan finds no tokens, passwords or private keys.

### SocialPost upload contract

**Mechanism:** Validate approved master → Build multipart body → POST /api/upload → Store platform results
**Fields:** video, title, user, platform[]
**Measure:** publish acceptance = successful platform results / requested platforms
**Control:** Require approval_id, explicit user, platform allow-list and dry_run by default.
**Evidence:** socialpost-request.json and response preview match the approved release package.

### SocialPost platform gateway

**Mechanism:** One approved upload → Adapt per channel → Queue and retry → Return analytics
**Fields:** Authorization, Apikey, schedule_at, platform_result
**Measure:** gateway success rate and partial-failure rate
**Control:** Evaluate each platform result independently and route failures to review.
**Evidence:** publication-log.xlsx records per-platform status and external id.

### YouTube metadata and synthetic disclosure

**Mechanism:** Set snippet → Set status → Upload media → Poll processing
**Fields:** snippet.title, status.privacyStatus, status.containsSyntheticMedia, video_id
**Measure:** metadata completeness and processing success
**Control:** Default to private, require approval for visibility, and set applicable disclosure fields.
**Evidence:** YouTube release payload contains approved title, privacy and disclosure status.

### Publishing idempotency

**Mechanism:** Create publish key → Check prior result → Attempt upload → Commit external id
**Fields:** idempotency_key, channel, external_id, published_at
**Measure:** duplicate publish rate = 0
**Control:** Reconcile by key or external id before a second upload.
**Evidence:** publication ledger contains one external_id per key.

### Rights, privacy and compliance gate

**Mechanism:** Verify source rights → Check personal data → Review disclosures → Approve channel use
**Fields:** rights_ref, consent_ref, synthetic_media, retention_class
**Measure:** compliance pass rate and unresolved high-risk count
**Control:** Fail closed until rights, consent, disclosure and retention are documented.
**Evidence:** compliance checklist shows zero unresolved high-risk findings.

### Observability and run ledger

**Mechanism:** Emit event → Correlate run → Measure stage → Alert owner
**Fields:** run_id, stage, duration_ms, error_code
**Measure:** success rate, p95 latency and cost per released video
**Control:** Use stable run_id and structured event fields at every boundary.
**Evidence:** run-ledger.xlsx supports stage-level filtering and evidence lookup.

### Performance event ingestion

**Mechanism:** Collect platform metrics → Normalize dimensions → Join to creative → Validate window
**Fields:** video_id, event_date, impressions, watch_time_s
**Measure:** data freshness and join coverage
**Control:** Store reporting window, timezone and source with every metric row.
**Evidence:** performance-events.xlsx has complete video_id and date keys.

### Retention and engagement analysis

**Mechanism:** Build retention curve → Locate drop-off → Relate to beat → Prioritize repair
**Fields:** second, retention_pct, beat_id, hypothesis
**Measure:** 3-second hold, average percentage viewed, CTA rate
**Control:** Tie retention changes to storyboard beats and a testable edit hypothesis.
**Evidence:** analytics chart and next-test record identify one prioritized change.

### Experiment and scaling control

**Mechanism:** Select hypothesis → Define variant → Set guardrail → Decide scale
**Fields:** experiment_id, primary_metric, guardrail, decision
**Measure:** lift with minimum sample and guardrail pass
**Control:** Require minimum evidence, guardrails and a named human scale decision.
**Evidence:** scaling-scorecard.xlsx records HOLD, ITERATE or SCALE with rationale.

## Labs

### Lab 01: Create the Video Production Contract and Research Backlog

Turn the Harbour Bean brief into a governed production contract, claim-risk register and research queue.

- Folder: `labs/lab-01-production-contract-and-research-backlog/`
- Nodes: Manual Trigger, Load Brief, Validate Contract, Score Claim Risk, Create Research Backlog, Write Checkpoint
- Acceptance: READY is emitted only when all 18 production-contract fields are present and every high-risk claim has a research owner.

### Lab 02: Run Evidence Research and Build the Claim Register

Score sources, extract bounded evidence and approve only claims that can be traced to a retrievable source.

- Folder: `labs/lab-02-evidence-research-and-claim-register/`
- Nodes: Manual Trigger, Research Queue, HTTP Research Adapter, Score Evidence, Claim Coverage Gate, Save Register
- Acceptance: Every factual script claim has an approved source_id; evidence score is at least 0.65; rejected sources remain visible.

### Lab 03: Generate the Script, Storyboard and Video Prompts

Transform approved claims into a timed 30-second script, storyboard and shot-level generative-video prompts.

- Folder: `labs/lab-03-research-to-script-storyboard/`
- Nodes: Manual Trigger, Approved Claims, Script Agent, Storyboard Parser, Duration Validator, Human Storyboard Review
- Acceptance: The storyboard totals 30.0 seconds, no beat overlaps, factual narration cites approved claims, and a named reviewer approves the storyboard.

### Lab 04: Build the Generative Video, Voice and Music Asset Pack

Create structured, rights-aware requests for video shots, voiceover, music and captions while preserving continuity.

- Folder: `labs/lab-04-generative-asset-request-pack/`
- Nodes: Manual Trigger, Approved Storyboard, Create Shot Requests, Create Voice Request, Create Music Brief, Asset Manifest Gate
- Acceptance: Every storyboard beat has a registered asset or fallback, rights_status is not UNKNOWN, and total requested duration covers the timeline.

### Lab 05: Assemble and Probe the Captioned Vertical Video

Assemble approved or placeholder media with FFmpeg and generate machine-readable technical evidence.

- Folder: `labs/lab-05-assemble-captioned-vertical-video/`
- Nodes: Manual Trigger, Approved Asset Manifest, Build FFmpeg Plan, Run Assembly Adapter, FFprobe Master, Technical Gate
- Acceptance: ffprobe reports one H.264 video stream, one AAC audio stream, 1080x1920, 30 fps and duration from 29.5 to 30.5 seconds.

### Lab 06: Run Quality Review and Human-in-the-Loop Approval

Evaluate technical, narrative, brand and compliance evidence, repair one finding and bind approval to the final payload hash.

- Folder: `labs/lab-06-quality-review-and-human-approval/`
- Nodes: Manual Trigger, QA Evidence, Score Review, Create Approval Hash, Wait for Human Decision, Verify Hash and Route
- Acceptance: No high-severity finding remains open; reviewer, timestamp, decision and payload_hash are recorded; the hash is rechecked immediately before release.

### Lab 07: Orchestrate the End-to-End SocialPost and YouTube Release

Connect the approved production stages into an n8n parent workflow and prepare an idempotent SocialPost YouTube upload.

- Folder: `labs/lab-07-end-to-end-socialpost-youtube-release/`
- Nodes: Manual Trigger, Research Sub-workflow, Content Sub-workflow, QA and Approval Gate, Build SocialPost Payload, Dry-Run Publication Log
- Acceptance: The n8n run reaches DRY_RUN_ACCEPTED once, records the SocialPost payload, blocks the duplicate key, and does not expose a credential or publish publicly.

### Lab 08: Analyse Performance and Build the Scaling Control Plan

Join synthetic platform performance to storyboard beats, identify one repair hypothesis and make a controlled scale decision.

- Folder: `labs/lab-08-analytics-feedback-and-scaling-control/`
- Nodes: Manual Trigger, Performance Events, Normalize Metrics, Join Storyboard Beats, Score Experiment, Human Scale Decision
- Acceptance: Metrics reconcile to source rows, the hypothesis names one beat and one change, and a human owner records the final HOLD/ITERATE/SCALE decision.

## References
- [Official course page](https://www.tertiarycourses.com.sg/wsq-agentic-ai-for-video-creation.html) — Course identity, duration, outcomes and TSC
- [n8n workflow export and import](https://docs.n8n.io/build/manage-workflows/export-and-import) — Workflow JSON portability and credential-sharing warning
- [n8n Wait node](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.wait/) — Webhook-resumed human approval
- [SocialPost](https://socialmediapost.tertiaryinfotech.com/) — Multipart POST /api/upload contract and supported platform gateway
- [YouTube videos.insert](https://developers.google.com/youtube/v3/docs/videos/insert) — Upload metadata, OAuth and status fields
- AI Video Prompting: reference/AI Video Prompting.pdf — Shot grammar, camera movement and continuity prompt patterns
