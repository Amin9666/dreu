# Week 3

**Dates:** 06-29 to 07-03

## Goals

- Build an evaluation split and holdout anomaly case set for controlled experiments.
- Add a second baseline detector and compare it against the current z-distance baseline.
- Generate per-event JSON evidence packets for guarded-agent input.
- Create adversarial and poisoned-context test cases for guardrail evaluation.


## Approach and Implementation

I extended the ESA anomaly pipeline script to support all four milestone follow-on tasks in one reproducible run. First, I added deterministic event-level splitting with a fixed seed to assign anomaly events into train/dev/test/holdout partitions, then generated a dedicated holdout case table for controlled comparisons.

For baseline expansion, I integrated an Isolation Forest detector and computed summary metrics alongside the existing z-score baseline. I recorded both row-level and holdout event-level comparison metrics in the run summary.

I also added per-event JSON packet generation so each anomaly has a structured evidence object suitable for the guarded triage agent. Finally, I generated adversarial cases (clean controls, prompt-injection notes, and misleading retrieval scenarios) to support the guardrail comparison study.

After implementation, I reran the pipeline end-to-end and verified that all new artifact files were created and populated.


## Results

- Produced a reproducible split file covering all detected anomaly events with train/dev/test/holdout assignments.
- Generated a holdout case set for controlled experiments.
- Added and executed Isolation Forest as a second baseline; comparison metrics are now included in the summary artifact.
- Exported per-event JSON evidence packets for downstream guarded-agent experiments.
- Created adversarial/poisoned-context test cases for guardrail evaluation.
- Updated data documentation and manifest entries to reflect the new milestone artifacts.

This week transitioned the project from initial baseline generation to an experiment-ready setup with evaluation structure, comparative baselines, and safety-focused test inputs.


## Notes

- Next step is to build an evaluator that scores guarded-agent outputs on evidence citation quality, unsupported-claim rate, and refusal/escalation behavior across clean versus adversarial contexts.


