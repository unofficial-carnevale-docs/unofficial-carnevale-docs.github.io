---
title: "Defensive Capability Analysis"
description: Raw defensive capability data analysis
nav_order: 4
is_analysis: true
---

## Units and method

Metric: [**ATK2K**](/mechanics/combat/) (Attacks-To-Kill = LP ÷ expected net LP lost per incoming attack)

This is the EHP-equivalent survivability number, folding LP, Dexterity, Protection, Parry, and Universal Shielding. Higher = tankier.
Baseline column uses the baseline reference attacker (Attack 3). `net_*` = expected LP lost per attack from each reference attacker.

See [Combat Capabilities Calculations](/mechanics/combat/) for method and calibration.

## Role standards (ATK2K vs baseline attacker)

| Role | n | min | p25 | median | p75 | max | ATK2K/ducat med |
|---|---|---|---|---|---|---|---|
| Tank | 6 | 20.9 | 22.07 | 23.7 | 25.1 | 33.6 | 1.53 |
| Brawler | 17 | 13.2 | 18.4 | 21.0 | 26.3 | 55.2 | 1.32 |
| Control | 4 | 8.0 | 8.98 | 12.65 | 16.02 | 16.1 | 0.67 |
| Canal Fighter | 24 | 6.7 | 8.6 | 12.55 | 15.7 | 36.8 | 0.8 |
| Sniper | 6 | 10.6 | 11.03 | 12.55 | 13.7 | 18.4 | 1.12 |
| Disruptor | 6 | 4.0 | 8.8 | 12.25 | 15.25 | 29.6 | 0.82 |
| Damage Dealer | 66 | 5.0 | 8.93 | 10.75 | 13.7 | 22.9 | 0.73 |
| Assassin | 10 | 7.3 | 9.8 | 10.3 | 13.55 | 17.0 | 0.59 |
| Line Fighter | 34 | 2.9 | 8.8 | 9.7 | 11.5 | 23.3 | 0.97 |
| Specialist | 38 | 1.8 | 5.6 | 9.7 | 10.6 | 20.6 | 0.69 |
| Support | 42 | 4.5 | 8.8 | 9.7 | 10.6 | 18.0 | 0.75 |
| Harasser | 9 | 3.8 | 4.9 | 8.7 | 9.8 | 15.0 | 0.75 |
| Objective Runner | 12 | 5.0 | 6.7 | 7.7 | 9.33 | 11.3 | 0.79 |

## Durability by faction (median ATK2K vs baseline)

| Faction | n | median ATK2K | median ATK2K/ducat |
|---|---|---|---|
| The Vatican | 47 | 11.5 | 0.97 |
| Patricians | 36 | 11.3 | 0.97 |
| Gifted | 31 | 10.6 | 0.69 |
| The Doctors | 42 | 9.8 | 0.82 |
| Rashaar | 41 | 9.7 | 0.78 |
| Strigoi | 36 | 9.7 | 0.66 |
| The Guild | 41 | 9.7 | 0.81 |

## Tankiest 15 models (ATK2K vs baseline)

| Model | Faction | Role | LP | Dex | Prot | ATK2K | ATK2K/ducat |
|---|---|---|---|---|---|---|---|
| Morgraur | Rashaar | Brawler | 45 | 3 | 5 | 55.2 | 0.81 |
| Venetian Heavy Guard | Patricians | Brawler | 15 | 4 | 5 | 47.9 | 2.99 |
| Brachyura | Rashaar | Brawler | 20 | 3 | 7 | 42.6 | 2.37 |
| Emissary of Mother Hydra | Rashaar | Canal Fighter | 30 | 3 | 5 | 36.8 | 0.72 |
| Sepulchral Vanguard | The Vatican | Tank | 13 | 3 | 5 | 33.6 | 2.24 |
| Seraph | The Vatican | Disruptor | 15 | 4 | 6 | 29.6 | 1.74 |
| Knight of the Holy Sepulchre | The Vatican | Brawler | 18 | 3 | 6 | 28.8 | 1.69 |
| Gethsemane | The Vatican | Brawler | 28 | 4 | 0 | 26.3 | 0.71 |
| Warden | The Doctors | Tank | 13 | 4 | 4 | 25.3 | 1.95 |
| Rhino | The Doctors | Tank | 20 | 3 | 5 | 24.5 | 1.63 |
| Avignon Guard | The Vatican | Brawler | 15 | 3 | 6 | 24.0 | 1.71 |
| Doctor of Tides | The Doctors | Canal Fighter | 15 | 3 | 6 | 24.0 | 1.33 |
| Knight of Malta | The Vatican | Brawler | 12 | 4 | 4 | 23.3 | 1.66 |
| Giurgiu Guard | Strigoi | Line Fighter | 12 | 4 | 4 | 23.3 | 1.79 |
| Spatar | Strigoi | Tank | 12 | 4 | 5 | 22.9 | 1.43 |

