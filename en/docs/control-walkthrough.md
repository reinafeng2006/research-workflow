# v0.8 control walkthrough

Method: manual tabletop review against shared-controls.md and stage diagrams/templates, using 14 fictional scenarios. No real research, API submission, worker launch or independent-agent verification was performed. Outcomes below are policy-path findings, not tests of a running controller. Budget values are examples, not defaults.

| Case | Input | Observed policy path |
| --- | --- | --- |
| Reuse cross-stage approval | Step 3 results reviewed and exact Step 4 plan approved; unchanged. | Cite authorization ID; no duplicate approval. |
| Authorization delta | Budget or expected outputs change. | Retain old authority; approve only uncovered delta, not a summary boolean. |
| Warning is not a pass | Ordinary rate warning; batch has not passed. | Notify; no next batch. Diagnose within authority; pause at a stop condition. |
| Normal continuation | Batch passes, meaningful progress, no stop, next batch authorized. | Continue after budget admission; no additional approval. |
| Materials-ready closure | Approved criterion materials_ready; no submission planned. | Submission authority not applicable to closure; retain not-submitted state for human closure. |
| Actual submission | Materials prepared but no exact-version/channel authorization. | Do not submit; retain prepared state. |
| Required gate failure | Required archive unusable. | Cannot relabel not_applicable or complete; unaffected portions may be accepted separately. |
| Early delivery constraints | Step 1 knows recipient requires independent validation data. | Record source; map into Step 2 design instead of waiting until Step 6. |
| Valid evidence reuse | Version, assumptions, dependencies, use and independence still match a passing check. | Cite check ID and applicability assessment; no rerun. |
| Local invalidation | One dependency changes; others remain valid. | Preserve records, invalidate affected scope; recheck only authorized affected work. Failed checks are not passes. |
| Concurrent budget admission | Fictional token units: limit100, spent40, in-flight remaining30, shutdown reserve10, new25. | 105 exceeds limit: reject. New15 totals95: reserve serially before dispatch; next task sees updated reservations. |
| Restart and telemetry | Restart or rollback; exact token telemetry unavailable. | Never reset totals; use approved conservative estimates/caps. No credible bound means no dispatch; no claim of enforced hard limits. |
| Combined roles | Coordinator produces; original verifier materially authors a repair. | Coordinator may produce but needs another verifier; repair author cannot independently verify that repair. |
| Deduplication and pause | Equivalent task in flight, or resource pause active. | No duplicate dispatch; reused evidence cannot lift a pause; follow recovery authority. |

All 14 paths are consistent with the revised specification. Runtime interruption, telemetry accuracy, race-free reservations and actual reviewer independence still require host implementation; this review does not establish them.
