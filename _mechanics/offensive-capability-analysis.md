---
title: "Offensive Capability Analysis"
description: Raw offensive capability data analysis
nav_order: 3
is_analysis: true
---

## Units and method

Unit: [**EDPA**](/mechanics/combat/) (Expected Damage Per AP, in Life Points).

The headline EDPA is **sustained, and Reload-aware**:
The model fires its best weapon up to its Reload cap over its full AP, then falls back to the next-best weapon, so a single-shot gun's per-AP throughput is roughly halved. The **alpha** column is the best *single-action* EDPA (the burst on the turn it does fire). For snipers, weight alpha for the kill turn and EDPA for sustained pressure. All cold (no WP, no Frenzy LP), best of weapons / accessible damage spells, vs the balanced reference (Dex 4 / Prot 3).

See [Combat Capabilities Calculations](/mechanics/combat/) for method and calibration.

## Role standards (sustained EDPA vs balanced)

`alpha med` = median single-shot burst.

`EDPA/ducat med` normalises for cost: **raw EDPA largely tracks cost** (Assassins/Brawlers cost more than Damage Dealers), so per-Ducat is the fairer cross-role comparison: Brawler median EDPA (3.25) > Damage Dealer (2.9) but per-Ducat they are equal (~0.19).

Both the sustained (`EDPA/ducat med`) and burst (`alpha/ducat med`) columns are per-Ducat. Use `alpha/ducat med` for Snipers (judged on burst, not sustained).

| Role | n | min | p25 | median | p75 | max | alpha med | alpha/ducat med | EDPA/ducat med |
|---|---|---|---|---|---|---|---|---|---|
| Assassin | 10 | 1.75 | 2.73 | 3.58 | 3.92 | 5.31 | 3.58 | 0.198 | 0.2 |
| Brawler | 17 | 2.35 | 2.68 | 3.25 | 3.75 | 5.06 | 3.25 | 0.196 | 0.2 |
| Damage Dealer | 66 | 1.1 | 2.11 | 2.95 | 3.59 | 5.46 | 3.14 | 0.207 | 0.19 |
| Canal Fighter | 24 | 0.57 | 1.48 | 2.68 | 3.1 | 4.98 | 2.68 | 0.151 | 0.15 |
| Tank | 6 | 1.33 | 2.06 | 2.45 | 2.79 | 3.1 | 2.45 | 0.154 | 0.15 |
| Control | 4 | 1.13 | 1.7 | 2.09 | 2.3 | 2.32 | 2.09 | 0.111 | 0.11 |
| Sniper | 6 | 0.75 | 0.97 | 1.75 | 2.3 | 2.54 | 2.92 | 0.204 | 0.13 |
| Disruptor | 6 | 0.44 | 1.25 | 1.69 | 2.04 | 2.68 | 1.69 | 0.113 | 0.11 |
| Harasser | 9 | 0.62 | 1.5 | 1.63 | 1.68 | 2.68 | 1.63 | 0.125 | 0.12 |
| Specialist | 38 | 0.11 | 1.13 | 1.56 | 2.37 | 4.14 | 1.56 | 0.123 | 0.12 |
| Line Fighter | 34 | 0.87 | 1.13 | 1.46 | 1.99 | 2.42 | 1.46 | 0.15 | 0.15 |
| Support | 42 | 0.44 | 0.62 | 1.46 | 2.09 | 4.38 | 1.5 | 0.113 | 0.11 |
| Objective Runner | 12 | 0.04 | 0.57 | 1.13 | 1.13 | 2.19 | 1.13 | 0.094 | 0.09 |

## Role offence profiles (median EDPA vs each reference defender)

Shows what each role is good against and where its output collapses considering **Raw** EDPA (absolute / threshold lens). The per-Ducat table follows raw tracks cost, so only the per-Ducat view compares roles fairly across rows.

| Role | balanced | soft | evasive | armoured | pen_proof_tank | parry |
|---|---|---|---|---|---|---|
| Assassin | 3.58 | 4.15 | 2.79 | 2.74 | 2.05 | 2.77 |
| Brawler | 3.25 | 4.48 | 2.76 | 2.45 | 2.45 | 2.06 |
| Damage Dealer | 2.95 | 4.01 | 2.52 | 2.17 | 1.9 | 2.13 |
| Canal Fighter | 2.68 | 3.79 | 2.2 | 1.92 | 1.5 | 1.69 |
| Tank | 2.45 | 3.4 | 1.99 | 1.67 | 1.32 | 1.4 |
| Control | 2.09 | 2.8 | 1.6 | 1.32 | 0.81 | 1.16 |
| Sniper | 1.75 | 2.54 | 1.56 | 1.23 | 1.06 | 1.44 |
| Disruptor | 1.69 | 2.75 | 1.46 | 1.05 | 1.05 | 1.03 |
| Harasser | 1.63 | 2.64 | 1.43 | 1.02 | 0.78 | 0.96 |
| Specialist | 1.56 | 2.5 | 1.35 | 1.05 | 0.67 | 0.96 |
| Line Fighter | 1.46 | 2.5 | 1.3 | 0.86 | 0.67 | 0.81 |
| Support | 1.46 | 2.49 | 1.3 | 0.87 | 0.67 | 0.92 |
| Objective Runner | 1.13 | 2.19 | 0.97 | 0.67 | 0.67 | 0.6 |

