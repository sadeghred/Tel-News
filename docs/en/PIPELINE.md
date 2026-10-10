# News Processing Pipeline

The target processing model is staged so each responsibility can be tested, replaced, or improved independently.

## Conceptual Stages

1. **Source ingestion** — receive content from configured sources.
2. **Normalization / transcript** — convert heterogeneous input into processable text and metadata.
3. **Event extraction** — identify the underlying news event.
4. **Relevance analysis** — reject material that does not meet configured editorial criteria.
5. **Clustering and deduplication** — detect overlapping reports and repeated events.
6. **Classification** — assign the item to its appropriate news category.
7. **Writing / rewriting** — produce publication-ready Persian news copy where required.
8. **Quality control** — validate output before publication.
9. **Metadata / hashtags** — attach publishing metadata.
10. **Review and routing** — decide destination(s) based on category and configuration.
11. **Publishing** — deliver through the appropriate platform adapter.

## AI-Hub

Selected AI stages use the central AI-Hub task layer. This keeps provider/model selection and credentials outside the Tel-News core.

## Local-First Processing

Operations that do not require generative AI can remain local. This reduces unnecessary AI calls and keeps the pipeline more efficient and deterministic.
