# Skill Trees in RPGs: A Design Research Document

*Compiled for game design reference — covers video game and tabletop RPG systems, structural patterns, player psychology, and practical recommendations.*

---

## 1. Why Skill Trees Exist

Skill trees solve a specific design problem: how do you give players a sense of growth and choice without overwhelming them with every option at once? As one designer's guide puts it, trees "help manage complexity" — imagine a game like *God of War* starting with every move unlocked; it would be overwhelming. The tree paces out complexity and gives the player a map of what's coming.

The lineage traces back further than video games. The concept borrows from tech trees in board games like *Civilization*, but it was **Diablo II** (2000) that popularized the branching skill tree in the RPG genre — active and passive skills, a limited pool of points, and visual branches that made planning part of the fun. Players drew build plans on graph paper and debated them on forums; the planning became "half the fun," and prototypes that skip a tree entirely tend to feel static, since players have nothing to look forward to unlocking.

**Core functions a skill tree serves:**
- **Paces content** — reveals mechanical complexity gradually instead of dumping it all at once.
- **Creates anticipation** — players theorycraft and plan before they ever reach a node.
- **Signals identity** — the shape of a player's tree becomes a visual signature of their build.
- **Gates power** — ties strength to time/effort investment, which underpins a game's difficulty curve.
- **Encourages replayability** — different paths through the same tree produce different playthroughs.

---

## 2. Structural Archetypes

Most skill trees fall into a handful of recognizable shapes. Understanding these as a toolkit — rather than "the" skill tree — is the most useful mental model for a designer.

### 2.1 Linear chains
Simple, ordered unlocks (A → B → C). Good for narrative-driven games where the designer wants tight control over pacing and doesn't want build diversity to break story balance. Low cognitive overhead, but low player agency.