### Same, per Ducat (median EDPA/Ducat vs each defender, fair cross-role comparison)

| Role | balanced | soft | evasive | armoured | pen_proof_tank | parry |
|---|---|---|---|---|---|---|
| Assassin | 0.198 | 0.248 | 0.175 | 0.146 | 0.12 | 0.135 |
| Brawler | 0.196 | 0.284 | 0.172 | 0.145 | 0.145 | 0.128 |
| Damage Dealer | 0.195 | 0.26 | 0.172 | 0.146 | 0.12 | 0.136 |
| Tank | 0.154 | 0.222 | 0.131 | 0.105 | 0.088 | 0.089 |
| Canal Fighter | 0.151 | 0.223 | 0.129 | 0.108 | 0.086 | 0.094 |
| Line Fighter | 0.15 | 0.255 | 0.135 | 0.095 | 0.084 | 0.09 |
| Sniper | 0.126 | 0.167 | 0.112 | 0.088 | 0.075 | 0.102 |
| Harasser | 0.125 | 0.223 | 0.108 | 0.075 | 0.094 | 0.069 |
| Specialist | 0.123 | 0.198 | 0.103 | 0.072 | 0.066 | 0.067 |
| Disruptor | 0.113 | 0.188 | 0.097 | 0.071 | 0.064 | 0.069 |
| Control | 0.111 | 0.175 | 0.093 | 0.069 | 0.05 | 0.062 |
| Support | 0.111 | 0.195 | 0.096 | 0.066 | 0.057 | 0.071 |
| Objective Runner | 0.094 | 0.182 | 0.081 | 0.056 | 0.056 | 0.05 |

## Snipers

A Sniper fires one Reload-limited shot per turn from range, its value is the single-shot **alpha**, not sustained throughput (so it is *not* counted in the Damage Dealer pool). Sniper standard: median alpha **2.92**, median alpha/Ducat **0.204**. A sniper below the alpha/Ducat median is weak even for its cost.

| Model | Faction | cost | alpha | sustained | alpha/Ducat |
|---|---|---|---|---|---|
| Naval Lieutenant | Patricians | 15 | 5.08 | 2.54 | 0.339 |
| Scorpio Marksman | The Vatican | 15 | 4.87 | 2.44 | 0.325 |
| Venetian Spy | Patricians | 16 | 3.74 | 1.87 | 0.234 |
| Guard Marksman | Patricians | 12 | 2.1 | 1.62 | 0.175 |
| Maltese Squire | The Vatican | 10 | 1.5 | 0.75 | 0.15 |
| Arbalest | The Guild | 10 | 1.5 | 0.75 | 0.15 |

## Reload: alpha strike vs sustained throughput

Models whose single-shot **alpha** far exceeds their **sustained** EDPA (Reload caps
their fire rate). High alpha = strong on the turn they fire. Low sustained = poor turn
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

## Damage-dealer quality by faction

Global Damage Dealer median EDPA = **2.95**, median EDPA/Ducat = **0.19**. Deviation = faction median vs that global median. **`vs global (value)` (per-Ducat) is the fairer read**. The raw column favours factions whose dealers are simply more expensive.

| Faction | n dealers | median EDPA | vs global (raw) | median EDPA/ducat | vs global (value) |
|---|---|---|---|---|---|
| The Guild | 12 | 3.4 | +15% | 0.229 | +21% |
| The Vatican | 7 | 3.29 | +12% | 0.224 | +18% |
| Strigoi | 10 | 3.0 | +2% | 0.176 | -7% |
| Rashaar | 4 | 2.96 | +1% | 0.216 | +14% |
| The Doctors | 13 | 2.77 | -6% | 0.189 | -1% |
| Gifted | 11 | 2.68 | -9% | 0.155 | -18% |
| Patricians | 9 | 2.13 | -28% | 0.164 | -14% |

## Cost-efficiency

Linear fit over offensive roles (117 models): expected EDPA ≈ 1.92 + 0.06 × cost. Models far **above** the line are cost-efficient for their output. Far below are overpriced.

