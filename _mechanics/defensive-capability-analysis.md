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

| Role | n | min | p25 | median | p75 | max |
|---|---|---|---|---|---|---|
| Tank | 7 | 20.9 | 22.35 | 23.3 | 24.9 | 33.6 |
| Brawler | 15 | 8.0 | 16.25 | 19.8 | 26.4 | 55.2 |
| Control | 4 | 8.0 | 8.98 | 12.65 | 16.02 | 16.1 |
| Canal Fighter | 24 | 6.7 | 8.6 | 12.55 | 15.7 | 36.8 |
| Sniper | 6 | 10.6 | 11.03 | 12.55 | 13.7 | 18.4 |
| Disruptor | 5 | 4.0 | 7.9 | 11.5 | 13.0 | 16.0 |
| Damage Dealer | 69 | 5.0 | 9.0 | 11.4 | 13.7 | 33.5 |
| Assassin | 10 | 7.3 | 9.8 | 10.3 | 13.55 | 17.0 |
| Line Fighter | 33 | 2.9 | 8.8 | 9.7 | 11.5 | 18.0 |
| Specialist | 38 | 1.8 | 5.6 | 9.7 | 10.6 | 20.6 |
| Support | 42 | 4.5 | 8.8 | 9.7 | 10.6 | 18.0 |
| Harasser | 9 | 3.8 | 4.9 | 8.7 | 9.8 | 15.0 |
| Objective Runner | 12 | 5.0 | 6.7 | 7.7 | 9.33 | 11.3 |

## Durability by faction (median ATK2K vs baseline)

| Faction | n | median ATK2K |
|---|---|---|
| The Vatican | 47 | 11.5 |
| Patricians | 36 | 11.3 |
| Gifted | 31 | 10.6 |
| The Doctors | 42 | 9.8 |
| Rashaar | 41 | 9.7 |
| Strigoi | 36 | 9.7 |
| The Guild | 41 | 9.7 |

## Tankiest 15 models (ATK2K vs baseline)

| Model | Faction | Role | LP | Dex | Prot | ATK2K |
|---|---|---|---|---|---|---|
| Morgraur | Rashaar | Brawler | 45 | 3 | 5 | 55.2 |
| Venetian Heavy Guard | Patricians | Brawler | 15 | 4 | 5 | 47.9 |
| Brachyura | Rashaar | Brawler | 20 | 3 | 7 | 42.6 |
| Emissary of Mother Hydra | Rashaar | Canal Fighter | 30 | 3 | 5 | 36.8 |
| Sepulchral Vanguard | The Vatican | Tank | 13 | 3 | 5 | 33.6 |
| Zovena Vela | Gifted | Damage Dealer | 10 | 4 | 6 | 33.5 |
| Seraph | The Vatican | Damage Dealer | 15 | 4 | 6 | 29.6 |
| Knight of the Holy Sepulchre | The Vatican | Brawler | 18 | 3 | 6 | 28.8 |
| Warden | The Doctors | Tank | 13 | 4 | 4 | 25.3 |
| Rhino | The Doctors | Tank | 20 | 3 | 5 | 24.5 |
| Avignon Guard | The Vatican | Brawler | 15 | 3 | 6 | 24.0 |
| Doctor of Tides | The Doctors | Canal Fighter | 15 | 3 | 6 | 24.0 |
| Knight of Malta | The Vatican | Brawler | 12 | 4 | 4 | 23.3 |
| Giurgiu Guard | Strigoi | Tank | 12 | 4 | 4 | 23.3 |
| Spatar | Strigoi | Tank | 12 | 4 | 5 | 22.9 |

## Vulnerability profile: net LP taken per attack by threat type

Compares each reference attacker. A model whose `penetrator`/`drown` column spikes
relative to `baseline` has a defence that specific threats bypass.

### Most Penetration-vulnerable (highest net_penetrator − net_baseline, Prot ≥ 3)

| Model | Faction | Role | Prot | net base | net pen | delta |
|---|---|---|---|---|---|---|
| Giurgiu Guard | Strigoi | Tank | 4 | 0.51 | 1.89 | 1.38 |
| Knight of Malta | The Vatican | Brawler | 4 | 0.51 | 1.89 | 1.38 |
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
