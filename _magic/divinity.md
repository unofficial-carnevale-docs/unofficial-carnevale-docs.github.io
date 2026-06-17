---
title: Divinity
is_discipline: true
nav_order: 11
---

## Per-Spell Evaluation

| Spell | Cost | Diff | Range | Target | Type | Output | Timing | Restrictions | FF |
|---|---|---|---|---|---|---|---|---|---|
| Cantrip of the Sun | 0 | 7 | 6" | S | Heal + Util | F | Now | Friendly only | N |
| Protection of the Eye | 1 | 5 | 6" | S | Buff | F | Now | Friendly only | N |
| Eldritch Armour | 1 | 6 | 6" | S | Buff | F | Now | Friendly only | N |
| Rejuvenation | 1 | 7 | 12" | M | Heal | Sc | Now | Friendly; free distribution | N |
| Holy Light | 1 | 8 | 6" AoE | T | LP + Debuff | F | Now | Enemy Mages only | N |
| Defender of Destiny | 1 | 8 | 6" AoE | M | Buff | F | Now | Friendly only; lasts end of round | N |
| Aqua Curitiva | 2 | 8 | 6" | T | Heal + Debuff | F | EoR | Friendly must hold position | N |

### Cantrip of the Sun

Pick one friendly character in line of sight within 6". That character replenishes **1 Life Point** and **1 Will Point**.

<div class="callout" markdown="1">
The only cantrip that recovers WP — net 0 WP + 1 AP for +1 LP and a WP top-up. A fumble here is especially costly (Stun + WP loss on a WP-recovery spell). Diff 7 (87% at MIND 4). Scarcity: WP recovery on a cantrip is unique in the game. Replaceability: nothing else provides this at 0 WP.
</div>

### Protection of the Eye

Pick one friendly character in line of sight within 6". That character gains **Universal Shielding (X)+3** until the end of its next turn.

<div class="callout" markdown="1">
Grants Universal Shielding (X+3 = 5 at Mage 2), but US is **not** flat Protection. Per rules_abilities.md it sets a *minimum* Protection floor, **capped at the target's starting Protection**, that only activates when an attacker's Penetration would drop effective Protection below that floor. So this is **anti-Penetration insurance, not a general durability buff**: against a no-Penetration attacker on a model already at its starting Protection it contributes **zero**, and the "5" ceiling is only reachable on models whose starting Protection is ≥5. Value is high specifically against Penetration-heavy threats (Blood Rites spells, post–Sunder Armour alpha strikes); low otherwise. Diff 5 (97% at MIND 4) makes it reliable to land — just deploy it against the right threat. Scarcity: Universal Shielding as a granted ability is unique to this spell.
</div>

### Eldritch Armour

Pick one friendly character in line of sight within 6". That character gains +(X) PROTECTION until the end of its next turn.

<div class="callout" markdown="1">
+2 Protection = +0.8 expected damage reduction per attack (at the median recipient: +2 Protection ≈ +0.8 LP saved per attack, capped by incoming damage). Stacking cap of 3 limits extremes. Simpler math than Protection of the Eye but often slightly weaker. Scarcity: +Protection buff also achievable via equipment; not unique. Replaceability: partial.
</div>

### Rejuvenation

Total up every **Ace** rolled plus (X). Replenish this many **Life Points** in total from any number of characters within 12" in line of sight, distributing the amount between the characters as you wish.

<div class="callout" markdown="1">
The most flexible healing spell in the game — freely distribute across any number of LOS friendlies within 12". Dice-scaling output (Aces+2 at Mage 2): MIND matters significantly. WP economy: Diff 7 (87%) is moderate risk. AP impact: neutral but the 12" safe range means the caster is never in danger. Scarcity: free-distribution multi-target healing is unique.
</div>

### Holy Light

All enemy characters with the **Mage** ability within 6" receive a **Stunned** counter and lose (X) **Life Points**.

<div class="callout" markdown="1">
Binary value — exceptional vs magic gangs (2 LP loss + Stun on every enemy Mage in 6" AoE, LP bypasses Protection), zero value vs non-magic gangs. Stun denies entire activations. Diff 8 (76%) is a real cost. AP impact: Stunning 2 enemy Mages = denying ~6 AP worth of activations — potentially the highest AP swing in the game. Scarcity: the only anti-Mage AoE in the game. Replaceability: completely irreplaceable.
</div>

### Defender of Destiny

All friendly characters within 6" gain **Parry (X)** and **Expert Protection (X)** until the end of the round.

<div class="callout" markdown="1">
All friendlies within 6" gain Parry(2) + Expert Protection(2) until end of round (longer duration than most buffs). AoE delivery multiplies value when 2+ friendly models are in range. Diff 8 is the barrier — best committed before the opponent's key attacker activates. Scarcity: multi-model Parry + ExProt AoE is unique; Glimpse of Glory offers both but single-target only.
</div>

### Aqua Curitiva

Pick one friendly character in line of sight within 6". Place the **Blast** marker under this character. At the end of the round, any friendly characters at least partially over the **Blast** marker replenish **(X)+2 Life Points**. Any enemy characters at least partially over the **Blast** marker receive a **Stunned** counter. Then remove the **Blast** marker.

<div class="callout" markdown="1">
Diff 8 + 2 WP is the most expensive investment in Divinity. The 4 LP heal is the highest single-event heal in the game, but end-of-round timing means the healed model can die before resolution, and enemies can leave the Stun zone freely. Best in static defensive situations. AP impact: Stun on enemy is AP denial but easily countered by movement. Treat end-of-round timing as a significant penalty to stated value.
</div>
