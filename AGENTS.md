# Agent Guidelines - Project Grendel

## Documentation Maintenance
Documentation is the "Digital Twin" of the project. It must be a strict reflection of current reality, not a set of aspirational goals.

### Autonomous Updates
Agents MUST autonomously update documentation when any of the following occur:
1. **Decision Finalized**: When a brainstorming session reaches a consensus or a design decision is made.
2. **Spec Change**: When a technical implementation diverges from the existing spec.
3. **Feature Completion**: When a working artifact is produced that changes the project's capabilities.

### Update Protocol
- **Brainstorming $\rightarrow$ Concept**: Move refined ideas from `docs/brainstorming/` to `docs/concept/`.
- **Concept $\rightarrow$ Spec**: Translate validated concepts into technical requirements in `docs/spec/`.
- **Spec $\rightarrow$ Protocol**: Define strict data shapes and API contracts in `docs/protocol/`.

### Verification
After any documentation update, the agent must verify that the new state does not conflict with other existing documents. If a conflict is found, it must be resolved via the `docs/brainstorming` flow before updating the spec.
