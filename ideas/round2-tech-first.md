# Round 2: tech-first brainstorm

**Why round 2:** round 1 started from *problems* and let tech be a wrapper. The winner (WellWatch) failed the obvious question: *"so what's the tech — a photo of a strip?"*

**New method:** start from cheap tech that can sense or do something *humans can't*, then cross it with the Lithuanian problems in [`research/local-data.md`](../research/local-data.md).

**Hard filter, the collapse test:** *remove the tech. Does the idea collapse?* If people could do it roughly as well by eye, by hand or with a spreadsheet, the idea fails.

**Also banned:** "phone on a tripod + AI checks your exercise form" (overused), gamified step/points apps, generic dashboards.

## Tech building blocks (all < €50 unless noted)
| Capability | Example part | What it senses that humans can't |
|---|---|---|
| E-nose (AI gas classification) | Bosch **BME688** (~€20) | Smell patterns: VOCs at ppb levels |
| Contact/airborne acoustics + AI | MEMS mic, piezo disc | Sounds too faint or too frequent to notice |
| Deep-UV absorbance | 235/275 nm UV-LED + photodiode | Dissolved chemicals (nitrate) without reagents |
| Fluorescence + AI counting | 395 nm LED + filter + phone/Pi camera | Microplastics (Nile red stain) |
| Thermal imaging | MLX90640 (~€60), FLIR One (~€250) | Heat loss, warm animals |
| Thermistor strings | DS18B20 chain | Ice thickness (the ice/water boundary) |
| Radar | 24/60 GHz mmWave (~€10–30) | Presence, breathing, motion — without a camera |
| Satellite | Sentinel-1 SAR / Sentinel-2 (free) | Ice cover through clouds, vegetation stress |
| Head-tracked spatial audio | Galaxy Buds + Android Spatializer API | Places a sound at a fixed point in 3D space |
| LoRa / NB-IoT | ~€10 radio modules | Sends data kilometres from forests and lakes |

## Idea list

| # | Idea | Tech core | Remove the tech → collapses? | Prior art | Verdict |
|---|---|---|---|---|---|
| R1 | **BeetleNose**: solar sensor nodes on spruce stands *smell* (e-nose) and *hear* (acoustic) a bark-beetle attack weeks before trees visibly die | E-nose AI + acoustics + LoRa | ✅ yes: humans can't smell ppb pheromones or hear larvae | Research only (Czech e-nose 2024, Fraunhofer acoustics); no product for forest owners | 🟢 **finalist** |
| R2 | **SoundCourt**: AI camera + head-tracked spatial audio lets blind/low-vision kids play ball games *with sighted classmates* | Real-time vision AI + 3D audio | ✅ yes for moving targets, the ball, teammates and shot feedback (a beeper on the rim only covers the static hoop) | Navigation sonification research; Google Project Guideline (running); beeper balls | 🟢 **finalist** |
| R3 | **WellWatch 2.0**: build a €50 reagent-free UV nitrate sensor (IoT probe for wells) instead of phone-reading strips | Deep-UV absorbance + IoT + risk model | ✅ yes: continuous in-well measurement is impossible by eye | Research prototypes (235/275 nm LED papers, 2022–26); pro sensors cost €10k+ | 🟢 **finalist** |
| R4 | **Ice-safe 2.0**: buoys measure thickness at a few lakes; a physics model (Stefan's law) + Sentinel-1 SAR ice-on detection + weather estimates thickness on *all* lakes | IoT + satellite + physics/ML | ✅ yes | SmartICE (Arctic), SAR ice-detection research; nothing for LT lakes | 🟡 strong runner-up |
| R5 | **Microplastic scanner**: Nile-red fluorescence + AI particle counting of beach/tap-water samples | Fluorescence + YOLO | ✅ yes | Published $139 device (2025): easy to build, but *what action follows?* | 🟡 good tech, weak "so what" |
| R6 | Turf-crumb runoff from school artificial pitches | — | ❌ rubber crumbs are mm-sized; a sieve and a scale do the job | — | 🔴 |
| R7 | **Smoke fingerprint**: e-nose network tells wood smoke from burning plastic/garbage in private-house districts | E-nose AI | ✅ yes | Polish police drones with lab-grade sensors (Katowice, Kraków) | 🟡 ethics (neighbour surveillance), outdoor dilution |
| R8 | Thermal drone fawn/corncrake rescue before mowing | Thermal + AI | ✅ yes | Mature in Germany (state-funded, 20× more fawns saved) | 🔴 just a transfer; hardware €€€ |
| R9 | **Thermal city scan**: thermal survey of every Soviet block + AI heat-loss ranking → personal letter for the renovation vote | Thermal + AI | ✅ mostly | Aerial heat-loss maps (UK and others) | 🟡 |
| R10 | **Ghost pacer**: LED strip along the school track/corridor races you against your previous self in PE running tests | LEDs + timing | ✅ yes | Wavelight (elite athletics) | 🟡 fun, shallow problem |
| R11 | Camera-free PE analytics with mmWave radar (privacy-safe activity measurement) | Radar AI | ✅ yes | Research | 🔴 "measure activity" isn't a problem people feel |
| R12 | Drowning alarm at unsupervised lakes (pole camera/AI) | Vision AI | ✅ yes | Pool systems (Poseidon), beach drones | 🔴 LT drownings are mostly drunk adults; privacy |
| R13 | Smart pheromone-trap counter (camera counts beetles in the State Forest Service's traps) | Vision + IoT | ✅ yes | Trapview & co. in agriculture | 🟡 merge into R1 as a feature |
| R14 | Bee-hive acoustic health (swarming, queen loss) | Audio AI | ✅ | BeeHero, Arnia (commercial) | 🔴 exists |
| R15 | Textile fibre ID for recycling (phone microscope or NIR) | Optics + AI | ✅ | Matoha, Fibersort; cheap NIR range too narrow for fibres | 🔴 feasibility |
| R16 | VR/AR telepresence PE for chronically ill kids in hospital | VR + robot | ✅ | AV1 school robot (No Isolation) | 🔴 complex, small |
| R17 | Wristband submersion alarm for kids at lakes | Pressure sensor + LoRa | ✅ | WAVE, Sentag | 🔴 exists |

## Scoring (tech-weighted)

Weights changed after round 1: **T 4, B 3**, C 4, Q 4, L 4, I 3, R 2, D 2, S 1 (sum 27 → ×100/135).

| Idea | T | B | C | Q | L | I | R | D | S | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|
| **BeetleNose** | 5 | 5 | 5 | 3 | 5 | 4 | 3 | 4 | 5 | **87** |
| **WellWatch 2.0** | 4 | 4 | 4 | 4 | 5 | 5 | 4 | 4 | 4 | **85** |
| **SoundCourt** | 5 | 5 | 5 | 3 | 3 | 4 | 3 | 4 | 5 | **81** |
| Ice-safe 2.0 | 5 | 5 | 4 | 3 | 4 | 3 | 3 | 4 | 5 | 79 |
| *(for comparison) WellWatch 1.0, honest tech score* | 3 | 2 | 4 | 5 | 5 | 5 | 4 | 5 | 4 | 82 |
| *(for comparison) KneeGuard* | 4 | 4 | 2 | 4 | 4 | 4 | 4 | 4 | 3 | 72 |
