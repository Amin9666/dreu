# Week 5

**Dates:** 07-13 to 07-17

## Goals

- Connect the evaluator to a local model runtime without installing the model into the main Python environment.
- Test the new setup on sample cases and confirm that the workflow can run end to end.
- Prepare the project for larger-scale guarded-agent experiments.

## Approach and Implementation

I set up an isolated Ollama runtime using Docker so the model could run outside the project’s Python environment. I then extended the evaluator to support an optional Ollama-backed path while preserving the original heuristic fallback. After the runtime was available, I ran the evaluator against a small set of cases using a local model endpoint and confirmed that the full workflow could produce outputs and save results to disk.

## Results

- Added optional support for real model-generated responses through Ollama.
- Verified the end-to-end flow using a local containerized model runtime.
- Produced successful evaluator outputs for sample cases using the new model-backed path.
- Established a cleaner experimental setup for future guarded-agent comparisons.

## Notes

- The next step is to expand the evaluation set, compare model-backed responses against the heuristic baseline, and begin summarizing the results for the research write-up.


