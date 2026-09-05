# The Nature of Conflict: Macro vs. Micro

Project Grendel adopts a "Commander/Delver" architecture, drawing inspiration from the duality of Macro and Micro management (similar to StarCraft II).

## 1. The Macro Loop (The Commander)
**Focus:** Preparation, Optimization, and Strategy.
**Mechanic:** TTRPG-style stat management and build optimization.

The Commander is responsible for the "Base Building" of the RPG experience:
- **Team Assembly:** Selecting characters based on complementary TTRPG stats (STR, DEX, INT).
- **Gear Engineering:** Using the blacksmithing/trading loops to equip the team for specific dungeon modifiers.
- **Strategic Directives:** Programming the high-level logic (the "Build Order") that the team will follow during a dive.
- **Success Metric:** Efficiency of the team build and resource management.

## 2. The Micro Loop (The Delve)
**Focus:** Execution, Reaction, and Tactical Efficiency.
**Mechanic:** Tactical State Machine.

The Delve is the "Battle" where the Commander's preparation is put to the test:
- **State Monitoring:** The API provides a real-time stream of enemy states and environmental hazards.
- **Tactical Response:** The bot must parse this state and execute the optimal "verb" (action) within a specific time window.
- **TTRPG Integration:** Stats act as modifiers. (e.g., High DEX increases the reaction window; High STR increases the impact of a successful strike).
- **Success Metric:** "Combat APM"—the speed and accuracy of the bot's reactions to the state machine.

## 3. The Synergy
The tension of the game exists in the gap between the two. A perfectly built team (Macro) can still fail if the combat logic (Micro) is too slow or flawed. Conversely, a brilliant combat script (Micro) can be overwhelmed by a lack of raw stats (Macro).
