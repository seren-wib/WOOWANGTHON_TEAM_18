# Cluster diagram: merge ⑤ ⑥ into one tab — lessons

## Log

- 2026-10-31: Decided to merge ⑤ and ⑥ (plan v67 moved the design to the physical/logical boundary; two tabs no longer help). Issue #11, Notion TODO added. Drawing in layers with a fact checklist after a previous one-shot redraw dropped items.

- 2026-10-31: Drew in six layers (zones → outside boxes → node contents → per-node networks → flows → failure notes/legend), exporting a PNG after each and fixing overflow/overlaps before the next. Fact checklist (124 phrases from plan v67 premise table, stages 00–12, 3′) passes 124/124 on the embedded XML; stale-word check (40%/80%/스티키/ECR/SQLite/임시 서브도메인/공유기 LAN/리더만 밖으로) is clean. Dropped the etcd-snapshot edge (not one of the nine flows; it shared a corridor with the image edge) — the R2 and snapshot boxes carry the fact. Port table/checklist/commands from old ⑤ intentionally not drawn (→ docs/design/cluster.md later). Branch pushed to the fork only; PR not opened yet (유성).

## Lessons

- A one-shot redraw drops facts; a per-layer render plus a phrase checklist against the source plan catches them cheaply (3 misses found on the first full pass, all fixed).
- draw.io zone titles do not wrap unless `whiteSpace=wrap`; long titles silently overrun neighbours. Keep zone titles short and put detail in a text cell.
- Long edge labels overlap boxes; number the edges and explain in a table.
- The generator (layer files + check script) lives outside the repo for now; if the diagram needs more revisions, commit it under `docs/architecture/tools/`.
