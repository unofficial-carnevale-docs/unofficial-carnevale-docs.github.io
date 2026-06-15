---
title: "Offense & Defense Modifiers"
nav_order: 2
prev_doc:
  title: Will Points
  url: /mechanics/will-points/
next_doc:
  title: Combat Capabilities
  url: /mechanics/combat/
---

Relative value of every offense and defense lever, normalized so they can be compared head-to-head. Derived from the dice math in [rules_abilities.md](rules_abilities.md), `rules_core_gameplay.md`, and the model framework.

## How to Read This

All figures use the reference engagement unless stated:

- **Attacker:** Attack 4
- **Defender:** Dexterity 4 (→ P(Ace) per attack die = 0.7), Protection 3, LP 12
- Values are **per single Combat attack** and given **before the Protection roll** (raw expected Damage added or saved). X = the ability's value (X=1 unless noted).
- "Ceiling" = whether the lever raises the **maximum** possible Damage of one attack.
- Recall: one die in every pool is the **Destiny die** — it counts toward Aces but **can never be re-rolled**, so re-roll abilities only ever touch **(stat − 1)** dice.

P(Ace) per attack die by target Dexterity: Dex 3 = 0.8 · Dex 4 = 0.7 · Dex 5 = 0.6 · Dex 6 = 0.5 · Dex 7 = 0.4.

---

## Offense Levers

Expected bonus Damage per Combat attack vs the reference Dex 4 target:

| Lever | X=1 | X=2 | Raises ceiling? | Improves to-hit / reliability? | Conditional on | Other actions helped |
|-------|-----|-----|-----------------|--------------------------------|----------------|----------------------|
| **+X Damage** (flat on hit) | **+0.99** | **+1.98** | Yes (+X) | No | landing ≥1 Ace (× P(hit)) | Combat only |
| **+X Attack** (extra dice) | +0.70 | +1.40 | Yes (+X) | Yes (more dice → higher P(hit)) | — | also **Grapple / Drown** |
| **−X Evasion** (weapon to-hit mod) | +0.40 | +0.80 | No | Yes (raises P(hit)) | — | Combat only |
| **Expert Offence / Marksman (X)** (re-roll failed dice) | +0.46 | +0.61 | **No** (capped at Attack dice) | **Yes — best** (lowest whiff, tightest spread) | a die having failed | Combat only (not Grapple/Drown) |
| **Penetration −X** | +0.40 vs armour | +0.80 vs armour | No | No | target having Protection (**0 vs unarmoured**) | Combat only |
| **Fear (X)** (re-roll all failures on trigger) | +0.14¹ | — | No | Yes (when it triggers) | target failing a MIND roll (`0.6^MIND`); negated by **Brave** | Combat only |
| **Poisoned** (extra LP on a damaging hit) | +1.8 to +3.6² | — | effectively (bonus LP) | No | first dealing ≥1 LP; **bypasses Protection** | Combat only |

¹ Fear(0) vs a MIND 3 target: 21.6% trigger × ~0.63 Aces from re-rolling all failures = **+0.14** avg. Rises sharply vs low-MIND targets (eff. MIND 1 → 60% trigger → +0.38) and is **zero vs Brave**.
² Poisoned: 60% trigger × extra LP by base size (30mm 3 → +1.8; 40mm 4 → +2.4; 50mm 5 → +3.0; 60mm+ 6 → +3.6), conditional on the hit already dealing ≥1 LP. Direct LP loss, no Protection Roll.

Formulas (vs a target with per-die hit chance `p`):

- **+X Damage:** `+X × P(hit)` = `X × (1 − (1−p)^Attack)`. ≈ `+X` for Attack 3+ vs Dex ≤5.
- **+X Attack:** `+X × p`.
- **−X Evasion (weapon):** the modifier is added to the target's **effective Dexterity** for the Attack Roll. A **negative** value lowers their effective Dexterity → `+0.1 per point` P(Ace) per die → `+ Attack × 0.1 × X` expected Damage. A **positive** Evasion modifier is the reverse — a to-hit *penalty* (the trade heavy two-handers pay for high Dmg/Pen). Exact mirror of the defensive +X Dexterity lever.
- **Expert Off/Marks(X):** `+ E[min(X, failures)] × p`, failures ~ Binomial(**Attack − 1**, 1−p). Always below `X × p`; EO(3) barely beats EO(2) on a small pool.
- **Penetration −X:** `+ min(X, Protection) × 0.4`. Zero against Protection 0.
- **Fear(X):** `P(trigger) × (Attack − 1)(1−p)p`, where `P(trigger) = 0.6^max(1, target MIND + X)`. The re-roll is **uncapped** (all failures, not X), so the *conditional* swing is large but the *average* is throttled by the trigger rate. Brave auto-passes the MIND roll.
- **Poisoned:** `P(deal ≥1 LP) × 0.6 × baseLP`, baseLP = 3 / 4 / 5 / 6 by 30 / 40 / 50 / 60mm+ base. Armour-independent and **scales up against bigger (usually tougher) targets**.

