---
title: "Offensive Capability Analysis"
description: Raw offensive capability data analysis
nav_order: 3
is_analysis: true
toc:
  - title: Units and method
    anchor: units-and-method
  - title: Role profiles vs defenders
    anchor: role-profiles-vs-defenders
  - title: Alpha vs sustained
    anchor: alpha-vs-sustained
  - title: By faction
    anchor: by-faction
  - title: Cost-efficiency
    anchor: cost-efficiency
  - title: Top 20 by EDPA
    anchor: top-20-by-edpa
---

## Units and method

Unit: [**EDPA**](/mechanics/combat/) (Expected Damage Per AP, in Life Points).

The headline EDPA is **sustained, and Reload-aware**:
The model fires its best weapon up to its Reload cap over its full AP, then falls back to the next-best weapon, so a single-shot gun's per-AP throughput is roughly halved. The **alpha** column is the best *single-action* EDPA (the burst on the turn it does fire). For snipers, weight alpha for the kill turn and EDPA for sustained pressure. All cold (no WP, no Frenzy LP), best of weapons / accessible damage spells, vs the balanced reference (Dex 4 / Prot 3).

See [Combat Capabilities Calculations](/mechanics/combat/) for method and calibration.

## Role profiles vs defenders

Median EDPA per role vs each reference defender, showing what each role is good against and where its output collapses. The `balanced` column (Dex 4 / Prot 3) is each role's headline EDPA. **Raw** EDPA is the absolute / threshold lens. The per-Ducat table follows: since raw EDPA largely tracks cost (e.g. Brawler median 3.25 > Damage Dealer 2.92, but per-Ducat both sit at ~0.19), only the per-Ducat view compares roles fairly across rows.

| Role | balanced | soft | evasive | armoured | pen_proof_tank | parry |
|---|---|---|---|---|---|---|
| Brawler | 3.25 | 4.48 | 2.76 | 2.45 | 2.45 | 2.06 |
| Assassin | 3.23 | 4.15 | 2.79 | 2.61 | 2.01 | 2.67 |
| Damage Dealer | 2.92 | 3.83 | 2.54 | 2.17 | 1.92 | 2.13 |
| Canal Fighter | 2.68 | 3.45 | 2.2 | 1.92 | 1.65 | 1.69 |
| Tank | 2.45 | 3.4 | 1.99 | 1.67 | 1.32 | 1.4 |
| Control | 2.09 | 2.8 | 1.6 | 1.32 | 0.81 | 1.16 |
| Sniper | 1.87 | 2.74 | 1.74 | 1.44 | 1.27 | 1.7 |
| Disruptor | 1.69 | 2.75 | 1.46 | 1.05 | 1.05 | 1.03 |
| Harasser | 1.63 | 2.64 | 1.43 | 1.02 | 0.78 | 0.96 |
| Specialist | 1.56 | 2.5 | 1.35 | 1.05 | 0.67 | 0.96 |
| Line Fighter | 1.46 | 2.5 | 1.29 | 0.86 | 0.67 | 0.81 |
| Support | 1.46 | 2.41 | 1.3 | 0.87 | 0.67 | 0.92 |
| Objective Runner | 1.13 | 2.19 | 0.97 | 0.67 | 0.67 | 0.6 |

### Per Ducat

Median EDPA/Ducat vs each defender, the fair cross-role comparison.

| Role | balanced | soft | evasive | armoured | pen_proof_tank | parry |
|---|---|---|---|---|---|---|
| Brawler | 0.196 | 0.284 | 0.172 | 0.145 | 0.145 | 0.128 |
| Assassin | 0.193 | 0.229 | 0.175 | 0.146 | 0.12 | 0.135 |
| Damage Dealer | 0.186 | 0.254 | 0.173 | 0.145 | 0.121 | 0.136 |
| Sniper | 0.156 | 0.194 | 0.132 | 0.106 | 0.104 | 0.119 |
| Tank | 0.154 | 0.222 | 0.131 | 0.105 | 0.088 | 0.089 |
| Canal Fighter | 0.151 | 0.223 | 0.129 | 0.108 | 0.091 | 0.094 |
| Line Fighter | 0.148 | 0.255 | 0.135 | 0.095 | 0.084 | 0.09 |
| Specialist | 0.123 | 0.194 | 0.103 | 0.072 | 0.066 | 0.067 |
| Harasser | 0.121 | 0.221 | 0.105 | 0.074 | 0.091 | 0.08 |
| Disruptor | 0.113 | 0.188 | 0.097 | 0.071 | 0.064 | 0.069 |
| Control | 0.111 | 0.175 | 0.093 | 0.069 | 0.05 | 0.062 |
| Support | 0.111 | 0.181 | 0.096 | 0.066 | 0.057 | 0.071 |
| Objective Runner | 0.094 | 0.182 | 0.081 | 0.056 | 0.056 | 0.05 |