### Most cost-efficient (highest EDPA per Ducat, offensive roles, cost ≥ 6)

| Model | Faction | Role | cost | EDPA | alpha | EDPA/ducat | vs curve |
|---|---|---|---|---|---|---|---|
| Monstrosity | The Doctors | Damage Dealer | 9 | 2.93 | 2.93 | 0.326 | +0.47 |
| Doctor of Poisons | The Doctors | Damage Dealer | 13 | 4.08 | 4.08 | 0.314 | +1.38 |
| Prelate of the Flaming Sword | The Vatican | Damage Dealer | 15 | 4.52 | 4.52 | 0.301 | +1.70 |
| Basilisk | The Doctors | Damage Dealer | 13 | 3.86 | 3.86 | 0.297 | +1.16 |
| Rialto Assassin | The Guild | Assassin | 16 | 4.74 | 4.74 | 0.296 | +1.86 |
| Doctor of the Firmament | The Doctors | Damage Dealer | 16 | 4.71 | 4.71 | 0.294 | +1.83 |
| Sinker | Strigoi | Canal Fighter | 10 | 2.93 | 2.93 | 0.293 | +0.41 |
| Baba-Yaga | The Guild | Damage Dealer | 19 | 5.46 | 5.46 | 0.287 | +2.39 |
| Shipwright | The Guild | Damage Dealer | 12 | 3.41 | 3.41 | 0.284 | +0.77 |
| Barber | The Guild | Damage Dealer | 12 | 3.38 | 3.38 | 0.282 | +0.74 |
| Venator of Devotion | The Vatican | Brawler | 17 | 4.7 | 4.7 | 0.277 | +1.76 |
| Zovena Vela | Gifted | Damage Dealer | 15 | 3.99 | 4.14 | 0.266 | +1.17 |
| Wallachian Impaler | Strigoi | Damage Dealer | 18 | 4.74 | 4.74 | 0.263 | +1.73 |
| Avignon Guard | The Vatican | Brawler | 14 | 3.66 | 3.66 | 0.261 | +0.90 |
| Rotter | Strigoi | Canal Fighter | 12 | 3.1 | 3.1 | 0.258 | +0.46 |

### Best raw output above the cost curve (biggest positive residual)

| Model | Faction | Role | cost | EDPA | expected | residual |
|---|---|---|---|---|---|---|
| Baba-Yaga | The Guild | Damage Dealer | 19 | 5.46 | 3.07 | +2.39 |
| Rialto Assassin | The Guild | Assassin | 16 | 4.74 | 2.88 | +1.86 |
| Doctor of the Firmament | The Doctors | Damage Dealer | 16 | 4.71 | 2.88 | +1.83 |
| Venator of Devotion | The Vatican | Brawler | 17 | 4.7 | 2.94 | +1.76 |
| Wallachian Impaler | Strigoi | Damage Dealer | 18 | 4.74 | 3.01 | +1.73 |
| Prelate of the Flaming Sword | The Vatican | Damage Dealer | 15 | 4.52 | 2.82 | +1.70 |
| Golgotha | The Vatican | Brawler | 18 | 4.46 | 3.01 | +1.45 |
| Doctor of Poisons | The Doctors | Damage Dealer | 13 | 4.08 | 2.7 | +1.38 |
| Whaler | The Guild | Damage Dealer | 17 | 4.22 | 2.94 | +1.28 |
| Raadru | Rashaar | Damage Dealer | 20 | 4.37 | 3.13 | +1.24 |
| Zovena Vela | Gifted | Damage Dealer | 15 | 3.99 | 2.82 | +1.17 |
| Basilisk | The Doctors | Damage Dealer | 13 | 3.86 | 2.7 | +1.16 |

## Frenzy & burst potential by faction (annotation layer)

EDPA above is **cold** (no WP, no Frenzy). Frenzied models spend LP as bonus dice
(2 LP per fully-boosted attack) for a one-off burst. This is the layer that explains
why a faction can sit below the cold standard yet hit far harder in practice. Burst
= median best-melee EDPA vs balanced with +2 LP-dice. Cost = 2 LP per boosted attack.

| Faction | n dealers/asn/brl | Frenzied | median cold EDPA | median burst EDPA | burst uplift |
|---|---|---|---|---|---|
| Gifted | 13 | 0 (0%) | 2.68 | - | - |
| Patricians | 15 | 2 (13%) | 2.86 | 4.22 | +59% |
| Rashaar | 16 | 0 (0%) | 3.04 | - | - |
| Strigoi | 17 | 14 (82%) | 3.1 | 4.33 | +48% |
| The Doctors | 22 | 1 (5%) | 2.73 | 2.41 | +113% |
| The Guild | 17 | 0 (0%) | 3.38 | - | - |
| The Vatican | 17 | 4 (24%) | 3.29 | 4.26 | +45% |

