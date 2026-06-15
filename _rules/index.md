---
permalink: /rules/
title: Rules
nav_order: 1
next_doc:
  title: Abilities
  url: /rules/abilities/
---

Sources: After Party Rulebook (48p) + FAQ & Errata v1.3

---

## Character Profile

Each character has:

- **Size**: base diameter in millimetres
- **Cost**: number of Ducats to include in the gang

### Points (never below 0 or above starting value)

| Point | Abbrev. | Role |
|-------|---------|------|
| Action Points | AP | Actions per turn; max 3/turn; fully replenished at the start of each round |
| Life Points | LP | At 0 = removed from the game ("killed") |
| Will Points | WP | Boost dice rolls (+1 die per WP, max 2 WP per roll); cast spells |
| Command Points | CP | Commands, Command Abilities, initiative |

### Statistics (never below 0 or above 10)

| Stat | Role |
|------|------|
| Move | Movement distance in inches |
| Dexterity | Dodge and agility; threshold to beat when targeting in Combat |
| Attack | Combat and ranged; 1 point = 1 die |
| Protection | Defence; protection rolls against damage |
| Mind | Magic; mental rolls |

### Keywords & Character Abilities

Keywords have no inherent effect on their own — they serve as reference targets for certain rules and abilities. Character Abilities are listed on the profile or gained through Command Abilities.

---

## Dice

Carnevale uses **D10s**. A successful result = an **Ace**.

- **10** = always an Ace
- **1** = never an Ace
- Default: **7+ = Ace** (except Attack Rolls and Magic Rolls)

**Maximum 10 dice per roll. Minimum 0 dice.**

Every roll must include one **Destiny Die** (a different colour) which determines Critical/Fumble. It can **never** be re-rolled.

A die may only be re-rolled **once**; the second result is final.

When multiple players want to spend WP on the same roll: declare in any order → resolve the roll. You cannot change your mind after declaring.

### Results

| Result | Condition |
|--------|-----------|
| **Success** | ≥ 1 Ace |
| **Fail** | 0 Aces |
| **Critical** | Destiny Die = 10 **AND** ≥ 1 other Ace (the Destiny Die also counts as an Ace → a Critical always has at least 2 Aces) |
| **Fumble** | Destiny Die = 1 **AND** 0 Aces |

### Types of Rolls

**Basic Roll**: uses one of the active character's stats. Threshold: 7+ unless stated otherwise.

**Opposed Roll**: both characters make a Basic Roll using the same stat. The targeted character rolls first and counts their Aces. That total is subtracted from the active player's dice pool (who then makes a Basic Roll with the remaining dice). *The targeted character cannot score Criticals or Fumbles.*

**Attack Roll**: uses ATTACK. Threshold = **target's DEXTERITY**. 10 always Ace, 1 never Ace.

**Magic Roll**: uses MIND. Threshold = **spell's Difficulty**.

**Protection Roll**: uses PROTECTION. Threshold: 7+.

| Protection Result | Effect |
|-------------------|--------|
| Success | Reduce Damage by 1 per Ace |
| Fail | No effect |
| Critical | Add 1 extra Ace to the roll, then reduce Damage by 1 per Ace |
| Fumble | Increase Damage by 1 |

### Will Points

Before a roll, spend up to **2 WP**. Each WP = +1 die (up to the maximum of 10 dice).

---

## Initiative

At the start of each round: each player chooses a character with remaining CP and rolls a number of dice equal to that character's **current remaining CP**. Count **7+** results. Highest total takes initiative (tie = re-roll).

If a player has no characters with remaining CP → automatically loses the roll. If no players have CP → each player rolls 1 die.

Initiative rolls **cannot be modified, re-rolled, or altered**.

---

## Measuring & Line of Sight

**Measuring**: in inches from the closest point of the base. May be measured at any time.

**Line of Sight (true LOS)**: draw a straight line between the two miniatures. If any part of the body or head is visible → LOS established.

**Terrain ≤ 1" high**: ignored for measuring, LOS, and movement.

**Base Contact**: bases physically touching. Vertical tolerance of 1". If two bases are within 1" of each other and both touching the same obstacle ≤ 1" high → base contact for weapons with 0" range (but the enemy still counts as being in cover in this case).