## Alpha vs sustained

Some roles are judged on their single-shot **alpha**, not sustained EDPA, because Reload caps how often they fire. These two views isolate that gap.

### Snipers

A Sniper fires one Reload-limited shot per turn from range, its value is the single-shot **alpha**, not sustained throughput (so it is *not* counted in the Damage Dealer pool). Sniper standard: median alpha **3.74**, median alpha/Ducat **0.234**. A sniper below the alpha/Ducat median is weak even for its cost.

| Model | Faction | cost | alpha | sustained | alpha/Ducat |
|---|---|---|---|---|---|
| [Naval Lieutenant](/factions/patricians/naval-lieutenant/) | Patricians | 15 | 5.08 | 2.54 | 0.339 |
| [Scorpio Marksman](/factions/the-vatican/scorpio-marksman/) | The Vatican | 15 | 4.87 | 2.44 | 0.325 |
| [Baroni](/factions/the-guild/baroni/) | The Guild | 15 | 4.83 | 2.41 | 0.322 |
| [Theophant of Sinai](/factions/the-vatican/theophant-of-sinai/) | The Vatican | 13 | 4.81 | 2.4 | 0.37 |
| [Venetian Spy](/factions/patricians/venetian-spy/) | Patricians | 16 | 3.74 | 1.87 | 0.234 |
| [Noble Seafarer](/factions/patricians/noble-seafarer/) | Patricians | 12 | 2.6 | 1.87 | 0.217 |
| [Guard Marksman](/factions/patricians/guard-marksman/) | Patricians | 12 | 2.1 | 1.62 | 0.175 |
| [Maltese Squire](/factions/the-vatican/maltese-squire/) | The Vatican | 10 | 1.5 | 0.75 | 0.15 |
| [Arbalest](/factions/the-guild/arbalest/) | The Guild | 10 | 1.5 | 0.75 | 0.15 |

### Burst over sustained

Models whose single-shot **alpha** far exceeds their **sustained** EDPA, from one of two causes: a **Reload-capped weapon** (guns and artillery that fire once per round, e.g. Spirit Cannon, Bomb, Electron Cannon) or a **once-per-round damage spell** (the Wild Magic casters here burst with a single strong Summon Vermin, the Drowned Nun with Dagonite Baptism). High alpha means strong on the turn they fire, low sustained means poor turn over turn. Cost-efficiency below uses sustained, so these rank lower than their burst suggests.

| Model | Faction | Role | alpha | sustained | drop |
|---|---|---|---|---|---|
| [Naval Lieutenant](/factions/patricians/naval-lieutenant/) | Patricians | Sniper | 5.08 | 2.54 | 2.54 |
| [Scorpio Marksman](/factions/the-vatican/scorpio-marksman/) | The Vatican | Sniper | 4.87 | 2.44 | 2.43 |
| [Baroni](/factions/the-guild/baroni/) | The Guild | Sniper | 4.83 | 2.41 | 2.42 |
| [Theophant of Sinai](/factions/the-vatican/theophant-of-sinai/) | The Vatican | Sniper | 4.81 | 2.4 | 2.41 |
| [Venetian Spy](/factions/patricians/venetian-spy/) | Patricians | Sniper | 3.74 | 1.87 | 1.87 |
| [Tarot Reader](/factions/strigoi/tarot-reader/) | Strigoi | Support | 4.38 | 2.66 | 1.72 |
| [Ordnance Doctor](/factions/the-doctors/ordnance-doctor/) | The Doctors | Damage Dealer | 3.45 | 1.73 | 1.72 |
| [The Demolitionist](/factions/gifted/the-demolitionist/) | Gifted | Damage Dealer | 3.15 | 1.58 | 1.57 |
| [Smuggler](/factions/the-guild/smuggler/) | The Guild | Support | 2.84 | 1.42 | 1.42 |
| [Maria Fioritura](/factions/gifted/maria-fioritura/) | Gifted | Support | 3.73 | 2.31 | 1.42 |
| [Electron Cannoneer](/factions/the-doctors/electron-cannoneer/) | The Doctors | Damage Dealer | 2.42 | 1.21 | 1.21 |
| [Galilean Priest](/factions/the-vatican/galilean-priest/) | The Vatican | Support | 3.24 | 2.04 | 1.2 |
| [The Drowned Nun](/factions/rashaar/the-drowned-nun/) | Rashaar | Canal Fighter | 2.93 | 1.77 | 1.16 |
| [Aglaope](/factions/rashaar/aglaope/) | Rashaar | Support | 2.75 | 1.59 | 1.16 |
| [Firebreather](/factions/the-guild/firebreather/) | The Guild | Damage Dealer | 2.2 | 1.1 | 1.1 |

