# User flows

```mermaid
flowchart TB
    SignIn[Sign in] --> Workspace[Open workspace]
    Workspace --> Health[Check API / network state]
    Workspace --> Upload[Upload documents]
    Upload --> Validate[Validate and index]
    Validate --> Knowledge[(Searchable knowledge)]
    Knowledge --> Retrieve[Run retrieval query]
    Retrieve --> Answer[Review answer and context]
    Answer --> History[Save response history]
    Answer --> Explore[Explore knowledge graph]
    Explore --> Update[Edit entity / relationship]
    Update -. re-index context .-> Knowledge
    Workspace --> Builder[Open form builder]
    Builder --> Fill[Complete schema form]
    Fill --> Check[Validate structured data]
    Check --> Export[Preview or export]
    Health -. retry .-> Validate
    Health -. retry .-> Retrieve
```

## Explainable retrieval journey

The user can move from a document set to a retrieval answer, then inspect the connected graph context instead of treating the response as a black box. Settings, graph limits, response modes, and network status remain visible so the workflow is debuggable and repeatable. The same workspace can turn reviewed knowledge into a validated, schema-driven output.