---

## Cover

If ≥ 25% of an enemy character is obscured → they are **in cover** → **+1 Protection**.

- A character **in base contact with their attacker** is never in cover.
- A character **in water** is always in cover, unless in base contact with their attacker.
- *FAQ v1.3:* Concealment adds or subtracts from the existing cover modifier (does not replace normal cover). E.g. Concealment (-1) causes the character to lose the benefit of standard cover.

---

## Attacks of Opportunity (AoO)

Costs **0 AP**. Cannot be *chosen* voluntarily but is triggered by various rules.

Choose: **Combat**, **Grapple**, or **Drown** action — treat as a normal action with all applicable Character Abilities, Weapon Abilities, and modifiers.

---

## Actions

### Run/Climb — 1 AP

Move up to the character's MOVE value in inches, broadly horizontally. May move over terrain < 1" high. **Cannot move through other characters.**

**Swimming**: in water, reduce MOVE by 2" at the start of the action (except Water Creature).

**Climbing Vertical Terrain > 1"**: make a Basic DEXTERITY Roll.

| Result | Effect |
|--------|--------|
| Success | Move up to remaining MOVE |
| Fail | Stay in place, discard remaining MOVE |
| Critical | MOVE +2 for this action |
| Fumble | The character falls from their current position |

The character **ignores** other characters while climbing, but cannot end on another character's space.

**Important**: if a character's turn ends without being able to stand on solid ground → they fall.

---

### Charging & Disengaging

**Charging**: moving into base contact with an enemy → AoO against that enemy → lose all remaining movement from that action.

**Charging from above**: starting 3"+ vertically above the target and moving into base contact → **charging from above** → chosen weapon gains **Penetration -5** for the AoO (even when falling onto them).

**Disengaging**: leaving base contact with ≥ 1 enemy. The opponent chooses one of their characters. Opposed DEXTERITY Roll. Smaller base = **+1 DEXTERITY** (attacking or defending).

| Result | Effect |
|--------|--------|
| Success | Character moves away normally |
| Fail | Enemy makes an AoO (cannot be a Grapple) → character moves away normally |
| Critical | Move away normally +2" |
| Fumble | Enemy makes an AoO (cannot be a Grapple) → character stays in place |

*FAQ v1.3:* The disengage itself is not affected by Limited Movement, but where the character can move afterwards is.

---

### Jump — 1 AP

**Cannot jump while in water.** Pick a point in LOS, no more than 3" above the character's base. Basic DEXTERITY Roll.

| Result | Effect |
|--------|--------|
| Success | Move 2" plus up to 1" for every Ace rolled |
| Fail | Move 2" |
| Critical | Move 4" plus up to 1" for every Ace rolled |
| Fumble | Move 1" |

If the character cannot be placed on solid ground → **falls**. Fall distance calculated from the start of the jump. A player may choose to end the jump mid-air (greater distance, guaranteed fall).

**Chained Jump**: once per turn, after performing a Jump onto an Obstacle or Debris, may immediately make an additional **0 AP Jump** from that obstacle.

*FAQ v1.3:* Jumps are not affected by Limited Movement.

---

### Controlled Landing — 1 WP (declared when Jumping)

If the jump results in a fall, the character scores an Ace on **5+** instead of 7+ for the falling roll.

| DEXTERITY Result | Effect on fall |
|-----------------|---------------|
| Success | Reduce LP lost by 1 per Ace |
| Fail | Full fall effect |
| Critical | Reduce LP lost by 2 plus 1 per Ace |
| Fumble | Full fall effect + Stunned counter |

---

### Falling

**Triggered when** a character cannot be wholly placed on solid ground.

Move the character straight down until they can be placed on solid ground. Fall **> 1"** → lose LP equal to the distance in inches fallen.

**Landing Spot modifiers** (modify the effective fall distance):

| Surface | Modifier |
|---------|----------|
| Soft | -4" |
| Water | -2" |
| Solid Ground | none |
| Difficult Ground | +2" |
| Dangerous | +4" |

**Basic DEXTERITY Roll** to reduce damage:

| Result | Effect |
|--------|--------|
| Success | Reduce LP lost by 1 per Ace |
| Fail | Full effect |
| Critical | Reduce LP lost by 2 plus 1 per Ace |
| Fumble | Full effect + Stunned counter |

