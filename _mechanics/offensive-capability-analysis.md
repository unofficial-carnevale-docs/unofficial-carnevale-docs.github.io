---
title: "Offensive Capability Analysis"
description: Raw offensive capability data analysis
nav_order: 3
is_analysis: true
---

## Units and method

Unit: [**EDPA**](/mechanics/combat/) (Expected Damage Per AP, in Life Points).

The headline EDPA is **sustained, Reload-aware**:
The model fires its best weapon up to its Reload cap over its full AP, then falls back to the next-best weapon, so a single-shot gun's per-AP throughput is roughly halved. The **alpha** column is the best *single-action* EDPA (the burst on the turn it does fire), and for snipers/artillery, weigh alpha for the kill turn and EDPA for sustained pressure. All cold (no WP, no Frenzy LP), best of weapons / accessible damage spells, vs the balanced reference (Dex 4 / Prot 3).

See [Combat Capabilities Calculations](/mechanics/combat/) for method and calibration.

## Role standards (sustained EDPA vs balanced)

`alpha med` = median single-shot burst. **Snipers are judged on alpha, not sustained**: their low sustained here is by design.

| Role | n | min | p25 | median | p75 | max | alpha med |
|---|---|---|---|---|---|---|---|
| Assassin | 10 | 1.75 | 2.73 | 3.58 | 3.92 | 5.31 | 3.58 |
| Brawler | 15 | 2.41 | 2.83 | 3.25 | 3.75 | 5.06 | 3.25 |
| Canal Fighter | 24 | 0.57 | 1.48 | 2.68 | 3.1 | 4.98 | 2.68 |
| Control | 4 | 1.13 | 1.7 | 2.09 | 2.3 | 2.32 | 2.09 |
| Damage Dealer | 69 | 1.1 | 2.11 | 2.9 | 3.58 | 5.46 | 3.13 |
| Disruptor | 5 | 0.44 | 1.13 | 1.63 | 1.75 | 2.13 | 1.63 |
| Harasser | 9 | 0.62 | 1.5 | 1.63 | 1.68 | 2.68 | 1.63 |
| Line Fighter | 33 | 0.87 | 1.13 | 1.43 | 1.99 | 2.42 | 1.43 |
| Objective Runner | 12 | 0.04 | 0.57 | 1.13 | 1.13 | 2.19 | 1.13 |
| Sniper | 6 | 0.75 | 0.97 | 1.75 | 2.3 | 2.54 | 2.92 |
| Specialist | 38 | 0.11 | 1.13 | 1.56 | 2.37 | 4.14 | 1.56 |
| Support | 42 | 0.44 | 0.62 | 1.46 | 2.09 | 4.38 | 1.5 |
| Tank | 7 | 1.33 | 1.99 | 2.29 | 2.73 | 3.1 | 2.29 |

## Role offence profiles (median EDPA vs each reference defender)

Shows what each role is good against, and where its output collapses.

| Role | balanced | soft | evasive | armoured | pen_proof_tank | parry |
|---|---|---|---|---|---|---|
| Assassin | 3.58 | 4.15 | 2.79 | 2.74 | 2.05 | 2.77 |
| Brawler | 3.25 | 4.48 | 2.76 | 2.45 | 2.45 | 2.06 |
| Damage Dealer | 2.9 | 4.01 | 2.49 | 2.12 | 1.89 | 2.09 |
| Canal Fighter | 2.68 | 3.79 | 2.2 | 1.92 | 1.5 | 1.69 |
| Tank | 2.29 | 3.3 | 1.88 | 1.58 | 1.32 | 1.25 |
| Control | 2.09 | 2.8 | 1.6 | 1.32 | 0.81 | 1.16 |
| Sniper | 1.75 | 2.54 | 1.56 | 1.23 | 1.06 | 1.44 |
| Disruptor | 1.63 | 2.48 | 1.41 | 0.98 | 0.98 | 0.93 |
| Harasser | 1.63 | 2.64 | 1.43 | 1.02 | 0.78 | 0.96 |
| Specialist | 1.56 | 2.5 | 1.35 | 1.05 | 0.67 | 0.96 |
| Support | 1.46 | 2.49 | 1.3 | 0.87 | 0.67 | 0.92 |
| Line Fighter | 1.43 | 2.49 | 1.3 | 0.85 | 0.67 | 0.81 |
| Objective Runner | 1.13 | 2.19 | 0.97 | 0.67 | 0.67 | 0.6 |