### 2.2 Branching trees (the "classic" shape)
The Diablo II model: a trunk with diverging branches, each branch themed around a playstyle (e.g., a Sorceress's Fire/Cold/Lightning branches). Players commit points and generally can't get everything — mutual exclusivity is the point. **Diablo II** offered active, passive, and unique class-flavor skills (Paladin auras, Barbarian shouts), but the fixed tier-gating sometimes forced players to buy "filler" points in skills they didn't want just to reach one they did.

### 2.3 Web / graph structures (no fixed trunk)
**Path of Exile's** passive tree is the canonical example: ~1,325 nodes in a single interconnected web shared by all classes, each class simply starting in a different region. This breaks the traditional "class defines your skill pool" model — any class can theoretically path to any other class's strengths, at a heavy point cost. The tree includes small stat nodes, larger "Notable" nodes (meaningful build-defining bonuses), and rare "Keystone" nodes that fundamentally rewrite a game mechanic. Because pathing costs points just to travel (not just to acquire power), the web format turns navigation itself into a build decision. Path of Exile 2 deliberately broke from PoE1's symmetrical, balanced tree shape toward asymmetric, "weirder" node clusters — explicitly trying to make the tree feel like a space for discovery rather than a spreadsheet.

### 2.4 Constellation / grouped clusters
**Skyrim's** perk system visualizes each of 18 skills as its own star-constellation, with perks as "stars" gated by base skill level and prerequisite perks. Each constellation is mostly a set of short linear chains with occasional forks, rather than one giant web — so it *reads* as more open than it mechanically is. It's frequently cited as one of the most visually satisfying trees in gaming, even though critics note the actual node effects can be underwhelming ("mostly dull") — a good reminder that visual presentation and mechanical depth are separate axes.

### 2.5 Grid / board systems
**Final Fantasy X's Sphere Grid** is a large roughly-circular board of ~828 nodes (in the original release) that all six party members traverse using consumable "spheres" rather than abstract points. Different sphere types do different jobs: Power spheres raise stats, Ability spheres unlock skills, Key spheres unlock gated sections, and "Skill spheres" can copy an ability another character already has anywhere on the board. Characters start in different regions (aligned to classic archetypes — Black Mage, Warrior, etc.) but the **Expert Grid** variant lets any character walk anywhere on the board from the start, and given enough time, every character can theoretically learn everything. This produces a distinctive tension: early-game roles feel classic-RPG distinct, but a fully-invested late game flattens everyone into the same stat ceiling, with only ultimate weapons and Overdrives differentiating characters. *Final Fantasy VII Rebirth's* "Folio" system is a direct spiritual descendant — branching node trees per character that unlock large stat jumps and new moves (a deliberate step up from *Remake's* flatter, more linear weapon-upgrade system).

### 2.6 Sub-tree clusters ("tree of trees")
**Borderlands 2/3** splits each character's kit into three parallel sub-trees, each themed around a build archetype, with a capstone/ultimate ability at the bottom of each. This lets a designer give one character 3 distinct "classes-within-a-class" without needing new characters, and gives players an easy mental model ("the tank tree," "the gun-damage tree," "the pet tree").

### 2.7 Hybrid / non-tree systems worth knowing
Not every RPG uses a literal branching tree, and it's useful to see the alternatives your target genre might expect:
- **Diablo III** dropped the tree entirely in favor of unlocking *all* active/passive skills by level, then modifying each active skill with interchangeable "runes." The goal was to make every skill technically viable at all times; in practice, min-maxers still converge on a small set of "best" rune/skill pairings, which is a useful cautionary tale — removing the tree doesn't automatically remove convergence toward optimal builds.
- **Monster Hunter World** ties "progression" to weapon/armor crafting rather than a menu tree — mechanically a tree (materials gate armor sets, sets gate content) but presented entirely diegetically through gear rather than abstract nodes.
- **Downwell**-style roguelites offer a small "pick one of three" choice between short runs instead of a persistent tree — this trades long-term build planning for tight, repeatable decision moments.

---

## 3. Node Types: What a Node Can Actually Do

A common design failure is filling most of a tree with flat stat modifiers (+1% melee damage), which players intellectually register as progress but rarely *feel* in play. The most-cited design guidance (echoed across multiple sources) is to combine:

1. **Stat modifier nodes** — cheap filler/connective tissue between meaningful nodes. Necessary for pacing and path cost, but shouldn't dominate.
2. **Impactful ability nodes** — unlock genuinely new gameplay options (new attacks, new interactions, new verbs), not just bigger numbers.
3. **Notable/keystone-style nodes** — rare, build-defining nodes that meaningfully change how a mechanic works (Path of Exile's Keystones are the purest example — a single node can rewrite a core rule of the game for that character).
4. **Mastery/choice nodes** — Path of Exile's Mastery system requires investing in a themed cluster first, then lets the player pick *one* bonus from a themed menu — a good pattern for giving late "flavor" choices without tree bloat.

**Design guidance repeated across sources:** avoid a fully-completable tree if you want builds to stay meaningfully distinct; scarcity of points is what makes the choice matter. A tree everyone eventually fills completely (like FFX's endgame) stops being a differentiator and becomes a checklist.

---

## 4. Player Interaction Patterns

### 4.1 Point economy
How players *earn* points shapes pacing as much as the tree's shape does:
- **Level-based** (most trees): points per character level — predictable, easy to plan around.
- **Currency/consumable-based** (FFX Sphere Grid): points are physical items (spheres) looted or farmed, which turns progression partly into a resource-management/farming loop rather than a pure "wait for next level."
- **Quest-based bonus points** (Path of Exile): extra points from specific quests, which rewards exploration/completionism alongside combat.
- **Dual currency** (Skyrim): a skill *level* (raised through use — "practice makes perfect") gates which perks are available, while a separate perk point (from character level) is spent to actually buy them. This ties two different progression rates together and can create friction (see Section 6 on grind).

### 4.2 Prerequisites and gating
Almost every tree gates deeper nodes behind either (a) a minimum number of points already spent in that branch, (b) a specific prerequisite node, or (c) a character/skill level. This is what makes "pathing" a decision distinct from "picking" — in web-style trees (PoE) you're often paying points just to *travel* toward a node you want, which makes the map itself a resource.

### 4.3 Respec (rebuilding your build)
Whether and how easily a player can undo their choices is one of the most consequential — and most debated — decisions a designer makes:
- **No respec / permanent choices** creates weight: every point spent matters more, and the tree becomes part of the character's identity. But it punishes experimentation and can trap new players in a build they don't understand yet, since most players make their worst allocation decisions early, before they've learned the systems.
- **Full free respec** (mid/late World of Warcraft, Baldur's Gate 3's "Withers" NPC) treats builds as situational loadouts (a PvE build vs. a raid build vs. a PvP build) rather than a character-defining commitment — maximizes experimentation, minimizes narrative weight of choice.
- **Limited/costly respec** (Elden Ring's Larval Tears, currency-gated respecs) is the common middle ground: it keeps decisions meaningful without permanently punishing a bad early pick.

There's active tension in the community about this — a 2023 piece on singleplayer RPGs argues restrictive respec design often persists simply because "that's how it's always been done," not because it's demonstrably better design. On the other side, some designers argue *forced* commitment is itself a valuable agency mechanic: being made to choose whether to detour your build toward a skill check right now, rather than save points for your ideal endgame build, is cited as a way to make each playthrough feel more personally authored.

### 4.4 Sunk cost and engagement
Skill trees are also, bluntly, a retention mechanic. Once a player has invested hours of planning and points into a build, the psychological cost of abandoning it (or the game) rises — the same sunk-cost dynamic that underlies leveling loops broadly. This isn't necessarily manipulative; ethically-used, "protecting an investment" can coexist with genuine fun. But it's worth being deliberate about, especially if a tree design leans on grind (see below) rather than interesting choices to create that investment.

---

## 5. Case Study Comparisons

| Game | Structure | Points via | Respec | Notable trait |
|---|---|---|---|---|
| **Diablo II** | Branching, per-class | Level-up | None (until late patches) | Pioneered active/passive class trees; tier-gating forced some "filler" spend |
| **Diablo III** | No tree — all skills unlocked by level, modified by runes | N/A | Free, instant | Removed the tree to maximize flexibility; convergence on "best" combos still occurred |
| **Diablo IV** | Branching, per-class (explicitly "harkens back to Diablo II") | Level-up | Paid respec | Return to a tree after D3's tree-less experiment |
| **Path of Exile (1)** | Massive shared web (~1,325 nodes), all classes on one tree | Level-up + quests | Limited (orbs) | Class only determines starting location, not your ceiling; Notables/Keystones/Masteries as node tiers |
| **Path of Exile 2** | Per-class dedicated tree layouts (no longer fully shared) | Level-up | TBD (in flux during Early Access) | Deliberately asymmetric/"wild" node shapes vs. PoE1's balanced symmetry |
| **Skyrim** | 18 constellation trees (per skill) | Perk points (level) gated by skill-use level | None (vanilla) | Visual polish carries a mechanically simpler system; heavily modded (e.g. "Ordinator," "Constellations") to add depth |
| **Final Fantasy X** | Circular board (Sphere Grid), shared by party | Consumable spheres (farmed) | Fully mutable (spheres aren't consumed on move in "Expert" grid) | Dual grid options (Standard/Expert) trade defined roles vs. total flexibility; late game flattens character differentiation |
| **Final Fantasy VII Rebirth** | Branching "Folio" trees per character | Points + found books | N/A | Explicit evolution of Remake's flatter linear weapon upgrades, echoing FFX Sphere Grid |
| **Borderlands 2/3** | Three parallel sub-trees per character, each with a capstone | Level-up | Paid respec (in-game vendor) | "Tree of trees" — lets one character serve 3 archetypes |
| **World of Warcraft** | Branching, per-spec | Level-up | Free/cheap in modern versions | Loosened respec restrictions over the game's lifetime in response to player friction |

---

## 6. Common Pitfalls (Repeated Across Sources)

1. **Stat-modifier bloat.** Filling most of the tree with "+1% X" nodes that are individually imperceptible in play. Players *notice* new verbs, not incremental numbers.
2. **Grind-driven trees.** Skyrim's Smithing skill famously encouraged players to craft hundreds of throwaway iron daggers purely to raise a number — progression divorced from meaningful play. If earning points requires boring repetition, the tree teaches the wrong behavior.
3. **UI pacing mismatches.** *Doom Eternal* is cited as an example where pausing fast action to navigate a skill menu broke the game's core pacing — a reminder that *when* and *how* the tree is presented matters as much as its content. Contrast with tight roguelite "pick one of three, keep moving" moments.
4. **Fake choice / false branching.** If every path in a tree is secretly "correct" (because the tree is small enough to eventually complete, or because one branch is strictly efficient), the sense of meaningful choice collapses into a checklist.
5. **Everyone ends up the same.** As seen in FFX's late game — if the tree is big enough and shared enough that all characters/builds converge on the same endpoint, the tree stops functioning as an identity system.
6. **Overcomplicated pathing without payoff.** Path of Exile's tree is beloved by veterans and cited by newcomers as intimidating/"incomprehensible" — density is not inherently good; it should scale with your target audience's appetite for theorycrafting.

---

## 7. Tabletop RPG Approaches

Tabletop systems solve the same "meaningful progression" problem without a persistent digital UI, which forces different tradeoffs.

### 7.1 D&D 5e — feats and multiclassing as a loose "tree"
D&D 5e doesn't use a formal skill tree UI, but its **feats** and **multiclassing** rules create tree-like structures socially enforced through prerequisites (minimum level, prior feat, ability score minimums). Community-made "feat chain" content (e.g., fan-made Multiclass Feats collections, or *Level Up: Advanced 5E's* three-stage "multiclass feat chains" that combine two classes into one archetype) shows designers extending the base system specifically to recreate tree-like progression the core rules leave out. A frequent critique in that community: 5e hands out feats too sparingly for feat-chains to function as a real build-planning tool the way a video game tree does — by the time you can finish a chain, you're deep into the campaign.

### 7.2 Pathfinder 2e — Dedication feats as branching multiclass trees
Pathfinder 2e's multiclassing is explicitly built as **feat chains**: a "Dedication" feat opens access to a second class's features, and further feats in that chain (e.g., three-tier "Basic/Expert/Master Spellcasting" chains for casters) deepen the investment. Unlike 5e, Pathfinder's approach never splits your character's actual class levels — it's a parallel progression track layered on top of your primary class, which the tabletop community generally regards as more modular and less punishing to a character's core competency.

### 7.3 General TTRPG skill-tree principles
Across tabletop systems generally, three node categories recur: **Skill Nodes** (abilities), **Attribute Nodes** (stat increases), and **Special Ability Nodes** (unique/rare powers) — directly mirroring the video-game node taxonomy in Section 3. Two structural approaches dominate: **linear progression** (step-by-step, good for tight narrative pacing) and **branching systems** (specialization paths, good for build diversity). Some systems go further with **dynamic trees that respond to fiction**, not just points spent — *Tyranny* (a video game, but built on TTRPG-style design principles) is the standout example: certain abilities only unlock based on which faction the player has aligned with narratively, tying the "tree" directly to story choices rather than pure mechanical investment. The *Star Wars Saga Edition* RPG is cited as a strong tabletop example of a **multiclass/hybrid system** — letting players blend abilities across classes while keeping the math balanced.

### 7.4 Point-buy and life-path alternatives
Not every tabletop system uses trees at all. **Point-buy systems** (allocate a pool of points across skills/attributes freely) offer maximum flexibility but risk "glass cannon" characters unless designers add safeguards — **point buckets** (separate pools for physical/mental/social traits, so you can't dump everything into one axis) and **scaling costs** (each additional rank in a skill costs progressively more) are the two most common fixes. **Burning Wheel's** life-path character creation is a narrative alternative: your character's skills emerge from a structured backstory-building process rather than a menu of nodes, tying "build" directly to "story" from character creation onward. **Standard arrays/templates** are the usual on-ramp for new players in point-buy systems, while full custom point allocation is reserved for experienced players who want the flexibility.

---

## 8. Practical Recommendations for a New RPG's Skill Tree

Drawing the above together into actionable guidance:

1. **Decide your shape early, and let it match your genre's pace.** A branching tree (Diablo-style) suits action combat with build identity; a web (PoE-style) suits a long-tail live-service game where theorycrafting *is* the endgame; a grid/board (FFX-style) suits parties with multiple characters you want to differentiate — and to explicitly *not* differentiate late-game, if you want flexibility to matter more than fixed roles.
2. **Budget your node types deliberately.** A rough, commonly-implied ratio: mostly cheap connective/stat nodes, a meaningful minority of new-verb ability nodes, and a small number of rare build-defining nodes (keystones/notables) that players specifically plan routes toward.
3. **Make points scarce enough that choices actually compete.** If your tree is small enough (or points plentiful enough) that a dedicated player completes it, the tree stops differentiating builds. Decide explicitly whether "eventually get everything" is a feature (FFX) or something to avoid (PoE).
4. **Choose your respec policy on purpose, not by default.** No respec = weightier choices, more player anxiety, more built-in identity. Free respec = builds become situational loadouts, more experimentation, less narrative weight. Costed/limited respec is the common compromise — pick based on whether you want players to feel like they're *authoring* a character or *tuning* a toolkit.
5. **Never gate points behind boring repetition.** However players earn points (leveling, spheres, quests), make the earning activity itself something they'd choose to do anyway — the Skyrim-Smithing grind problem is the cautionary tale to avoid.
6. **Match the UI's weight to the moment.** A full-screen tree-planning menu is appropriate between missions/at camp; it's actively harmful mid-combat-loop pacing (Doom Eternal's cited mistake). Consider a lightweight "pick one of a few" prompt for in-the-moment choices, reserving the full tree UI for deliberate planning sessions.
7. **Consider tying nodes to fiction, not just numbers**, especially if the game has a strong narrative layer — Tyranny's faction-gated abilities are a standout tabletop-influenced model for making the tree feel like part of the story rather than a menu bolted onto it.
8. **If multiple characters/classes share one system, decide explicitly how much they should converge.** Shared trees encourage build creativity (PoE) but risk everyone ending up equivalent at endgame (FFX); separate per-class trees preserve identity but reduce cross-build experimentation (PoE2's move away from a fully shared tree).

---

## Sources Consulted
- TheGamer — "13 Best Skill Tree Designs In Video Games"; "What Goes Into Crafting Good Skill Trees In RPGs"; "Which Sphere Grid Should You Choose In Final Fantasy X?"
- Eneba Hub — "10 Best Games With Skill Trees in 2026 for RPG Fans"
- Medium (Thomas Theux) — "Game Design is easy. A guide to crafting skill trees"
- gamedesigning.org — "Game Design Skill Trees (Beginners guide)"
- ttrpg-games.com — "Skill Trees in TTRPGs: Basics and Design"; "How Designers Build Player Agency in RPGs"
- pathofexile.com and Path of Exile Fandom Wiki — Passive Skill Tree documentation
- futurelighthouse.com — "Path of Exile Passive Skill Tree Explained"
- poetrades.net — "Path of Exile Passive Skill Tree: Complete Guide"
- mmojugg.com and Goodreads community posts — Path of Exile 2 tree design changes
- Final Fantasy Fandom Wiki — "Sphere Grid"; EIP Gaming and Steam Community guides on the Sphere Grid
- TechRadar — "Final Fantasy 7 Rebirth's skill trees"
- Nexus Mods — Skyrim "Constellations" perk mod documentation
- FandomWire — "From Skyrim To Shadow of Mordor, These Are 5 of the Best Skill Trees In Gaming"
- FictionHorizon — "20 Most Satisfying Skill Trees In Games"
- NeoGAF community thread — "Best skill trees in games"
- Goodreads blog post — "The Two Diablos: D&D, Game Mechanics, and Design Philosophy PART TWO"
- Blizzplanet — BlizzCon 2019 Diablo IV Talent Tree coverage
- PC Gamer — "why is it still so annoying to respec in singleplayer RPGs?"
- Pretzel — "Should games allow you to respec?"
- G2A News — "What Is a Respec in Gaming?"
- EN World forums — D&D 5e/Pathfinder multiclassing and feat-chain discussions
- Pathfinder Authority — "Pathfinder Multiclassing Rules and Strategies"