- Falling into water: reduce LP lost by a further 2 (cumulative with the Landing Spot modifier).
- Flight: takes 2 less Damage from falling.
- Aerial Attack: does not lose LP from falling, provided it is a charge from above.

---

### Dive — 2 AP

**The character must be in water.** Basic DEXTERITY Roll.

| Result | Effect |
|--------|--------|
| Success | Gain 1 Underwater Counter |
| Fail | No effect |
| Critical | Gain 2 Underwater Counters |
| Fumble | Lose 1 Life Point |

**Underwater Counter**: each counter = **+2 Protection**. All counters are removed when the character takes another action.

**At the start of an activation** with ≥ 1 Underwater Counter: may remove all counters and immediately move the character up to **4" per counter** (must stay in water). Water Creature: **8" per counter**.

*FAQ v1.3:* Water Creatures do lose Life Points if they have a Stunned counter and start their turn in water.

---

### Hide — 1 AP

**Conditions**: not in base contact with any enemy, not in water.

Gain a **Hidden counter** → end this character's turn.

- Enemies more than 6" away cannot draw LOS to this character (provided it is in cover from them).
- This character cannot draw LOS to any characters further than 6" away.

The counter is immediately lost if the character moves or takes another action.

---

### Guard — 1 AP

**Conditions**: not in base contact with any enemy, not in water.

Gain a **Guard counter** → end this character's turn.

When an enemy makes a Run/Climb or Jump action in this character's LOS: may discard the counter to make an AoO **at the end of the enemy's action** (or first if the enemy moves into base contact during that action).

The counter is immediately lost if the character moves or takes another action.

---

### Combat — 1 AP

Choose a weapon and an enemy in LOS within the weapon's range. **Attack Roll** (ATTACK vs target's DEXTERITY).

| Result | Effect |
|--------|--------|
| Success | Target takes 1 point of Damage for every Ace rolled |
| Fail | No effect |
| Critical | Target takes 1 point of Damage for every Ace rolled **+ loses 1 additional Life Point** |
| Fumble | Attacker loses 1 Life Point + target makes an AoO against the attacker |

**Damage → Protection Roll → LP loss.** For each 1 Damage suffered after the Protection Roll, the target loses 1 Life Point. A character **does not make a Protection Roll** if directly instructed to lose Life Points.

**Combat in Water**: a swimming character may only use weapons with the **Aquatic** ability, unless they started their action outside of water (e.g. jumping in from the canal side).

*FAQ v1.3:* Expert Offence only applies to Combat actions in base contact. Expert Marksman only applies when not in base contact.

---

### Grapple — 1 AP

Enemy in base contact. **Opposed ATTACK Roll** (7+ for an Ace). Larger base = **+1 ATTACK** (attacking or defending).

| Result | Effect |
|--------|--------|
| Success | Move the target 2" plus up to 1" for every Ace rolled |
| Fail | No effect |
| Critical | Move the target 2" plus up to 1" for every Ace rolled + **Stunned counter** |
| Fumble | Target makes a Grapple on the attacker instead, using the same dice result |

- Cannot move the target to a point higher than 1" above where they started.
- Can cause the target to fall off a building or into water (falling rules apply).
- The character performing the Grapple is ignored for all movement during the Grapple.
- A grappled character doesn't cause AoOs for moving out of or into base contact.
- Grappling a friendly character: Basic ATTACK Roll (not Opposed).

*FAQ v1.3:* Expert Offence does not apply to Grapples. Vampiric Attack does not work on Grapples or Drowns.

---

### Drown — 1 AP

Enemy in base contact **and in water**. Targets with **Water Creature** are immune. **Opposed ATTACK Roll** (7+ for an Ace). Larger base = **+1 ATTACK** (attacking or defending).

| Result | Effect |
|--------|--------|
| Success | Target loses 2 Life Points, plus 1 Life Point for every Ace rolled |
| Fail | No effect |
| Critical | Target loses 4 Life Points, plus 1 Life Point for every Ace rolled |
| Fumble | Attacker loses 2 Life Points |

**No Protection Roll against a Drown.**

---

### Cast Spell — 1 AP

→ See `rules_magic.md`

---

