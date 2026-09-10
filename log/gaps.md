# Gap Log

Conceptual gaps only — moments where my mental model of how something works
turned out to be wrong. Not facts, not API details, not library quirks.

Written by the `/predict` skill. Reviewed weekly.

**How to use this:** look for repeated `Concept` values. One entry is noise.
Three entries sharing a concept is a real hole, and that is what I study when
I have free time.

Entry format:

```markdown
## YYYY-MM-DD — <short topic>
- **Context:** <task, one line>
- **I thought:** <my model, one line>
- **Actually:** <correct model, one to three lines>
- **Concept:** <underlying concept, 1-3 words>
```

---

## 2026-08-25 — partial-failure recovery stops at the wrong layer
- **Context:** OCR service — compose() discarding billed transcription when a post-execute stage fails
- **I thought:** getting the partial RunResult out of compose (via an exception carrying it) fixes the data loss; the pipeline needs no change
- **Actually:** surfacing the data only makes it *available*. It is still lost to the user unless the persistence layer writes it as ProviderRun rows. A recovery path is only finished at the layer where the data becomes durable and visible — not where it becomes reachable.
- **Concept:** failure-path persistence

## 2026-08-25 — guards applied to one input, not its siblings
- **Context:** OCR service — four of eight findings had the same shape
- **I thought:** each was a separate oversight
- **Actually:** all four were a correct idea applied to one field and not its twin. `artifact_path` sanitised `name` but not `run_id`; `_page_request` cleared `json_schema` but not `structured`; `retry_job` copied `options` but not `mode`; the extraction bypass checked `extracting` but not `output_mode`. In each case a second field carried the same authority as the guarded one, and the code read as safe because the guard was visibly present.
- **Concept:** paired-field invariants