## Snipers (judged on alpha, not sustained)

A Sniper fires one Reload-limited shot per turn from range: its value is the
single-shot **alpha**, not sustained throughput (so it is *not* counted in the Damage
Dealer pool). Sniper standard: median alpha **2.92**, median alpha/Ducat **0.204**. A sniper below the alpha/Ducat median is weak even for its cost.

| Model | Faction | cost | alpha | sustained | alpha/Ducat |
|---|---|---|---|---|---|
| Naval Lieutenant | Patricians | 15 | 5.08 | 2.54 | 0.339 |
| Scorpio Marksman | The Vatican | 15 | 4.87 | 2.44 | 0.325 |
| Venetian Spy | Patricians | 16 | 3.74 | 1.87 | 0.234 |
| Guard Marksman | Patricians | 12 | 2.1 | 1.62 | 0.175 |
| Maltese Squire | The Vatican | 10 | 1.5 | 0.75 | 0.15 |
| Arbalest | The Guild | 10 | 1.5 | 0.75 | 0.15 |

## Damage-dealer quality by faction

Global Damage Dealer median EDPA = **2.9**. Deviation = faction's Damage Dealer median vs that global median.

| Faction | n dealers | median EDPA | vs global |
|---|---|---|---|
| The Guild | 12 | 3.4 | +17% |
| The Vatican | 9 | 3.29 | +13% |
| Strigoi | 10 | 3.0 | +3% |
| Rashaar | 4 | 2.96 | +2% |
| The Doctors | 13 | 2.77 | -4% |
| Gifted | 11 | 2.32 | -20% |
| Patricians | 10 | 2.24 | -23% |

## Cost-efficiency

Linear fit over offensive roles (118 models): expected EDPA ≈ 1.89 + 0.061 × cost. Models far **above** the line are cost-efficient for their output. Far below the line means overpriced.

### Most cost-efficient (highest EDPA per Ducat, offensive roles, cost ≥ 6)

| Model | Faction | Role | cost | EDPA | alpha | EDPA/ducat | vs curve |
|---|---|---|---|---|---|---|---|
| Monstrosity | The Doctors | Damage Dealer | 9 | 2.93 | 2.93 | 0.326 | +0.49 |
| Doctor of Poisons | The Doctors | Damage Dealer | 13 | 4.08 | 4.08 | 0.314 | +1.40 |
| Prelate of the Flaming Sword | The Vatican | Damage Dealer | 15 | 4.52 | 4.52 | 0.301 | +1.72 |
| Basilisk | The Doctors | Damage Dealer | 13 | 3.86 | 3.86 | 0.297 | +1.18 |
| Rialto Assassin | The Guild | Assassin | 16 | 4.74 | 4.74 | 0.296 | +1.88 |
| Doctor of the Firmament | The Doctors | Damage Dealer | 16 | 4.71 | 4.71 | 0.294 | +1.85 |
| Sinker | Strigoi | Canal Fighter | 10 | 2.93 | 2.93 | 0.293 | +0.43 |
| Baba-Yaga | The Guild | Damage Dealer | 19 | 5.46 | 5.46 | 0.287 | +2.41 |
| Shipwright | The Guild | Damage Dealer | 12 | 3.41 | 3.41 | 0.284 | +0.79 |
| Barber | The Guild | Damage Dealer | 12 | 3.38 | 3.38 | 0.282 | +0.76 |
| Venator of Devotion | The Vatican | Damage Dealer | 17 | 4.7 | 4.7 | 0.277 | +1.77 |
| Wallachian Impaler | Strigoi | Damage Dealer | 18 | 4.74 | 4.74 | 0.263 | +1.75 |
| Avignon Guard | The Vatican | Brawler | 14 | 3.66 | 3.66 | 0.261 | +0.92 |
| Rotter | Strigoi | Canal Fighter | 12 | 3.1 | 3.1 | 0.258 | +0.48 |
| Stigmatist | The Vatican | Damage Dealer | 13 | 3.34 | 3.34 | 0.257 | +0.66 |

### Best raw output above the cost curve (biggest positive residual)

