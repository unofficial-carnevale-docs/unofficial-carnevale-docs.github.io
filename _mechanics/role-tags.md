---
title: Role Tags
nav_order: 1
is_analysis: true
---

## Why tag models?

To be able to compare models, we tried to give them Tags to group them by role. These tags were validated by ensuring their computed capability doesn't sit far from their role's standard.

## Conventions

- **Adjectives** refine a role in parentheses: `Damage Dealer (melee, anti-armor)`, `Canal Fighter
  (drown)`. They describe sub-role / target-preference, not a separate role.
- **Dual tags** read `A / B`, primary first.
- **Scoring bucket** (how the capability model judges a model):
  - **Offense:** scored on EDPA vs the role's own baseline: Damage Dealer, Brawler, Assassin, Canal Fighter, Sniper (**alpha** only), Line Fighter (own lower bar).
  - **Defense:** scored on ATK2K survivability: Tank.
  - **Utility:** low EDPA is expected, not a failing: Support, Control, Objective Runner, Disruptor, Harasser, Specialist.

| Role | Bucket | One-line |
|---|---|---|
| Assassin | Offense | Mobile with the kill power to remove a chosen key target. |
| Brawler | Offense | Aggressive, durable-ish melee with high sustained output. |
| Canal Fighter | Offense | Combat effectiveness tied to water. |
| Control | Utility | Hard CC: Stun, Grapple-lock, forced movement, area denial. |
| Damage Dealer | Offense | Primary job is dealing damage (melee / ranged / magic). |
| Disruptor | Utility | Suppresses the enemy Will Point economy. |
| Harasser | Utility | Fast, disrupts rather than kills. |
| Line Fighter | Offense (low) | Rank-and-file frontline melee, holds the line. |
| Objective Runner | Utility | Fast model that grabs / contests / scores objectives (incl. Pickpocket theft). |
| Sniper | Offense (alpha) | Long-range, Reload-gated, trades sustained EDPA for range + burst. |
| Specialist | Utility | Unique-mechanic models that fit no standard role. |
| Support | Utility | Buffs / heals / enables allies (mages, auras, WP batteries). |
| Tank | Defense | Soaks damage and protects. Survivability is the point, not output. |

## Roles

### Assassin

Mobile model with the **kill power** to remove a chosen high-value target (alpha strike on a target).

- **Include:** fast/infiltrating models with the punch to actually kill a key piece.
- **Exclude:** fast models that *can't* reliably kill and exist to tie up/disrupt (Harasser). The
  Assassin/Harasser line is kill power. Fast scorers (Objective Runner).

### Brawler

Aggressive melee with high sustained output and enough bulk to stay in the fight (vs a glass-cannon Damage Dealer).

- **Include:** front-line melee with above-curve EDPA and survivability for its cost.
- **Exclude:** ranged/magic output (Damage Dealer), water-bound melee (Canal Fighter).

### Canal Fighter

Combat effectiveness **tied to water**: fights in/from water (Water Creature and/or Aquatic weapon) or
is slow/weak on land and built for the canals.

- **Include:** Water Creatures, strong amphibians in water-poor factions, Drown/water-control
  specialists. For Rashaar, as water is the faction baseline, only the standouts are tagged.
- **Exclude:** Fast-Swimmer-*bonus*-only models that fight fine on land (water is optional, not
  defining).
- **Adjective rule:** members from a Damage-Dealer/Brawler origin = clean `Canal Fighter`. Members from
  any other role carry a function adjective: `(drown)`, `(pull)`, `(grappler)`, `(ranged)`, `(tank)`,
  `(mage, support)`.

### Control

Hard crowd-control: Stun, Grapple-lock, forced movement, impassable/area denial.

- **Include:** models built to lock down or reposition enemies via abilities/spells.
- **Exclude:** soft mobility-nuisance (Harasser), WP/resource denial (Disruptor).

### Damage Dealer

Primary job is dealing damage. The default offense role.

- **Include:** melee, ranged, or magic dealers. Adjectives carry the flavour: `(melee)`, `(ranged)`,
  `(magic, <discipline>)`, `(anti-armor)`, `(Stun)`, `(anti-large)`.
- **Exclude:** water-bound dealers (Canal Fighter), long-range Reload shooters whose value is the
  alpha (Sniper), models that can't reliably kill and exist to annoy (Harasser).
