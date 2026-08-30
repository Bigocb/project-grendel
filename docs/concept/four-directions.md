# Four Directions: Project Concept Comparison

*Comparison of four candidate shapes for an API-only RPG. Each represents a different "bot problem" for the player to solve.*

## Comparison Matrix

| Feature | Path A: Party-as-Fleet | Path B: Single Persistent Hero | Path C: Guild/Settlement | Path D: The Synthesis |
|---|---|---|---|---|
| **Core Loop** | Dispatch parties $\rightarrow$ wait $\rightarrow$ manage fallout | Node-by-node exploration $\rightarrow$ shared world interaction | Base building $\rightarrow$ dispatch workers $\rightarrow$ defend | A + B + C simultaneously |
| **Bot Problem** | Scheduling multiple parties vs. different timers/risks | Pathing, opportunistic PvP, build optimization | Production-chain and strategic settlement metagame | Reconciling three different clocks and avatars |
| **Primary Risk** | Combat resolution may feel like "extraction()" | Might feel too "thin" compared to fleet management | Loses the "mobile unit" feel; becomes spreadsheet optimization | Massive scope creep; conflicting foundational systems |
| **Key Appeal** | Real stakes (injury/permadeath) | Direct inheritor of the "scarce shared economy" | High-level strategic metagame | Combines all distinctive mechanics |

---

## Detailed Path Analysis

### Path A — Party-as-Fleet
**Focus:** Expedition management.
- **Loop:** Dispatch $\rightarrow$ Resolution $\rightarrow$ Downtime/Recovery.
- **Appeal:** Juggling multiple units against different timers (similar to SpaceTraders' best loops).
- **Required Specs:** Roster limits, injury/permadeath rules, duration tiers, combat resolution model.

### Path B — Single Persistent Hero (Current Working Spine)
**Focus:** MUD-style exploration.
- **Loop:** Waypoint movement $\rightarrow$ Combat/Gathering $\rightarrow$ Trade/Craft.
- **Appeal:** Direct persistent presence in a shared world; high build depth.
- **Required Specs:** Travel graph, PvP rules, death consequences, contested resource rules.

### Path C — Guild / Settlement Management
**Focus:** Base building and power projection.
- **Loop:** Build/Upgrade $\rightarrow$ Dispatch Workers $\rightarrow$ Defend/Raid.
- **Appeal:** Strategic metagame and internal production-chain optimization.
- **Required Specs:** Building trees, worker timers vs. upkeep, raid/defense mechanics, diplomacy.

### Path D — The Synthesis
**Focus:** Hybridization of A, B, and C.
- **Verdict:** Not currently pursued. Risk of "scope trap" and conflicting system clocks.
- **Potential:** Could be a late-game unlock layered on Path B.