### Offense rules of thumb

1. **+X Damage is the highest *average* output boost** — and it also raises the ceiling. Best on any model that reliably lands hits (Attack 3+ vs Dex ≤5). Its only weaknesses: it does nothing on a whiff (its value is multiplied by P(hit), which collapses vs high-Dex targets or low Attack), and a flat bonus is wasted as overkill on a hit that already kills.
2. **+X Attack is the most *versatile* boost** — raises average, ceiling, AND reliability (more dice = more likely to land), and is the **only damage lever that also powers Grapple and Drown**. It scales up against soft, low-Dexterity targets (every die is likely to hit) and down against evasive ones.
3. **Expert Offence / Marksman is the *most reliable* but lowest-output boost** — it converts near-misses, giving the lowest whiff rate and tightest damage spread, but it can **never exceed your Attack dice** (no ceiling gain). Its relative value **rises as targets get harder to hit** and it overtakes +X Attack around Dex 7. Worthless dead weight if you are missing for other reasons or attacking via Grapple/Drown.
4. **Penetration is *conditional* damage** — the only offense lever whose value **rises with the enemy's Protection** (~+0.4 per point, up to their Protection value) and **falls to zero against unarmoured targets**. Pair it with a hit you want to push through armour, not as a general boost.
5. **−X Evasion is "accuracy as a weapon stat"** — the offensive mirror of +Dexterity, raising hit chance ~0.1 per point (≈ +0.4 Damage at Attack 4). **Mind the sign:** a *positive* Evasion modifier is the accuracy *penalty* that heavy, high-Damage weapons (Zweihänder, Flail, claymores) pay — read the weapon line accordingly. Worth most against evasive (high-Dex) targets, where each point of hit chance is scarcest.
6. **Fear is a low-average, high-variance accuracy rider, not a damage staple** — on a trigger it re-rolls *all* your missed attack dice (a bigger swing than Expert Offence), but the trigger rate collapses against MIND 3+ targets (≈22%) and is zero against Brave. It is a conditional damage bonus that pays off against low-MIND gangs — **not** a control effect (it does nothing to the target's movement, actions, or status; it only helps your own attack land).
7. **Poisoned is the strongest offensive rider here — when the hit lands.** The extra LP bypasses Protection entirely, triggers 60% of the time, and **scales with the target's base size** (+1.8 vs 30mm up to +3.6 vs 60mm+), making it anti-tank / anti-monster. The catch: it is gated on the attack first dealing ≥1 LP, so pair it with reliable to-hit and Penetration — a poisoned weapon that can't break armour does nothing.

### When the offense ranking flips

| Situation | Best pick | Why |
|-----------|-----------|-----|
| Reliable hitter vs average target | **+X Damage** | highest average, raises ceiling |
| Soft / low-Dex target, or you also Grapple/Drown | **+X Attack** | scales with low Dex, helps all Attack actions |
| Evasive (Dex 6+) target, or you need consistency | **−X Evasion / Expert Off/Marks** | both buy scarce hit chance; re-rolls worth most when Aces are rare |
| Heavily armoured target | **Penetration** (then +X Damage) | only lever that beats Protection |
| Unarmoured target | **+X Damage / +X Attack** | Penetration does nothing here |
| Large-base / monster / tank target | **Poisoned** | extra LP scales with base size and ignores armour |
| Low-MIND swarm | **Fear** | high trigger rate → frequent re-rolls of your own missed attack dice |
| High-MIND or Brave target | **avoid relying on Fear** | trigger rate near zero / negated entirely |

---

## Defense Levers

Expected LP saved per incoming reference attack (Attack 4), or raw durability:

| Lever | Value (per attack / total) | Penetration-proof? | Helps vs Drown & direct LP loss? | Reliability | Conditional on |
|-------|----------------------------|--------------------|----------------------------------|-------------|----------------|
| **+X LP** | +X effective HP, banked | **Yes** | **Yes — the only one** | **Highest** (no roll) | nothing — never wasted |
| **+X Dexterity** | −(Attacker Attack × 0.1) Damage per attack (≈ −0.4 at Atk 4) | **Yes** | No (Grapple/Drown use Attack, not Dex) | High | being attacked via Combat |
| **+X Protection** (extra dice) | +0.40 saved per Damage (≈ +0.4/attack) | No | No | Medium (rolled) | incoming Damage; degraded by Pen |
| **Expert Protection (X)** (re-roll) | +0.34 (X=1) / +0.48 (X=2) at Prot 3 | No | No | Higher than raw Prot | same as Protection |
| **Universal Shielding (X)** | anti-Pen floor only, capped at starting Prot | it *is* the Pen counter | No | Situational | enemy Penetration present |
| **Parry (X)** (force re-roll of Aces) | removes ≈ X × (1−p) hits (Dex 4: ~X×0.3; Dex 6: ~X×0.5) | **Yes** (pre-Damage) | No | Scales with attacker quality | attacker landing Aces |

Formulas:

- **+X Dexterity:** lowers every attacker's per-die hit chance by 0.1 per +1 → saves `Attacker_Attack × 0.1 × X` Damage per attack. Scales with the **attacker's** Attack.
- **+X Protection:** `+ X × 0.4` LP saved per Damage, **capped at the incoming Damage** (floored at 0) and reduced point-for-point by enemy **Penetration**.
- **Expert Protection(X):** `+ E[min(X, failures)] × 0.4`, failures ~ Binomial(**Prot − 1**, 0.6); same Pen vulnerability and Damage cap.
- **Parry(X):** forces the attacker to re-roll up to X of their successful Aces → removes `E[min(X, attacker Aces)] × (1 − p)` hits, where `p = (11 − your Dex)/10`. **Stronger the higher your own Dexterity.**

### Defense rules of thumb

1. **+X LP is the only *universal* defence** — unconditional, un-rollable, immune to Penetration, and **the only lever that helps against Drowns and direct LP-loss** (spells like Mother Hydra's Claws, Holy Light, Blood Drain bypass Protection entirely). Never wasted. Treat it as the survivability floor; everything else is situational on top.
2. **+X Dexterity is the best defence against *elite* attackers** — it cuts hits at the source (Attack × 0.1 per point), so it also suppresses their Criticals, Damage+ triggers, and Penetration, and **cannot be penetrated**. It scales with the attacker's Attack, and doubles as mobility (jumps, climbs, disengaging). Useless against Grapple, Drown, and direct LP loss.
3. **+X Protection / Expert Protection is best against *volume* of medium hits with low Penetration** — but it is rolled (variance), **wasted against Drown / LP-loss**, **capped by the incoming Damage** (poor against many tiny hits), and **degrades fastest under Penetration** (Blood Rites, Sunder Armour). Expert Protection is the lower-variance version of the same thing.
4. **Universal Shielding is pure anti-Penetration insurance** — a minimum-Protection floor capped at the model's starting Protection, contributing **zero** against a no-Penetration attacker. Rate it only in Penetration-heavy matchups.
5. **Parry is anti-elite** — it deletes the strongest attacker's best Aces before Damage, is Penetration-proof, and **scales with both the attacker's quality and your own Dexterity** (Parry + high Dex compound). Weak against swarms of low-Attack models, who land few Aces to parry.

### When the defense ranking flips

| Threat | Best pick | Why |
|--------|-----------|-----|
| Drowns, or direct LP-loss spells | **+X LP only** | Protection, Dex, Parry, Shielding are all bypassed |
| One high-Attack elite attacker | **+X Dexterity / Parry** | suppress hits at the source, pen-proof, scale with attacker quality |
| Many medium hits, low Penetration | **+X Protection / Expert Protection** | per-Damage saving scales with attack volume |
| Penetration-heavy gang (Blood Rites, post-Sunder) | **+X LP / +X Dexterity / Universal Shielding** | Protection is being stripped; these still work |
| Swarm of weak attackers | **+X Protection / +X LP** | Dex/Parry give little when each attacker lands few Aces |

---

## Cross-Cutting Principles

- **Only LP defends against everything.** Drown, direct LP-loss spells, and falling all skip the Protection roll; Dexterity, Protection, Parry, and Shielding do nothing against them. LP is the universal currency of survival.
- **Two-sided stats beat single-purpose abilities for versatility.** +X Attack helps Combat *and* Grapple/Drown; +X Dexterity defends Combat *and* enables jumps/disengage. +X Damage, Expert Offence, +X Protection, and Expert Protection each do exactly one job. A point of a stat is rarely the highest single-number boost, but it is almost always the most flexible.
- **Re-roll abilities (Expert X) trade ceiling for consistency.** They never raise the maximum and are capped by the (stat − 1) re-rollable dice; their worth rises precisely when raw success is scarce (high-difficulty target/roll).
- **Penetration and Protection are a direct tug-of-war.** Every point of Penetration cancels a point of Protection (~0.4 Damage each), down to zero. This is why Sunder Armour → high-Damage attack is one of the strongest two-action sequences, and why +Damage out-scales +Penetration once the target is already unarmoured.
- **Synergies worth remembering:** Parry + high Dexterity (compounding hit denial); Sunder Armour / Penetration + flat +Damage (push the inflated hit through stripped armour); **Penetration + Poisoned** (break armour to land the ≥1 LP that triggers the armour-independent poison); +X Attack + Vampiric Attack (more landed hits → more LP refunded); Expert Offence / −Evasion + targets you struggle to hit (high Dex / Parry opponents); Fear + Expert Offence are redundant (both re-roll failures) — don't double-invest.

> Calibrated on the reference statline (Attack 4 / Dex 4 / Prot 3), now **confirmed against the real faction stat distribution** (non-leader medians: Attack 3, Dexterity 4, Protection 3 — the reference sits at or just above median) and reproduced **10/10** by the Monte Carlo engine (`scripts/engine.py` calibration self-test). The lever magnitudes below hold for the real roster.
