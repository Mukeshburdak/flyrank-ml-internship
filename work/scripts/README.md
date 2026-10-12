# Project-specific scripts

Place scripts written or adapted for this project in this directory. Keep the shared reference pipeline under the repository-level `scripts/` unchanged.

For each script, document:
- its purpose and inputs/outputs;
- required environment/packages;
- random seed and split strategy, where applicable;
- how to run it from a fresh clone.

Never commit dataset CSVs or client-identifying information. Commit small metrics JSON outputs under `work/outputs/` so reported numbers can be traced to reproducible runs.
