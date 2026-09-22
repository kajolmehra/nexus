# Architecture

Nexus is a Vite/React/TypeScript client organized around feature pages and shared state stores. A typed API module communicates with a LightRAG-compatible backend, while Firebase handles authentication and Firestore connectivity status. Zustand stores coordinate retrieval settings, chat history, graph data, and session state.

## Feature boundaries

- **Documents:** upload, supported-file guidance, document status, and deletion.
- **Retrieval:** query settings, response modes, streaming/async states, history, and retry/backoff.
- **Graph:** raw graph normalization, Sigma rendering, node search, layouts, focus, and property editing.
- **Forms:** JSON Schema/UI Schema definitions, validation, multi-step navigation, preview, and PDF-ready output.
- **Workspace:** authentication, access control, API settings, language, theme, network health, and reusable UI primitives.