| Model | Faction | Role | cost | EDPA | expected | residual |
|---|---|---|---|---|---|---|
| Baba-Yaga | The Guild | Damage Dealer | 19 | 5.46 | 3.05 | +2.41 |
| Rialto Assassin | The Guild | Assassin | 16 | 4.74 | 2.86 | +1.88 |
| Doctor of the Firmament | The Doctors | Damage Dealer | 16 | 4.71 | 2.86 | +1.85 |
| Venator of Devotion | The Vatican | Damage Dealer | 17 | 4.7 | 2.93 | +1.77 |
| Wallachian Impaler | Strigoi | Damage Dealer | 18 | 4.74 | 2.99 | +1.75 |
| Prelate of the Flaming Sword | The Vatican | Damage Dealer | 15 | 4.52 | 2.8 | +1.72 |
| Golgotha | The Vatican | Brawler | 18 | 4.46 | 2.99 | +1.47 |
| Doctor of Poisons | The Doctors | Damage Dealer | 13 | 4.08 | 2.68 | +1.40 |
| Whaler | The Guild | Damage Dealer | 17 | 4.22 | 2.93 | +1.29 |
| Raadru | Rashaar | Damage Dealer | 20 | 4.37 | 3.11 | +1.26 |
| Basilisk | The Doctors | Damage Dealer | 13 | 3.86 | 2.68 | +1.18 |
| Witch | The Guild | Damage Dealer | 16 | 3.85 | 2.86 | +0.99 |

## Frenzy & burst potential by faction (annotation layer)

EDPA above is **cold** (no WP, no Frenzy). Frenzied models spend LP as bonus dice
(2 LP per fully-boosted attack) for a one-off burst. This is the layer that explains
why a faction can sit below the cold standard yet hit far harder in practice. Burst
= median best-melee EDPA vs balanced with +2 LP-dice, at 2 LP per boosted attack.

| Faction | n dealers/asn/brl | Frenzied | median cold EDPA | median burst EDPA | burst uplift |
|---|---|---|---|---|---|
| Strigoi | 17 | 14 (82%) | 3.1 | 4.33 | +48% |
| The Vatican | 18 | 4 (22%) | 3.27 | 4.26 | +45% |
| Patricians | 15 | 2 (13%) | 2.86 | 4.22 | +59% |
| The Doctors | 22 | 1 (5%) | 2.73 | 2.41 | +113% |
| Gifted | 13 | 0 (0%) | 2.68 | - | - |
| Rashaar | 16 | 0 (0%) | 3.04 | - | - |
| The Guild | 17 | 0 (0%) | 3.38 | - | - |

## Reload: alpha strike vs sustained throughput

Models whose single-shot **alpha** far exceeds their **sustained** EDPA (Reload caps
their fire rate). High alpha = strong on the turn they fire, low sustained = poor turn
over turn. Cost-efficiency above uses sustained, so these rank lower than their burst suggests.

| Model | Faction | Role | alpha | sustained | drop |
|---|---|---|---|---|---|
| Naval Lieutenant | Patricians | Sniper | 5.08 | 2.54 | 2.54 |
| Scorpio Marksman | The Vatican | Sniper | 4.87 | 2.44 | 2.43 |
| Theophant of Sinai | The Vatican | Damage Dealer | 4.81 | 2.4 | 2.41 |
| Venetian Spy | Patricians | Sniper | 3.74 | 1.87 | 1.87 |
| Ordnance Doctor | The Doctors | Damage Dealer | 3.45 | 1.73 | 1.72 |
| The Demolitionist | Gifted | Damage Dealer | 3.15 | 1.58 | 1.57 |
| Baroni | The Guild | Damage Dealer | 4.83 | 3.34 | 1.49 |
| Smuggler | The Guild | Support | 2.84 | 1.42 | 1.42 |
| Electron Cannoneer | The Doctors | Damage Dealer | 2.42 | 1.21 | 1.21 |
| Firebreather | The Guild | Damage Dealer | 2.2 | 1.1 | 1.1 |
| Janissary Sapper | Patricians | Damage Dealer | 3.96 | 2.86 | 1.1 |
| Marine Biologist | The Doctors | Canal Fighter | 1.7 | 0.85 | 0.85 |
| Maltese Squire | The Vatican | Sniper | 1.5 | 0.75 | 0.75 |
| Arbalest | The Guild | Sniper | 1.5 | 0.75 | 0.75 |
| Noble Seafarer | Patricians | Damage Dealer | 2.6 | 1.87 | 0.73 |

