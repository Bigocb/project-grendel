# Open Questions

## Core Mechanics
- **Battle Style & Mechanics**: What style of battle are we using? What are the specific battle mechanics we want to implement? (e.g., Turn-based, Real-time with cooldowns, Atomic/Single-call, Multi-step/Resource-based).
    - *Current Discussion*: Real-time action vs. Turn-based?
- **Combat Translation (The "Tactile Gap")**: How do we translate action-oriented combat into a non-visual, API-driven medium?
    - *Challenge*: Replacing visual/tactile feedback (swinging a sword) with request/response cycles.
    - *Question*: How do we make sending requests and waiting for responses feel like a "fun" combat experience?
    - *Fundamental Question*: Is "combat" the right conceptual direction for an API-only game, or should the primary conflict be framed differently?
- **Alternative Directions to Combat**:
    - *Survival*: Would survival mechanics (resource management, environment pressure) translate well to an API design?
    - *Exploration*: Could the focus be on discovery/exploration, where combat is a secondary/simplified event (e.g., TTRPG-style dice rolls) rather than a core tactile loop?
    - *TTRPG Influence*: Looking at TTRPGs as a primary reference for engaging gameplay without visuals.
- **Class System**: How structured is the class system?
    - *Hard Classes*: Defined classes with specific gating.
    - *Free Builds*: Your gear/abilities define your "class" (e.g., brawler build vs. scout build).
    - *Discussion*: How heavily should we lean into formal classes vs. emergent builds?
- **Build Inspiration**: Which games have the best build systems (abilities, experience, etc.) that we want to draw from?

## API & User Experience
- **The "Doing it for them" Balance**: How much of the operational burden (e.g., handling 429s, optimizing call efficiency) should be managed by the API versus left to the player's bot?
    - *Guiding Question*: "Are we doing it for them?"
    - *Goal*: Find the balance between a frustrating experience and a challenge that rewards technical optimization.
