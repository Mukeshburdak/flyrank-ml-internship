# Machine Learning-Based Content Refresh Prioritization Using Search Performance Analytics

- **Author:** Mukesh Burdak
- **Lane:** Content refresh prioritization / applied search intelligence
- **Repo:** https://github.com/Mukeshburdak/flyrank-ml-internship
- **Date:** 2026-10-12
- **Status:** Initial scaffold — experiments and measured results are pending

> This report is intentionally a work-in-progress scaffold. It records the proposed question and safe workflow; it does not claim that model training, evaluation, or deployment has been completed. Update each section only after the corresponding work has been run and reviewed.

## 0. Abstract

**Pending.** Complete this section after the data audit, baseline, model comparison, and validation are finished. Summarize the research question, approved data slice, method, measured result, and intended human decision. Do not copy example metrics from the reference pipeline.

## 1. Problem framing

**Decision supported:** Help an editor prioritize which content items should be reviewed for a possible refresh.

**Unit of analysis:** One pseudonymized content item (confirm against the actual data contract before analysis).

**Intended output:** A ranked review queue with transparent reason codes, if the available fields support it.

**Human action:** An editor reviews the queue and decides whether an item merits further investigation. The score is decision support, not an instruction to change content automatically.

**Cost of a wrong call:** A useful item may receive unnecessary review, or an item needing attention may be missed. The review queue must therefore be checked by a person.

**Research question:** Can observed search-performance and freshness signals produce a reproducible, useful prioritization of content items for human review compared with a simple transparent baseline?

**Current status:** Proposed framing only; validate the target/proxy and available features in the data-contract and baseline notebooks before modeling.

## 2. Data safety

- Use only the approved anonymized sample or another explicitly approved release.
- Do not commit datasets or private/client-identifying information.
- Do not paste client data into third-party AI tools.
- Treat pseudonymous identifiers such as content/client IDs as grouping or join keys only, never as model features.
- Review label-derived fields such as `trend_direction` and `trend_pct` for leakage before feature selection.
- The available sample documentation indicates that raw queries, page titles, URLs, keywords, and query-document relevance labels are not included. Do not imply that this project evaluates query-document ranking without suitable labels.
- Public descriptions must use observed, measured, directional, or decision-support language. Do not make causal claims or claim to predict Google's algorithm.

**Current status:** Safety rules recorded; a column-by-column data contract and leakage review remain to be completed and documented.

## 3. Baseline

**Planned approach:** Establish a transparent rule-based score using only fields justified by the data contract. Compare it with any learned model on the same split and using the same metric.

**Pending:** Final feature definition, code, random seed, dataset/version details, baseline metrics, and base rate. Do not report numbers until the notebook or script has produced them and the metrics are committed under `work/outputs/`.

## 4. Model / analysis

**Planned approach:** After validating the task definition and leakage risks, compare an interpretable baseline with an appropriate supervised model only if the data supports a defensible target/proxy. Candidate models should be selected and documented in the modeling notebook rather than assumed in advance.

**Pending:** Target/proxy definition, exact feature list, exclusions, model configuration, and training results.

## 5. Evaluation

**Planned approach:** Choose a client-grouped or time-aware split based on the data structure and the intended use. Compare baseline and model on the same held-out data. Report the task base rate alongside Precision@K or accuracy where applicable, and include an error analysis.

**Pending:** Split design, seed, metrics, comparison table, and error analysis. No evaluation result is claimed at this stage.

## 6. Interpretation

**Pending.** Add only findings supported by reproducible outputs. Explain feature effects or model behavior in plain language, including surprising findings and negative results. Distinguish association from causation.

## 7. Recommendation

**Intended use:** A human-reviewed queue for deciding which content items to inspect first, if evaluation shows the score is useful.

**Limits:** The output is prioritization support, not a guarantee of future search performance and not a prediction of Google's ranking algorithm. Editors retain decision authority.

**Pending:** Ranked examples from approved data, reason codes, confidence/limitations, and an action playbook grounded in measured findings.

## 8. Reproducibility

Record the commands used, Python/package versions, random seeds, split method, data source/version, and exact feature list after the workflow is implemented.

- **Current status:** Starter repository and assignment notebooks are present; completed experiment outputs have not yet been recorded in this report.
- **Re-run instructions:** To be added after the pipeline is finalized.
- **Metrics artifacts:** Commit result JSON files under `work/outputs/`; do not commit dataset CSVs.
- **Reference code:** Keep the shared reference pipeline in `scripts/` unchanged. Put project-specific scripts under `work/scripts/`.

## 9. Acknowledgments & data credit

This project is part of the FlyRank ML Internship. The approved data source must be credited in the final paper as **Built on the FlyRank ML Internship dataset**, linking to https://flyrank.ai. Add any further acknowledgments only when verified.

---

## Claims checklist before submission

- [ ] All reported numbers match committed metrics and a fresh re-run.
- [ ] Baseline and model use the same evaluation split and metric.
- [ ] Base rate is reported alongside relevant metrics.
- [ ] Leakage checks and identifier exclusions are documented.
- [ ] No datasets or client-identifying details are committed.
- [ ] Statements are framed as observed/measured/directional/decision-support.
- [ ] No unsupported causal claims or claims about predicting Google's algorithm.
- [ ] Paper includes data credit and the deployed URL is recorded in `submission/paper_url.txt` once available.
