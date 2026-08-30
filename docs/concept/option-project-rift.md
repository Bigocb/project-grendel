# Design Option: Project Rift (Headless API RPG)

*Note: This is a proposed design direction, NOT the decided path.*

## Concept
An API-only RPG inspired by SpaceTraders. No official client; the interface is purely code. The game focuses on build mastery and a persistent, reactive world rather than logistics.

## Core Pillars
1. **Build & Power Fantasy (Primary):** Mastery lives in the assembly and deployment of builds (gear, skills, classes) rather than real-time execution.
2. **World Reactivity (Secondary):** A world that remembers; permanent changes (e.g., bosses staying dead) and NPCs that recognize specific agents.
3. **Systems & Emergent Economy (Supporting):** Crafting and trade exist primarily to fuel the build and world reactivity.

## Key Mechanics
- **Core Loop:** Gather Power $\rightarrow$ Assemble Build $\rightarrow$ Commit to World $\rightarrow$ Outcome Changes World State $\rightarrow$ Reshapes Next Steps.
- **World Scope (`world_id`):** Every piece of world state is scoped. Allows for solo instanced universes, guild universes, and public shared universes without re-architecture.
- **Cross-Universe Systems:** Marketplace, Async PvP, and Leaderboards are shared across all universes from day one.
- **Combat:** Lightweight multi-step encounters with a few genuine decision points, each with a sane default to prevent bot stalling.
- **Lore:** Thin lore (naming and identity only), following the SpaceTraders philosophy of systems mastery over narrative prose.

## Current Ideation: Classes/Archetypes
- **Hybrid Model (Proposed):** Classes grant distinct resources and signature abilities, while gear and general skills remain universal.
- **Identity:** Leaning toward permanent or costly-to-change class identity.
- **Scope:** Proposed as combat-only to keep non-combat verbs consistent.