## Best durability value (top 15 by ATK2K/Ducat)

The per-Ducat counterpart to Tankiest — most survivability per point spent.

| Model | Faction | Role | cost | ATK2K | ATK2K/ducat |
|---|---|---|---|---|---|
| Venetian Heavy Guard | Patricians | Brawler | 16 | 47.9 | 2.99 |
| Brachyura | Rashaar | Brawler | 18 | 42.6 | 2.37 |
| Sepulchral Vanguard | The Vatican | Tank | 15 | 33.6 | 2.24 |
| Warden | The Doctors | Tank | 13 | 25.3 | 1.95 |
| Giurgiu Guard | Strigoi | Line Fighter | 13 | 23.3 | 1.79 |
| Seraph | The Vatican | Disruptor | 17 | 29.6 | 1.74 |
| Avignon Guard | The Vatican | Brawler | 14 | 24.0 | 1.71 |
| Knight of the Holy Sepulchre | The Vatican | Brawler | 17 | 28.8 | 1.69 |
| Knight of Malta | The Vatican | Brawler | 14 | 23.3 | 1.66 |
| Rhino | The Doctors | Tank | 15 | 24.5 | 1.63 |
| Spatar | Strigoi | Tank | 16 | 22.9 | 1.43 |
| Hippogryph | The Doctors | Harasser | 7 | 9.8 | 1.4 |
| Cult Enforcer | Rashaar | Brawler | 14 | 19.5 | 1.39 |
| City Guard | Patricians | Line Fighter | 10 | 13.7 | 1.37 |
| Hired Muscle | Patricians | Brawler | 11 | 14.9 | 1.35 |

## Vulnerability profile: net LP taken per attack by threat type

Compares each reference attacker. A model whose `penetrator`/`drown` column spikes
relative to `baseline` has a defence that specific threats bypass.

### Most Penetration-vulnerable (highest net_penetrator − net_baseline, Prot ≥ 3)

| Model | Faction | Role | Prot | net base | net pen | delta |
|---|---|---|---|---|---|---|
| Knight of Malta | The Vatican | Brawler | 4 | 0.51 | 1.89 | 1.38 |
| Giurgiu Guard | Strigoi | Line Fighter | 4 | 0.51 | 1.89 | 1.38 |
| Warden | The Doctors | Tank | 4 | 0.51 | 1.89 | 1.38 |
| Bishop Guard | The Vatican | Line Fighter | 4 | 0.67 | 1.89 | 1.22 |
| Baba-Yaga | The Guild | Damage Dealer | 3 | 1.36 | 2.5 | 1.14 |
| Beggar | The Guild | Objective Runner | 3 | 1.36 | 2.5 | 1.14 |
| Blood Courier | The Guild | Support | 3 | 1.36 | 2.5 | 1.14 |
| Celestial Congregation | The Vatican | Support | 3 | 1.36 | 2.5 | 1.14 |
| Cetean Upiór | Strigoi | Canal Fighter | 3 | 1.36 | 2.5 | 1.14 |
| Mature Kraken | Rashaar | Control | 3 | 1.36 | 2.5 | 1.14 |
| Salaacia | Rashaar | Canal Fighter | 3 | 1.36 | 2.5 | 1.14 |
| Strigoi Sluger | Strigoi | Damage Dealer | 3 | 1.36 | 2.5 | 1.14 |