## By faction

Faction-level offence: output quality against the global standard, plus the two annotation layers (Frenzy and WP) that lift factions above their cold EDPA.

### Output quality

Per-faction median EDPA for each primary offensive role, vs that role's global median (Snipers are judged separately on alpha, above). ***vs global (value)* (per-Ducat) is the fairer read**. The raw column favours factions whose models are simply more expensive.

**Small-n factions (1-2 models) are effectively a single statline, not a distribution.**

**Damage Dealers** (global median EDPA 2.92, EDPA/Ducat 0.19):

| Faction | n | median EDPA | vs global (raw) | median EDPA/ducat | vs global (value) |
|---|---|---|---|---|---|
| The Vatican | 6 | 3.21 | +10% | 0.215 | +13% |
| The Guild | 10 | 3.4 | +16% | 0.208 | +9% |
| Rashaar | 4 | 2.54 | -13% | 0.198 | +4% |
| The Doctors | 13 | 2.77 | -5% | 0.189 | -1% |
| Patricians | 8 | 2.5 | -15% | 0.171 | -10% |
| Strigoi | 10 | 2.88 | -1% | 0.168 | -12% |
| Gifted | 11 | 2.68 | -8% | 0.155 | -18% |

**Brawlers** (global median EDPA 3.25, EDPA/Ducat 0.2):

| Faction | n | median EDPA | vs global (raw) | median EDPA/ducat | vs global (value) |
|---|---|---|---|---|---|
| The Vatican | 8 | 3.7 | +14% | 0.215 | +7% |
| Rashaar | 3 | 3.75 | +15% | 0.208 | +4% |
| The Guild | 1 | 2.68 | -18% | 0.206 | +3% |
| Patricians | 3 | 3.01 | -7% | 0.194 | -3% |
| Gifted | 1 | 2.68 | -18% | 0.179 | -11% |
| The Doctors | 1 | 2.41 | -26% | 0.161 | -20% |

**Assassins** (global median EDPA 3.23, EDPA/Ducat 0.19):

| Faction | n | median EDPA | vs global (raw) | median EDPA/ducat | vs global (value) |
|---|---|---|---|---|---|
| The Guild | 2 | 3.7 | +15% | 0.243 | +28% |
| The Doctors | 1 | 2.89 | -11% | 0.222 | +17% |
| Patricians | 2 | 3.28 | +2% | 0.213 | +12% |
| Gifted | 1 | 3.99 | +24% | 0.2 | +5% |
| The Vatican | 1 | 2.68 | -17% | 0.134 | -29% |
| Strigoi | 3 | 3.52 | +9% | 0.133 | -30% |

### Frenzy burst

EDPA above is **cold** (no WP, no Frenzy). Frenzied models spend LP as bonus dice (2 LP per fully-boosted attack) for a one-off burst. This is the layer that explains why a faction can sit below the cold standard yet hit far harder in practice. Burst = median best-melee EDPA vs balanced with +2 LP-dice. Cost = 2 LP per boosted attack.

| Faction | n dealers/asn/brl | Frenzied | median cold EDPA | median burst EDPA | burst uplift |
|---|---|---|---|---|---|
| Gifted | 13 | 0 (0%) | 2.68 | - | - |
| Patricians | 14 | 2 (14%) | 2.9 | 4.22 | +59% |
| Rashaar | 16 | 0 (0%) | 2.83 | - | - |
| Strigoi | 17 | 14 (82%) | 3.09 | 4.33 | +48% |
| The Doctors | 22 | 1 (5%) | 2.73 | 2.41 | +113% |
| The Guild | 15 | 0 (0%) | 3.38 | - | - |
| The Vatican | 16 | 4 (25%) | 3.27 | 4.26 | +45% |