## WP-boost potential by faction (annotation layer)

Cold EDPA excludes WP. Spending up to 2 WP on a roll adds dice (~+50% raw Aces on a
full boost). This shows each faction's offensive models that can boost from their **own**
WP pool, the resulting boosted attack, and how rich the faction's WP economy is, the layer that lifts WP-rich factions above the cold
standard. Boost = best single attack with up to +2 dice (capped by the model's own WP
pool), uplift vs cold alpha.

| Faction | WP economy | offensive models w/ own WP | median boosted atk | median uplift |
|---|---|---|---|---|
| The Vatican | Highest (most WP-rich) | 15/18 (83%) | 4.63 | +48% |
| Patricians | High (combat rewards + Sopracomito battery) | 17/17 (100%) | 4.08 | +38% |
| The Doctors | High (Nexus pool sharing) | 10/15 (67%) | 4.05 | +50% |
| Gifted | Situational-high (La Signora pulse) | 12/13 (92%) | 4.08 | +50% |
| The Guild | Medium (many small sources) | 16/16 (100%) | 4.36 | +42% |
| Rashaar | Medium (Soul Drain, close-range) | 7/7 (100%) | 4.39 | +32% |
| Strigoi | Low (uses Frenzy/LP instead) | 3/13 (23%) | 4.06 | +52% |

## Top 20 EDPA overall (sustained, with offence source)

| # | Model | Faction | Role | EDPA | alpha | EDPA/ducat | source |
|---|---|---|---|---|---|---|---|
| 1 | Baba-Yaga | The Guild | Damage Dealer | 5.46 | 5.46 | 0.287 | spell:Summon Vermin |
| 2 | Monstrous Stryx | Strigoi | Assassin | 5.31 | 5.31 | 0.133 | sustained: Monstrous Clawsx2 |
| 3 | Morgraur | Rashaar | Brawler | 5.06 | 5.06 | 0.074 | sustained: Colossal Jawsx3 |
| 4 | Emissary of Mother Hydra | Rashaar | Canal Fighter | 4.98 | 4.98 | 0.098 | sustained: Eldritch Mawx3 |
| 5 | Rialto Assassin | The Guild | Assassin | 4.74 | 4.74 | 0.296 | sustained: Balanced Throwing Knifex2 |
| 6 | Wallachian Impaler | Strigoi | Damage Dealer | 4.74 | 4.74 | 0.263 | sustained: Impaling Stakex2 |
| 7 | Doctor of the Firmament | The Doctors | Damage Dealer | 4.71 | 4.71 | 0.294 | spell:Summon Vermin |
| 8 | Venator of Devotion | The Vatican | Brawler | 4.7 | 4.7 | 0.277 | sustained: Zweihänderx2 |
| 9 | Prelate of the Flaming Sword | The Vatican | Damage Dealer | 4.52 | 4.52 | 0.301 | sustained: Burning Longswordx2 |
| 10 | Golgotha | The Vatican | Brawler | 4.46 | 4.46 | 0.248 | sustained: Stone Fistsx2 |
| 11 | Tarot Reader | Strigoi | Support | 4.38 | 4.38 | 0.274 | spell:Summon Vermin |
| 12 | Raadru | Rashaar | Damage Dealer | 4.37 | 4.37 | 0.218 | sustained: Webbed Fistsx2 |
| 13 | Whaler | The Guild | Damage Dealer | 4.22 | 4.22 | 0.248 | sustained: Whaling Lancex2 |
| 14 | Voltage Bombardiers | The Doctors | Specialist | 4.14 | 4.14 | 0.345 | sustained: Soul Bombardx2 |
| 15 | Gethsemane | The Vatican | Brawler | 4.1 | 4.1 | 0.111 | sustained: Maw Pressx3 |
| 16 | Moon Eater | Strigoi | Damage Dealer | 4.1 | 4.1 | 0.178 | sustained: Brutal Clawsx2 |
| 17 | Doctor of Poisons | The Doctors | Damage Dealer | 4.08 | 4.08 | 0.314 | sustained: Poisoned Bladex2 |
| 18 | Senshi the Undying | Gifted | Assassin | 3.99 | 3.99 | 0.2 | sustained: Daishōx2 |
| 19 | Zovena Vela | Gifted | Damage Dealer | 3.99 | 4.14 | 0.266 | sustained: Fiery Explosionx1+Fireballx1 |
| 20 | Justice | Gifted | Damage Dealer | 3.9 | 3.9 | 0.217 | sustained: Sword of Balancex2 |
