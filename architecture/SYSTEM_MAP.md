# ICM system map

| Layer | Boundary |
|---|---|
| Interface | src/registry/orbe contains reusable orb visuals; src/app is the upstream gallery. |
| Intelligence / orchestration | Owned by consuming product; Hermes remains DEQODE orchestration where applicable. No new orchestrator here. |
| Model router | Owned by consuming product; visual components must not select models. |
| Services / voice | Existing consumer voice adapter supplies state and amplitude; inspect upstream recipes before adapting. |
| Data / knowledge | Owned by each product/entity; no community knowledge or transcripts belong in this public fork. |
| Governance / security | DQ Universal plus consumer permissions, server-side secrets, explicit microphone controls, safe errors and accessibility. |
| Deployment / integration | Component source copied selectively with licence and pinned provenance; gallery is not a required production service. |

Inventory: upstream Next.js gallery, React 19 components, shared hooks, examples and Vitest tests. Preserved without restructuring. No new deployment configured.
