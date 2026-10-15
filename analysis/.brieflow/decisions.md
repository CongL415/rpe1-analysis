# Runner decision journal

14 consequential decision(s) — most recent last.

- **2026-10-14T20:32:00.210904+00:00** · `pre-launch` · 🧑 **operator-answers** — SBS+phenotype: cellpose cyto3 (ignored notes cpsam hypothesis); ALIGN=False; CHANNEL_COMBOS=all 6 phenotype channels; MIN_CELL_CUTOFFS={all:50}; sbs CYTO_CHANNEL=Alexa 568 (ch2)  
  _why:_ operator answered the unresolved interview rows
- **2026-10-14T20:38:52.683076+00:00** · `pre-launch` · 🤖 **slack-gate** — paging OFF (operator declined)  
  _why:_ operator chose to skip Slack paging for now
- **2026-10-14T20:40:21.826107+00:00** · `preprocess` · 🧑 **launch-approved** — launch as reviewed  
  _why:_ operator passed --approved against a matching launch_review.json  
  _inputs:_ `{"review_sha256": "22466d0ac75cd2177c30b3b1d367a81b7382a8bf057fc854c85b005f193572f2"}`
- **2026-10-14T20:40:21.844734+00:00** · `preprocess` · ⚙️ **blocker-pause** — paused  
  _why:_ notebook_run_failed
- **2026-10-14T20:40:21.854355+00:00** · `preprocess` · ⚙️ **escalate-draft** — issue_draft written  
  _why:_ rc=5  
  _inputs:_ `{"path": "/data/analysis/cong-ops-2-analysis/analysis/.brieflow/issue_draft.md"}`
- **2026-10-14T20:41:23.984153+00:00** · `preprocess` · 🧑 **launch-approved** — launch as reviewed  
  _why:_ operator passed --approved against a matching launch_review.json  
  _inputs:_ `{"review_sha256": "22466d0ac75cd2177c30b3b1d367a81b7382a8bf057fc854c85b005f193572f2"}`
- **2026-10-14T20:41:24.760736+00:00** · `preprocess` · ⚙️ **blocker-pause** — paused  
  _why:_ notebook_run_failed
- **2026-10-14T20:41:24.770591+00:00** · `preprocess` · ⚙️ **escalate-draft** — issue_draft written  
  _why:_ rc=5  
  _inputs:_ `{"path": "/data/analysis/cong-ops-2-analysis/analysis/.brieflow/issue_draft.md"}`
- **2026-10-15T00:10:28.168813+00:00** · `pre-launch` · 🧑 **env-fix** — installed marimo; copied marimo phase notebooks + flow.sh from brieflow-analysis@marimo; brieflow submodule 83a3158 -> zarr3 6ffea12; PATH includes miniforge3 for conda  
  _why:_ old Jupyter template had no 0_preprocess.py; screen.yaml pins zarr3
- **2026-10-15T00:11:30.170744+00:00** · `preprocess` · 🧑 **launch-approved** — launch as reviewed  
  _why:_ operator passed --approved against a matching launch_review.json  
  _inputs:_ `{"review_sha256": "22466d0ac75cd2177c30b3b1d367a81b7382a8bf057fc854c85b005f193572f2"}`
- **2026-10-15T08:48:47.867539+00:00** · `merge` · ⚙️ **sweep-winner** — INITIAL_SBS_TILES=[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 21]  
  _why:_ 20 tiles farthest-point-sampled across well r02c02 (of 21 cell-dense tiles, from 21 total) for max spatial spread  
  _inputs:_ `{"n_tiles": 20, "plate": "1", "well": "r02c02"}`
- **2026-10-15T08:48:51.751890+00:00** · `merge` · ⚙️ **sweep-winner** — DET_RANGE=[0.225, 0.275]  
  _why:_ DET_RANGE=[0.225, 0.275] from determinant=(M*B)**2=0.2500 (M*B=0.5000; ph 0.5933762649494021µm / sbs 1.1867525298988042µm)  
  _inputs:_ `{"det_range": [0.225, 0.275]}`
- **2026-10-15T08:54:50.903597+00:00** · `classify` · ⚙️ **skip-phase** — classify not run  
  _why:_ RUN_CLASSIFY is not True; aggregate runs without a classifier
- **2026-10-15T09:48:46.924363+00:00** · `cluster` · ⚙️ **sweep-target-missed** — FINAL_LEIDEN_RESOLUTIONS=[1, 2, 3]  
  _why:_ no tested resolution (0.1-100) reached 20±5 genes/cluster; closest: resolution 1 at a median of 14.0 — every tested resolution gives larger clusters (library-limited); kept the resolutions around the closest. Set FINAL_LEIDEN_RESOLUTIONS or cluster_selection.target_genes_per_cluster to choose otherwise  
  _inputs:_ `{"target": 20, "tolerance": 5, "miss": {"closest_resolution": 1, "closest_median": 14.0, "tested": [0.1, 100], "largest_median": 54.0, "smallest_median": 1.0}}`
