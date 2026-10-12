# Project Status and Next Steps

**Project:** Machine Learning-Based Content Refresh Prioritization Using Search Performance Analytics  
**Owner:** Mukesh Burdak  
**Last updated:** 2026-10-12

## Current repository state

- The starter repository and assignment notebook skeletons are present.
- `work/README.md` is the guide for the workspace and remains the source of truth for assignment paths and data-use rules.
- The capstone report scaffold has been created at `work/capstone_report.md`.
- ML-02 is already completed and committed; continue from ML-03. The notebook includes exploratory numbers, which should be treated as descriptive observations rather than evidence that a refresh will cause recovery.
- No model metrics or completed experiment results are claimed in this status file.

## Work sequence

- [x] Complete ML-02: define the research question and decision. Verified in `work/notebooks/w01_research_question.ipynb`; notebook includes executed data checks and was committed on 2026-07-26.
- [ ] Review and complete ML-03: notebook revised to distinguish the retrospective decline proxy from a true ranking/refresh-benefit target; rerun the revised diagnostic cells and review before marking complete.
- [ ] Review and complete ML-04: data-contract notebook revised to use the approved local anonymized sample, verify actual schema/grain, and flag target/time-window leakage; run it in an approved environment and review checks before marking complete.
- [ ] Complete ML-07: build and evaluate a transparent baseline.
- [ ] Complete ML-08: train a suitable model only if the target and data support it.
- [ ] Complete ML-09: audit the validation design and errors.
- [ ] Complete ML-10: turn measured results into a human action playbook.
- [ ] Complete ML-11/ML-12: capstone paper, demo outline, social post, and employer-facing summary.
- [ ] Commit reproducible metrics JSON files under `work/outputs/`.
- [ ] Deploy the paper and add its exact URL to `submission/paper_url.txt`.

Optional stretch notebooks ML-05 and ML-06 are optional according to `work/README.md`.

## Repository rules

1. Do not edit the shared reference pipeline in `scripts/`; put project-specific copies/changes in `work/scripts/`.
2. Do not commit datasets or private/client-identifying information.
3. Commit generated metrics JSON files and document seeds/splits.
4. Keep all public claims evidence-based; do not claim causation or prediction of Google's algorithm.
5. Do not copy example metrics from the starter README as if they were this project's results.
