# Restructure Log

Append-only audit trail for every file move, rename, addition, or deletion performed during the project restructure into the ICM-style stage layout (per Van Clief, Interpretable Context Methodology).

## Rules in force

1. **No file may be deleted.** Superseded or noise files are moved to `_archive/`, not removed.
2. **No file may be renamed.** Basename is preserved on every move; only the parent path changes.
3. **Every change is recorded here** before or alongside the git commit that effects it.
4. **One git commit per batch**, with the batch label in the commit subject, so `git log` and this log cross-attest each change.
5. **No content edits** to existing files without separate explicit approval. Newly *created* files (this log, `CONTEXT.md` stubs, `.gitkeep`) are permitted as part of scaffolding.

---

## Batch 00 — Scaffolding

**Date:** 2026-05-19
**Approved by:** user message "I'd like you to implement the retructuring while adhering to our rule of no deleting or renaming. If you use the restructure log and good practice git version control, you can have full autonomy to solve the task"

### Directories created (new, empty)

```
00_admin/
01_literature/references/{academic, policy_grey, risk_uncertainty, reference_works, methodology_genai}/
02_theory/{output, _scratch}/
03_corpus/{references, output}/
04_codebook/output/
05_analysis/{output, _scratch}/
06_report/                 # will receive coding/my_report/ contents in Batch 05
_archive/
_config/
shared/
skills/
```

### Files created (new)

| File | Purpose |
|---|---|
| `RESTRUCTURE_LOG.md` | this audit trail |
| `CONTEXT.md` | Layer 1 routing stub (new, placeholder; full content to be drafted with user approval) |
| `<stage>/CONTEXT.md` (per numbered stage) | Layer 2 stage-contract stubs (placeholders only) |
| `<empty-dir>/.gitkeep` | force-track empty scaffolding folders |

No existing files were moved, renamed, or deleted in this batch.

---

## Batch 01 — Promote CLAUDE.md to project root (Layer 0)

**Date:** 2026-05-19

| Action | Source | Destination | Basename preserved? | Reason |
|---|---|---|---|---|
| move (git mv) | `coding/CLAUDE.md` | `CLAUDE.md` | yes | Promote agent-orientation document from sub-folder to workspace root, per ICM Layer 0. File contents unchanged; only path changes. Internal paths inside CLAUDE.md (e.g., `coding/Readthrough_Notes_v1.md`) are now stale and will need updating in a later, separately-approved content edit. |

---