## WP-boost potential by faction (annotation layer)

Cold EDPA excludes WP. Spending up to 2 WP on a roll adds dice (~+50% raw Aces on a
full boost). This shows each faction's offensive models that can boost from their **own**
WP pool, the resulting boosted attack, and how rich the faction's WP economy is (per
`wp_generation_by_faction.md`), the layer that lifts WP-rich factions above the cold
standard. Boost = best single attack with up to +2 dice (capped by the model's own WP
pool), uplift vs cold alpha.

| Faction | WP economy | offensive models w/ own WP | median boosted atk | median uplift |
|---|---|---|---|---|
| The Vatican | Highest (most WP-rich) | 16/19 (84%) | 4.63 | +46% |
| Rashaar | Medium (Soul Drain, close-range) | 7/7 (100%) | 4.39 | +32% |
| The Guild | Medium (many small sources) | 16/16 (100%) | 4.36 | +42% |
| Patricians | High (combat rewards + Sopracomito battery) | 17/17 (100%) | 4.08 | +38% |
| Gifted | Situational-high (La Signora pulse) | 12/13 (92%) | 4.06 | +52% |
| Strigoi | Low (uses Frenzy/LP instead) | 3/13 (23%) | 4.06 | +52% |
| The Doctors | High (Nexus pool sharing) | 10/15 (67%) | 4.05 | +50% |

## Top 20 EDPA overall (sustained, with offence source)

| # | Model | Faction | Role | EDPA | alpha | source |
|---|---|---|---|---|---|---|
| 1 | Baba-Yaga | The Guild | Damage Dealer | 5.46 | 5.46 | spell:Summon Vermin |
| 2 | Monstrous Stryx | Strigoi | Assassin | 5.31 | 5.31 | sustained: Monstrous Clawsx2 |
| 3 | Morgraur | Rashaar | Brawler | 5.06 | 5.06 | sustained: Colossal Jawsx3 |
| 4 | Emissary of Mother Hydra | Rashaar | Canal Fighter | 4.98 | 4.98 | sustained: Eldritch Mawx3 |
| 5 | Rialto Assassin | The Guild | Assassin | 4.74 | 4.74 | sustained: Balanced Throwing Knifex2 |
| 6 | Wallachian Impaler | Strigoi | Damage Dealer | 4.74 | 4.74 | sustained: Impaling Stakex2 |
| 7 | Doctor of the Firmament | The Doctors | Damage Dealer | 4.71 | 4.71 | spell:Summon Vermin |
| 8 | Venator of Devotion | The Vatican | Damage Dealer | 4.7 | 4.7 | sustained: Zweihänderx2 |
| 9 | Prelate of the Flaming Sword | The Vatican | Damage Dealer | 4.52 | 4.52 | sustained: Burning Longswordx2 |
| 10 | Golgotha | The Vatican | Brawler | 4.46 | 4.46 | sustained: Stone Fistsx2 |
| 11 | Tarot Reader | Strigoi | Support | 4.38 | 4.38 | spell:Summon Vermin |
| 12 | Raadru | Rashaar | Damage Dealer | 4.37 | 4.37 | sustained: Webbed Fistsx2 |
| 13 | Whaler | The Guild | Damage Dealer | 4.22 | 4.22 | sustained: Whaling Lancex2 |
| 14 | Voltage Bombardiers | The Doctors | Specialist | 4.14 | 4.14 | sustained: Soul Bombardx2 |
| 15 | Gethsemane | The Vatican | Brawler | 4.1 | 4.1 | sustained: Maw Pressx3 |
| 16 | Moon Eater | Strigoi | Damage Dealer | 4.1 | 4.1 | sustained: Brutal Clawsx2 |
| 17 | Doctor of Poisons | The Doctors | Damage Dealer | 4.08 | 4.08 | sustained: Poisoned Bladex2 |
| 18 | Senshi the Undying | Gifted | Assassin | 3.99 | 3.99 | sustained: Daishōx2 |
| 19 | Justice | Gifted | Damage Dealer | 3.9 | 3.9 | sustained: Sword of Balancex2 |
| 20 | Basilisk | The Doctors | Damage Dealer | 3.86 | 3.86 | sustained: Venomous Sprayx2 |
