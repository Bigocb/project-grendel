# World Model: Universes, Not a Universe

*This is a core architectural proposal for handling world state and concurrency.*

## The Problem: Divergence vs. Convergence
Building a single shared world (EVE-style) is ambitious but rigid. Building private worlds per agent is simple but traditionally a dead end for shared gameplay. 

**The Contradiction:** You cannot merge divergent per-agent world states into one shared canon later. If Agent A kills a boss and Agent B doesn't, there is no logical merge that produces a single true timeline.

## The Resolution: First-Class `world_id`
Instead of treating "instanced" and "shared" as different stages or modes, every piece of world state is scoped by a `world_id` from day one. The `world_id` is not an implementation detail, but a first-class concept.

### Implementation Matrix

| world_id | Meaning | Experience |
|---|---|---|
| `world_id = agent_id` | Solo instanced universe | The v1 default; every agent has their own private world. |
| `world_id = guild_x` | Small private universe | A group of agents opts into a shared, private instance. |
| `world_id = public_1` | Large open universe | An EVE-style shared world, unlocked without re-architecture. |
| `world_id = event_x` | Limited-time universe | A seasonal or special event space. |

## Implications
- **No Migrations:** Transitioning from solo to shared gameplay doesn't require data migration, only changing the `world_id` value.
- **Consistent Logic:** The same region, combat, and progression logic run regardless of whether the `world_id` is private or public.
- **Parallel Realities:** Fictionalizes the transition—a "rift" can pull a character from a private universe into a shared one, making the mechanic and the lore reinforce each other.
