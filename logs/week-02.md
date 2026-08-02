# Week 2

**Dates:** 06-22 to 06-26

## Goals

- Investigate candidate public telemetry anomaly datasets.
- Compare dataset fit for the planned pipeline.
- Recommend one primary dataset and key risks.

## Approach and Implementation

Week 2 centered on dataset inquiry guided by the initial plan. I reviewed candidate public telemetry datasets, with the ESA Anomaly Dataset as the primary option called out in the proposal.

I compared candidates against practical requirements for the proposed workflow: channel availability, anomaly labeling quality, format consistency, and whether the data can support baseline anomaly detection plus evidence packet generation.

I documented tradeoffs such as preprocessing effort, potential missing metadata, and how reliably each dataset supports anomaly categorization and explanation tasks. I then prepared a recommendation for advisor review.

## Results

- Completed a structured survey of candidate telemetry anomaly datasets.
- Identified the ESA Anomaly Dataset as the strongest initial fit for the first milestone.
- Recorded open questions about data cleanliness, label granularity, and preprocessing effort before full pipeline implementation.

The dataset inquiry established a concrete data direction and reduced uncertainty for upcoming baseline modeling and evidence-extraction work.

## Notes

- Next step is to finalize the primary dataset and begin the baseline anomaly-detection preprocessing workflow.


