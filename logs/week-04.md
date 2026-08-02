# Week 4

**Dates:** 07-06 to 07-10

## Goals

- Build the first guarded-agent evaluation scaffold for the ESA telemetry triage workflow.
- Create a repeatable way to score evidence citation, uncertainty, and unsupported-claim behavior.
- Verify the evaluator on sample adversarial cases before moving to larger experiments.

## Approach and Implementation

I implemented a lightweight evaluation script that loads the prepared evidence packets and adversarial cases, builds a prompt for the agent, and scores the resulting response. I also added a small regression test suite to verify that the prompt construction and scoring logic behave correctly. The evaluator was run on a small batch of cases and used the prepared telemetry evidence as the source of truth for judging safe behavior.

## Results

- Added a working evaluation scaffold for guarded-agent outputs.
- Verified the prompt and scoring logic with automated tests.
- Produced an initial JSON results artifact from sample adversarial cases for downstream analysis.
- Clarified that the project can now move from data preparation to actual experiment execution.

## Notes

- The next step is to connect the evaluator to a real local model so responses can be compared against the heuristic baseline.