### Row — 1 AP

Character riding a gondola. Basic DEXTERITY Roll.

| Result | Effect |
|--------|--------|
| Success | Gondola and characters on it move 2" plus 1" for every Ace rolled |
| Fail | Gondola and characters on it move 2" |
| Critical | Gondola and characters on it move 4" plus 1" for every Ace rolled |
| Fumble | All characters on the Gondola move 1" directly into water |

A Row action cannot take the Gondola out of water, but can move it farther than the minimum distance provided characters on top do not move farther than specified.

---

## Command Points

Each command may be used **once per round per character** (max 4 CP spent/round).

| Command | Cost | Timing | Effect |
|---------|------|--------|--------|
| **PLAN** | 1 CP | Start of round | Discard an Agenda and draw another one |
| **ORDER** | 1 CP | Start of a different friendly character's turn, in LOS | That character gains +1 AP this turn (never exceeds 3 AP total) |
| **COUNTER** | 1 CP | After an enemy character completes an action (and after all AoOs) | Choose a **different** friendly character in LOS → gains 1 AP for an out of sequence action. Counts toward their 3 AP/round total (a character who has already used 3 AP cannot benefit) |
| **ABILITY** | 1 CP | At any point during the turn, not during another action | Use a Command Ability |

**Only one Command Ability** per character per turn, regardless of how many they have access to.

**Types of Command Abilities**:

- **AURA**: affects characters in range when and only when they are in range. A character in range of an Aura when they activate benefits from the bonus until the end of their action (even if they leave range during that action, including during AoOs).
- **PULSE**: immediate effect on targets in range at the time of activation.

*FAQ v1.3:* You cannot use the Counter command on a Mage to have them cast a spell they have already cast this round.

---

## Terrain

### Solid Ground

Any broadly horizontal space: streets, sloped roofs, stairs, balconies. No movement modifiers. Scenery pieces ≤ 1" high count as solid ground for Run/Climb actions.

**Difficult Ground**: rough terrain (smashed cobbles, large rocks…). Run/Climb over Difficult Ground → must make a Basic DEXTERITY Roll.

**Unstable Ground**: unstable terrain (rafts, planks, gondolas…). Recommended no larger than 4" across.

When a character jumps or falls onto Unstable Ground: all other characters on it make a Basic DEXTERITY Roll (after AoOs). If the jumping character is on a larger base than a character on the Unstable Ground, they have -1 DEXTERITY for that roll.

| Result | Effect |
|--------|--------|
| Success | No effect |
| Fail | Move the character 2" towards the nearest edge; if they move off → fall |
| Critical | The controlling player moves the character up to 2" in any direction |
| Fumble | Move the character off the nearest edge → fall |

Unstable Ground can also count as an Obstacle (e.g. a gondola). In that case, resolve all other characters' rolls first, then the character may make a Chained Jump as normal.

### Vertical Terrain

Walls, buildings over 1" tall. Characters cannot move horizontally through these pieces, but can climb them.

### Ropes & Ladders

Climbing or descending a rope, ladder, or rigging as part of a Run/Climb action: **without** making a Basic DEXTERITY Roll.

### Impassable Terrain

Cannot be moved through. Buildings cannot usually be entered.

### Ruins

Access points (doors, windows) may be moved through without penalty. Moving up or down through ruins to different floors at any point → treat the entire area as Vertical Terrain.

### Water & Canals

Canal: at least 4" wide. Moving into or out of a canal where the wall is ≤ 1" high: free, no MOVE reduction. Wall > 1": impossible even with a Dexterity roll.

**Water Access** (lowered jetties, ladders, steps): moving out of water via a Water Access point → no -2" MOVE penalty. Water Access pieces can be used to climb out of canals where the wall is higher than 1".

### Obstacles & Debris

Any terrain ≤ 3" high that is not solid ground = Obstacle. Jumping onto an Obstacle → free **0 AP Chained Jump** (once per turn).

**Small Obstacle**: too small for a character to stand on (e.g. barrel, gondola pole). Can be moved through or jumped onto, but the character cannot end its turn on one — move the shortest distance possible off the obstacle.

**Large Obstacle**: large enough for a character to stand on (e.g. fountain, stack of boxes). Follows normal rules for solid ground or Vertical Terrain as well as being an Obstacle.

