# User flows

```mermaid
flowchart LR
    SignIn[Sign in] --> Workspace[Open workspace]
    Workspace --> Upload[Upload documents]
    Upload --> Retrieve[Run retrieval query]
    Retrieve --> History[Review response history]
    Retrieve --> Explore[Explore knowledge graph]
    Explore --> Update[Edit entity / relationship]
    Workspace --> Builder[Open form builder]
    Builder --> Fill[Complete schema form]
    Fill --> Export[Preview or export]
```

## Explainable retrieval journey

The user can move from a document set to a retrieval answer, then inspect the connected graph context instead of treating the response as a black box. Settings, graph limits, response modes, and network status remain visible so the workflow is debuggable and repeatable.