### WP-boost

Cold EDPA excludes WP. Spending up to 2 WP on a roll adds dice (~+50% raw Aces on a full boost). This shows each faction's offensive models that can boost from their **own** WP pool, the resulting boosted attack, and how rich the faction's WP economy is, the layer that lifts WP-rich factions above the cold standard. Boost = best single attack with up to +2 dice (capped by the model's own WP pool), uplift vs cold alpha.

| Faction | WP economy | offensive models w/ own WP | median boosted atk | median uplift |
|---|---|---|---|---|
| The Vatican | Highest (most WP-rich) | 15/18 (83%) | 4.63 | +48% |
| Patricians | High (combat rewards + Sopracomito battery) | 17/17 (100%) | 4.08 | +38% |
| The Doctors | High (Nexus pool sharing) | 9/15 (60%) | 4.12 | +53% |
| Gifted | Situational-high (La Signora pulse) | 12/13 (92%) | 4.08 | +50% |
| The Guild | Medium (many small sources) | 13/15 (87%) | 4.29 | +45% |
| Rashaar | Medium (Soul Drain, close-range) | 7/7 (100%) | 4.31 | +32% |
| Strigoi | Low (uses Frenzy/LP instead) | 3/13 (23%) | 4.06 | +52% |

## Cost-efficiency

Linear fit over offensive roles (113 models): expected EDPA ≈ 1.83 + 0.064 × cost. Models far **above** the line are cost-efficient for their output. Far below are overpriced.

### Most cost-efficient (EDPA/Ducat, cost ≥ 6)

| Model | Faction | Role | cost | EDPA | alpha | EDPA/ducat | vs curve |
|---|---|---|---|---|---|---|---|
| Monstrosity | The Doctors | Damage Dealer | 9 | 2.93 | 2.93 | 0.326 | +0.52 |
| Doctor of Poisons | The Doctors | Damage Dealer | 13 | 4.08 | 4.08 | 0.314 | +1.41 |
| Prelate of the Flaming Sword | The Vatican | Damage Dealer | 15 | 4.52 | 4.52 | 0.301 | +1.72 |
| Basilisk | The Doctors | Damage Dealer | 13 | 3.86 | 3.86 | 0.297 | +1.19 |
| Rialto Assassin | The Guild | Assassin | 16 | 4.74 | 4.74 | 0.296 | +1.88 |
| Sinker | Strigoi | Canal Fighter | 10 | 2.93 | 2.93 | 0.293 | +0.46 |
| Shipwright | The Guild | Damage Dealer | 12 | 3.41 | 3.41 | 0.284 | +0.81 |
| Barber | The Guild | Damage Dealer | 12 | 3.38 | 3.38 | 0.282 | +0.78 |
| Venator of Devotion | The Vatican | Brawler | 17 | 4.7 | 4.7 | 0.277 | +1.78 |
| Zovena Vela | Gifted | Damage Dealer | 15 | 3.99 | 4.14 | 0.266 | +1.19 |
| Doctor of the Firmament | The Doctors | Damage Dealer | 16 | 4.25 | 4.71 | 0.266 | +1.39 |
| Wallachian Impaler | Strigoi | Damage Dealer | 18 | 4.74 | 4.74 | 0.263 | +1.75 |
| Avignon Guard | The Vatican | Brawler | 14 | 3.66 | 3.66 | 0.261 | +0.93 |
| Rotter | Strigoi | Canal Fighter | 12 | 3.1 | 3.1 | 0.258 | +0.50 |
| Hulking Moroi | Strigoi | Damage Dealer | 14 | 3.59 | 3.59 | 0.256 | +0.86 |

### Above the cost curve (biggest positive residual)

| Model | Faction | Role | cost | EDPA | expected | residual |
|---|---|---|---|---|---|---|
| Ostrich Chariot?! | The Guild | Damage Dealer | 34 | 5.96 | 4.02 | +1.94 |
| Rialto Assassin | The Guild | Assassin | 16 | 4.74 | 2.86 | +1.88 |
| Venator of Devotion | The Vatican | Brawler | 17 | 4.7 | 2.92 | +1.78 |
| Wallachian Impaler | Strigoi | Damage Dealer | 18 | 4.74 | 2.99 | +1.75 |
| Prelate of the Flaming Sword | The Vatican | Damage Dealer | 15 | 4.52 | 2.8 | +1.72 |
| Golgotha | The Vatican | Brawler | 18 | 4.46 | 2.99 | +1.47 |
| Doctor of Poisons | The Doctors | Damage Dealer | 13 | 4.08 | 2.67 | +1.41 |
| Doctor of the Firmament | The Doctors | Damage Dealer | 16 | 4.25 | 2.86 | +1.39 |
| Whaler | The Guild | Damage Dealer | 17 | 4.22 | 2.92 | +1.30 |
| Raadru | Rashaar | Damage Dealer | 20 | 4.37 | 3.12 | +1.25 |
| Zovena Vela | Gifted | Damage Dealer | 15 | 3.99 | 2.8 | +1.19 |
| Basilisk | The Doctors | Damage Dealer | 13 | 3.86 | 2.67 | +1.19 |

## Top 20 by EDPA

Sustained EDPA, with the offence source that produces it.

| # | Model | Faction | Role | EDPA | alpha | EDPA/ducat | source |
|---|---|---|---|---|---|---|---|
| 1 | Ostrich Chariot?! | The Guild | Damage Dealer | 5.96 | 5.96 | 0.175 | sustained: Bird Kickx2 +Bottle Burner(free AoO/AP) |
| 2 | Monstrous Stryx | Strigoi | Assassin | 5.31 | 5.31 | 0.133 | sustained: Monstrous Clawsx2 |
| 3 | Morgraur | Rashaar | Brawler | 5.06 | 5.06 | 0.074 | sustained: Colossal Jawsx3 |
| 4 | Emissary of Mother Hydra | Rashaar | Canal Fighter | 4.98 | 4.98 | 0.098 | sustained: Eldritch Mawx3 |
| 5 | Rialto Assassin | The Guild | Assassin | 4.74 | 4.74 | 0.296 | sustained: Balanced Throwing Knifex2 |
| 6 | Wallachian Impaler | Strigoi | Damage Dealer | 4.74 | 4.74 | 0.263 | sustained: Impaling Stakex2 |
| 7 | Venator of Devotion | The Vatican | Brawler | 4.7 | 4.7 | 0.277 | sustained: Zweihänderx2 |
| 8 | Prelate of the Flaming Sword | The Vatican | Damage Dealer | 4.52 | 4.52 | 0.301 | sustained: Burning Longswordx2 |
| 9 | Golgotha | The Vatican | Brawler | 4.46 | 4.46 | 0.248 | sustained: Stone Fistsx2 |
| 10 | Raadru | Rashaar | Damage Dealer | 4.37 | 4.37 | 0.218 | sustained: Webbed Fistsx2 |
| 11 | Doctor of the Firmament | The Doctors | Damage Dealer | 4.25 | 4.71 | 0.266 | sustained: spell:Summon Verminx1+spell:Kraken's Breathx1 |
| 12 | Whaler | The Guild | Damage Dealer | 4.22 | 4.22 | 0.248 | sustained: Whaling Lancex2 |
| 13 | Voltage Bombardiers | The Doctors | Specialist | 4.14 | 4.14 | 0.345 | sustained: Soul Bombardx2 |
| 14 | Gethsemane | The Vatican | Brawler | 4.1 | 4.1 | 0.111 | sustained: Maw Pressx3 |
| 15 | Moon Eater | Strigoi | Damage Dealer | 4.1 | 4.1 | 0.178 | sustained: Brutal Clawsx2 |
| 16 | Doctor of Poisons | The Doctors | Damage Dealer | 4.08 | 4.08 | 0.314 | sustained: Poisoned Bladex2 |
| 17 | Senshi the Undying | Gifted | Assassin | 3.99 | 3.99 | 0.2 | sustained: Daishōx2 |
| 18 | Zovena Vela | Gifted | Damage Dealer | 3.99 | 4.14 | 0.266 | sustained: Fiery Explosionx1+Fireballx1 |
| 19 | Baba-Yaga | The Guild | Damage Dealer | 3.98 | 5.01 | 0.209 | sustained: spell:Kraken's Breathx1+spell:Blood Drainx1 |
| 20 | Justice | Gifted | Damage Dealer | 3.9 | 3.9 | 0.217 | sustained: Sword of Balancex2 |