**Debris**: always in water. Characters may swim freely through Debris and may climb out of the water onto Debris (like climbing out of a canal), but cannot end their turn on Debris — immediately move the character the shortest distance possible into the surrounding water.

### Barricades

**Light**: a character in base contact with a Light barricade counts as being in cover and gets +1 Protection if the attacking character is on the other side.

**Heavy**: same rule, but +2 Protection.

Moving over a barricade that has enemy characters in base contact on the other side: the moving character must test as if disengaging.

### Gondolas

Unstable Ground and Large Obstacle. Must be placed on water. **2 characters** on 30mm bases, or **1 character** on a 40mm base. Losing ≥ 3 LP in one action → falls off the gondola (move to the shortest possible distance into water). Counts as Debris for characters not riding it.

*Balance Changes v1.3:* Gondola (equipment) reduced from 15 to 11 Ducats.

---

## Building Your Gang

### Ducats

Budget agreed before the game or defined by the scenario. Recommended for one-off games: **100 Ducats**. Most scenarios use 75, 100, 125, or 150 Ducats.

### Frequency Rules

- All characters must share the same **Faction (X)** keyword
- Must always include exactly **1** character with the **Leader** keyword (unless the scenario specifies otherwise)
- Number of **Hero** characters ≤ total number of **Henchman** characters
- A character with the **Unique** keyword may only appear **once** per gang (the same character may appear in the opponent's gang, but Unique rules only apply to your own version)
- Multiple gangs: recommended only at 200+ Ducats

### Spells (at gang building)

Choose which spells your Mages know before the game. This choice is fixed for the entire game.

---

## Equipment

Purchased during gang building. Each individual piece may only be taken **once per player**. No limit on the number of different pieces.

| Equipment | Cost | Effect |
|-----------|------|--------|
| Flashbang Grenade | 1d | Once per game: when disengaging, automatically score a Critical instead of rolling |
| Bottled Courage | 2d | Once per game: re-roll a single die (not the Destiny Die) |
| Climbing Tools | 2d | Once per game: when making a Run/Climb action, automatically score a Critical instead of rolling |
| Limewater Rebreather | 2d | Once per game: when making a Dive action, automatically score a Critical instead of rolling |
| Lantern | 2d | Once per game: at the start of a round, pick a friendly character. Until the end of the round, any character within 6" (friendly or enemy) cannot claim bonuses from being in cover and loses any Hidden counters |
| Parachute | 3d | Once per game: when Falling, the Destiny Die automatically counts as a 10 |
| Gondola | 3d | Set up a Gondola in your Deployment Zone in water at the start of the game |
| Intercepted Documents | 4d | Before deploying any characters, one friendly character gains the **Infiltration** Character Ability |
| Carnevale Mask | 4d | Once per game: at the start of an enemy character's turn, pick a friendly character not in base contact with any enemy — that character cannot be attacked in any way (Combat, Drown, Magic Spells, etc.) for that enemy character's turn |
| Poison | 5d | Once per game: before rolling for a Combat action, the chosen weapon gains the **Poisoned** ability for that attack |
| Leather Undershirt | 10d | Once per game: when a friendly character has taken Damage, and before Protection Rolls, roll 1 die and subtract that many points from the Damage received |

---

## Scenarios

### Recommended Terrain

Rule of thirds: **1/3 water, 1/3 ground level, 1/3 elevation (buildings)**. Standard board: 3'×3'. Ensure every vertical surface has a landing spot every 6–8" so characters can stand on buildings.

**This is a standing analytical constraint for all model and spell evaluation:**
- Water is present in every game — water-dependent spells and abilities (swimming, drowning, Ice Lock, Waves of Force, Fast Swimmer, Water Creature) are always relevant, not situational.
- Elevation is present in every game — Flight, Ethereal, and jumping mechanics (Dexterity roll) affect every game. Models that interact with elevation freely have consistent value.
- Natural chokepoints form at the junctions between water, ground, and elevation — zone denial spells (Abyssal Mist, Groundsnap, Ice Lock) and movement spells (Walk Between Worlds, Gateway, Cantrip of the Chariot) are stronger than they appear on a flat-board reading.
- Dexterity is not just a melee defence stat — it also determines jump rolls, which come up frequently on elevation-heavy boards.

### Setup

1. Choose scenario (+ attacker/defender roles if applicable)
2. Build gang, choose spells
3. Place scenery (alternate placement recommended if not specified)
4. Place Objectives and draw Agendas
5. Roll-off → highest chooses Deployment Zone and deploys → next highest → etc.

**Deployment**: within the Deployment Zone, no higher or lower than 3" above or below ground level, not in water (unless specified). At least 4" away from enemy characters.

### Objectives

30mm round markers. Placed after terrain, before deployment. At least **4" away from Deployment Zones** and **4" away from each other** (unless specified). May be placed in water or above ground level. Usually placed alternately.

**Scoring**: having a friendly character within 3" at the end of the game, with no enemy characters also within 3" (unless scenario specifies otherwise).

**Objective Types**:

- **Claimable**: can be claimed by different gangs. Note which gang claimed it. Unless stated otherwise, scores VP for the gang that claimed it at the end of the game, regardless of characters' distance from it.
- **Destructible**: 1 AP while in base contact = remove from the game.
- **Hidden**: placed face down. A character ending its turn in base contact with the Objective and not in base contact with an enemy character can reveal it.
- **Mobile**: can be picked up and carried. To pick up: end turn in base contact, not in base contact with an enemy. The carrier can only make **Run/Climb actions**. Drops the objective if: loses ≥ 3 LP in one action, is removed from the game, or is affected by certain spells (e.g. Gateway). Pickpocket automatically takes a Mobile Objective from an enemy character upon successfully disengaging.

*FAQ v1.3:* **Mindless** characters can interact with Objectives normally (pick up, claim, reveal, destroy) but are ignored when scoring Victory Points for Primary Objectives at the end of the game. They can still score VP through Agendas, killing enemies, or surviving.

### Agendas

Secondary objectives drawn randomly. Check at the **end of each game round**.

**Agenda Rules**:

| Rule | Effect |
|------|--------|
| **Cycle** | When you score an Agenda, immediately draw another one |
| **Double** | Rather than scoring VP immediately, keep the Agenda in play; if achieved again = double VP; if not = 0 VP. May only be kept in play once |
| **Secret** | Keep your Agendas secret from opponents until achieved |
| **Secondary** | Must achieve at least one Agenda to score any Victory Points from any source in the game |
| **Total** | Must achieve all Agendas to score VP for them (may still score the Primary Objective) |

### Duration

Defined by the scenario. At the end of the last round → tally VP → determine winner.

---

## Order of Play

**Setup:**
1. Scenario + roles
2. Gang + spells
3. Scenery
4. Objectives + Agendas
5. Deployment (roll-off, highest to lowest)

**Round:**
1. Initiative (roll current CP, highest wins)
2. Player with initiative activates one character (up to 3 AP)
3. Take turns clockwise until all characters have activated
4. End of Round: resolve end-of-round effects, check Agendas
5. New round begins (back to step 1) if game is not over

**End of Game:** at the end of the final round → tally VP → determine winner.

---

## Fortune's Favour (After Party)

Optional narrative rule. The first player to perform a particularly daring feat may be awarded Fortune's Favour by their opponent (consensus in multiplayer).

The character that performed the feat replenishes **1 Will Point** (or **2 Will Points** if the player can tell the story of the heroics). Cannot exceed starting value.

Fortune's Favour can then be passed to any other character who performs a further worthy feat. Winning while holding Fortune's Favour = questionable victory.

---

## Miscellaneous Rules

**Damage vs. losing Life Points**: when a character "takes Damage" → Protection Roll possible. When directly instructed to "lose Life Points" (drowning, spells…) → no Protection Roll.

**Removed from the game**: at 0 LP. Counts as "killed" for VP and related rules.

**Friendly fire**: characters in your gang are "friendly characters"; all opposing gangs have "enemy characters". It is possible to attack your own allies (but friendly/enemy ability rules apply normally).

**FAQ v1.3 — Stacking**: special rules with (X) stack up to a maximum of **3**. If a character with Expert Offence (2) would gain another Expert Offence (2), they end up with Expert Offence (3). If a rule would grant a value above 3, only the highest value is used. Stats, however, can stack up to 10.
