---
title: Distance and Jumps
nav_order: 0
is_ref: true
toc:
  - title: TL;DR
    anchor: tldr
  - title: Measuring Distances
    anchor: measuring-distances
  - title: The Jump Action
    anchor: the-jump-action
  - title: Jump Distance Table
    anchor: jump-distance-table
  - title: Minimum Jump to Cross a Gap
    anchor: minimum-jump-to-cross-a-gap
  - title: Expected Jump Distance
    anchor: expected-jump-distance
---

## TL;DR

Expected horizontal gap a model can clear on a flat jump (average outcome, no Acrobatic):

| DEX | 30mm base | 40mm base | 50mm base | 75mm base |
|:---:|:---------:|:---------:|:---------:|:---------:|
| 3   | 3.1"      | 2.7"      | 2.3"      | 1.3"      |
| 4   | 3.6"      | 3.2"      | 2.8"      | 1.8"      |
| 5   | 4.0"      | 3.6"      | 3.2"      | 2.2"      |

The first point of **Acrobatic** adds roughly **+0.4"** to the expected gap (less for each further point).

Height reduces the clearable horizontal gap (DEX 4 reference, penalty grows nonlinearly):

| Target height | Horizontal gap lost |
|:-------------:|:-------------------:|
| 1"            | −0.1"               |
| 2"            | −0.6"               |
| 3"            | −1.5"               |

**Example.** A DEX 4 model on a 30mm base can on average clear a **3.6" flat gap**. Against a 3" tall building, that same model can reach the top from **2.1" away** on average.

[Open the Jump Calculator →](/tools/#jump)

## Measuring Distances

All distances in Carnevale are measured in a straight line between the two closest points of the objects involved. This line can go in any direction: horizontal, vertical, or diagonal. There is no top-down projection.

The diagonal rule has a direct consequence for jumps: reaching a raised surface costs more distance than its horizontal gap suggests, because the straight line climbs at an angle.

## The Jump Action

**Cost:** 1 AP. A character cannot jump while in water.

Pick a target point within line of sight that is **no higher than 3" above the character's base**. Make a Basic **Dexterity** roll:

| Result | Effect |
|---|---|
| Critical | 4" + up to 1" per Ace rolled |
| Success | 2" + up to 1" per Ace rolled |
| Fail | 2" |
| Fumble | 1" |
{: .outcome}

The character moves in a straight line toward the nominated point. This line can pass over intervening terrain that is **less than 1" high**.

**Partial landing.** If only part of the base lands on solid ground, the character may be nudged up to 1" further along the jump line to reach full support.

**Failing to land.** If the character cannot be wholly placed on solid ground, it falls. Fall distance is measured from the height at the **start of the jump**, not the start of the fall.

**Overshooting.** If the rolled distance exceeds the distance to the target point, the remaining distance may be used **as a Run/Climb action** along the same line.

<div class="callout">
<p class="callout-title">FAQ</p>

**Does a Jump require the character to start on solid ground?** No. A character could climb a wall partway and then jump across to a balcony.

**Can I Jump while carrying an Objective?** No. Only Run/Climb actions (including climbing) are allowed.

**If a character fails its jump and falls onto something higher than ground level, how far do they fall?** The distance fallen is measured from the start of the jump to wherever the character lands. Landing on a market stall rather than the ground reduces the damage taken.

</div>

## Jump Distance Table

The table below shows the effective straight-line distance needed to reach a surface at a given height and horizontal gap. Formula: distance = √(horizontal² + height²).

| Horizontal gap | Height 1" | Height 2" | Height 3" |
|:--------------:|:---------:|:---------:|:---------:|
| 1" | 1.41" | 2.24" | 3.16" |
| 2" | 2.24" | 2.83" | 3.61" |
| 3" | 3.16" | 3.61" | 4.24" |
| 4" | 4.12" | 4.47" | 5.00" |
| 5" | 5.10" | 5.39" | 5.83" |
| 6" | 6.08" | 6.32" | 6.71" |

**Reading the table:** A 2" tall building with a 1" horizontal gap requires 2.24" of jump distance. A Fail (2") falls short. A Success with at least 1 Ace reaches up to 3", which is sufficient. Targets higher than 3" above the character's base are not legal jump destinations.

## Minimum Jump to Cross a Gap

The Jump Distance Table gives the straight-line distance to the **near edge** of the target surface. But a model's base must land **fully** on that surface. The 1" nudge helps, but larger bases need more overshoot to finish supported.

The minimum jump roll needed to fully land (including the nudge) is:

**minimum jump = straight-line distance to near edge + base diameter in inches − 1"**

| Base size | Extra distance needed over the gap |
|:---------:|:----------------------------------:|
| 30mm | +0.2" |
| 40mm | +0.6" |
| 50mm | +1.0" |
| 60mm | +1.4" |
| 75mm | +2.0" |

These overheads apply regardless of whether the jump is flat or elevated. For elevated targets, look up the straight-line distance in the Jump Distance Table and add the overhead from here.

**Example.** A 40mm model jumping to a 2" tall building 1" away needs 2.24" (from the table) + 0.6" = **2.84"** total. A Fail (2") falls short. A Success with 1 Ace (up to 3") just clears it.

## Expected Jump Distance

The table below shows the average distance covered by a jump, by DEX value and **Acrobatic (X)** level. All values include the full effect of Criticals (4" base), Fails (fixed 2"), and Fumbles (1"), weighted by their probability. Values assume the player always uses all available Aces and re-rolls failed non-Destiny dice with Acrobatic.

| DEX | No Acrobatic | Acrobatic (1) | Acrobatic (2) | Acrobatic (3) |
|:---:|:------------:|:-------------:|:-------------:|:-------------:|
| 1   | 2.30"        | 2.30"         | 2.30"         | 2.30"         |
| 2   | 2.82"        | 3.13"         | 3.13"         | 3.13"         |
| 3   | 3.29"        | 3.67"         | 3.84"         | 3.84"         |
| 4   | 3.74"        | 4.14"         | 4.41"         | 4.51"         |
| 5   | 4.16"        | 4.57"         | 4.90"         | 5.10"         |
| 6   | 4.58"        | 4.98"         | 5.35"         | 5.63"         |
| 7   | 4.99"        | 5.39"         | 5.78"         | 6.11"         |
| 8   | 5.39"        | 5.79"         | 6.19"         | 6.55"         |

**The first point of Acrobatic adds roughly 0.40" to the expected distance** at DEX 4 and above, tapering to +0.31" at DEX 2 where only one die can be re-rolled. The driver is that you re-roll a die that has **already failed**, so the re-roll lands an Ace 40% of the time (each Ace is worth ~1"), and at typical DEX you almost always have a failed die to spend it on. A re-rolled Ace can also flip a Success into a Critical when the Destiny die is a 10, which lifts the average a touch. Further points of Acrobatic see steep diminishing returns (the second adds only +0.17" at DEX 3 up to +0.39" at DEX 8) as the supply of failed dice runs out.