- **Note (mages):** a mage's EDPA assumes its *best damage spell*. A support mage usually spends slots
  on buffs/heals, so high EDPA ≠ "is a dealer".

### Disruptor

Suppresses the enemy **Will Point economy**, by either **lockout** (preventing WP use: "(may) not use
Will Points", aura or base contact) or **strip/drain** (removing WP: "loses X WP", WP "wasted").

- **Include:** WP-lockout auras / contact (Exorcist, Black Lamp, Ghoul, Strigoi Priest, Witch Finder,
  Sepulchral Vanguard), WP strip-on-hit / drain (Eater of Sin, Fate).
- **Exclude:**
  - *Exploiting* a WP-0 state: bonus damage or re-rolls vs depleted targets (Exorcist's "+3 Dmg vs
    0-WP", Thomas Thieme's re-roll). That's a payoff, not denial.
  - *Incidental* WP-strip riders: **Pickpocket** (lose 1 WP on disengage).
  - *Dispel-only / dispel-buff* with no WP denial (Strigoi Jude's Judgement buffs allies' dispel only).
  - *Too situational* denial (Throne, Harlequin: conditional / 50% proc).

### Harasser

A fast model that **disrupts the enemy rather than kills it**: tie up, screen, bait, block, pin the
backline/support via mobility and nuisance, with **low kill power** (not an Assassin) and not hard CC
(not Control).

- **Include:** fast, cheap/expendable disruptors (Move ≥5 or Flight/Acrobatic/Slippery/Infiltration/
  Engage), often Mindless (can't score: pure disruptor). An **expensive** model qualifies only if it
  harasses with **high efficiency** (strong mobility + a real disruption tool, e.g. Harlequin's
  Slippery + Mischievous WP-negate, whose sword is too soft to assassinate at its cost).
  Adjective `(aquatic)` for a water-based harasser (Leech).
- **Exclude:** real killers (high EDPA: Assassin/Damage Dealer/Brawler), pure scorers/pickpockets (Objective
  Runner), hard-CC (Control), too-fragile bait pieces, models whose primary role is resource/support,
  models too slow to harass, defensive disengage tricks that aren't enemy nuisance (e.g. Confusing Exit).

### Line Fighter

Rank-and-file frontline melee, holds your line, moderate output, not an elite dealer.

- **Include:** vanilla frontline combatants between Brawler and cheap filler.
- **Exclude:** a Line Fighter whose EDPA exceeds the Damage Dealer median is arguably a dealer.

### Objective Runner

Fast/mobile model whose job is to grab, contest, and score objectives, including Pickpocket theft
(steal WP + objectives on disengage).

- **Include:** mobile scorers and pickpocket thieves whose primary value is theft/scoring.
- **Exclude:** Mindless models (can't score Primary Objectives). If fast + low-output they lean
  Harasser. Fast killers (Assassin).

### Sniper

Long-range shooter with high single-shot **alpha**, Reload-gated, low sustained EDPA by design (range and
burst are the trade). Scored on alpha, not EDPA.

- **Include:** dedicated long-range gunners.
- **Exclude:** mid-range or rapid shooters that sustain fire (Damage Dealer (ranged)).

### Specialist

Catch-all for unique-mechanic models that fit no standard role.

- **Include:** Mask-givers, spawners/summoners, gondola/transport, adaptive/copy models, Emissary
  tentacles, Artifact carriers, Destiny-Die control, and other irreplaceable niche tech.
- **Exclude:** anything that fits other tags.

### Support

Buffs, heals, or enables allies: mages (buff/heal disciplines), auras, Companions, WP batteries.

- **Include:** dedicated enablers and WP-battery / Nexus-style models. A support mage tagged Support whose EDPA exceeds the Damage Dealer median is still Support
  if it would spend its slots on buffs/heals.
- **Exclude:** models that actively deny *enemy* resources (Disruptor).

### Tank

Survivability is the role. High ATK2K (LP × Protection × Parry/Shielding), plants, blocks, bodyguards.

- **Include:** durable blockers, Bodyguards, high-Protection/Shielding anchors with modest offense.
- **Exclude:** durable models whose *point* is output (Brawler) or water (Canal Fighter). A Tank with ATK2K below ~80% of the Tank median is a "soft tank".
