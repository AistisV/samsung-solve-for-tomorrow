# Scout report: Nature, forests, biodiversity, wildlife and climate adaptation (Lithuania)

> Scout: nature domain, round 3. Date: 2026-09-25.
> **Research caveat:** the shared WebSearch budget ran out partway through, and WebFetch was blocked for almost every domain (lrv.lt, vialietuva.lt, ncbi, transportecology…). Every number below with a link came from search-result snippets of that source. Anything marked **[unverified]** comes from my background knowledge of the literature and **must be checked before it goes on a slide**.

---

## 0. TL;DR

| Rank | Idea | One line |
|---|---|---|
| **1 (strongest)** | **BriedisStop**: edge-AI thermal "animal on the road" warning at wildlife-fence ends and crossings | A thermal camera and on-device AI see a moose or deer at the verge at night. A warning sign flashes only then. The same unit logs every crossing, so Via Lietuva learns which of its fences, underpasses and green bridges work. |
| 2 | **ŽalosDronas**: drone and AI measurement of game-animal crop damage for municipal commissions | LT's 2025 damage methodology already *allows* drones. We turn one drone flight into a measured damage map, a € figure and a filled-in commission report. |
| 3 | **Šernų skaitliukas**: camera-trap AI census for hunting clubs (ASF / game management) | Hunters already own trail cameras. AI sorts thousands of photos, and the Random Encounter Model (validated by EFSA/ENETWILD) turns them into a real density for each species. That replaces snow-track counts that critics call "pointless". |
| 4 | **BarštisScan**: phone-on-dashboard AI that maps Sosnowsky's hogweed from municipal and road-maintenance vehicles | Vehicles that already drive every road survey the roadsides for free. Municipalities get a live map of colonies and can check whether treated sites grow back. |
| 5 | **PelkėsPulsas**: satellite and logger verification of peatland rewetting for the Nature Restoration Law | Sentinel-1/2 plus a few cheap water-level loggers show whether a rewetted peatland is actually wet, then convert that into tonnes of CO₂ avoided. |

---

## 1. Key Lithuanian evidence gathered

| Fact | Source |
|---|---|
| Police-registered wildlife–vehicle collisions rose from **342 (2017) to 1,000 (2025)**. Roe deer are **53%** of cases. Moose cases are few but the costliest (average insured damage **>€5k**). May 2025: ~100 cases, >€290k damage (BTA). Record **119 cases in Dec 2025**. Total insured damage **>€5M**, and the number of claims grew by almost a fifth in 2025. | [Reidas Official / Via Lietuva](https://reidasofficial.lt/eismas/gyvunai-kelyje-pavasaris-lietuva-kaip-isvengti-susidurimo/), [77.lt](https://77.lt/susidurimu-su-laukiniais-gyvunais-zala-virsijo-5-mln-euru), [Alkas 2025-10](https://alkas.lt/2025/10/04/daugeja-susidurimu-su-gyvunais-i-ka-svarbiausia-atkreipti-demesi/) |
| Research: wild animals cause **~4,000 traffic accidents/yr** in LT (wider definition than police-registered), with **30–40 injured and ~1 killed per year**. **Moose cause 66.7% of the deaths and 47.2% of the injuries** despite low numbers. Since 2018 wildlife accidents outnumber other transport-accident types [per snippet]. | [MDPI Animals 2024 / PubMed 38791668](https://pubmed.ncbi.nlm.nih.gov/38791668/) |
| 2002–2017: 14,989 ungulate–vehicle collisions (1,434 moose, 258 red deer, 11,788 roe deer, 1,509 wild boar). Dataset is public on Mendeley. | [ScienceDirect 2020](https://www.sciencedirect.com/science/article/abs/pii/S0301479720310975), [Mendeley data](https://data.mendeley.com/datasets/4y8t78dsxy/2) |
| Via Lietuva: fences now cover the A2 and most of the A1. **~90 km more in 2026** (A1 146–205 km, A6 134–166 km). Tools already in use: green bridges, underpasses, amphibian systems and **variable message signs**. Regional roads are now getting projects too. | [Via Lietuva](https://vialietuva.lt/naujienos/via-lietuva-plecia-apsaugos-sistemas-nuo-laukiniu-gyvunu-siemet-ju-bus-irengta-dar-apie-90-kilometru), [Alkas 2026-07](https://alkas.lt/2026/07/17/keliuose-pleciamos-apsaugos-sistemos-nuo-laukiniu-gyvunu/) |
| **ASF in wild boar**, Q1 2025: **939 cases in 22 municipalities**, 885 of them in carcasses. **Panevėžys district: 616**. Farm outbreaks include 19,672 pigs (Vilnius distr., Oct 2024) and 381 (Radviliškis, 2025). Weekly carcass searches run in affected zones. In LV/EE, carcass finds dropped after carcass payments stopped. | [LRT](https://www.lrt.lt/naujienos/lietuvoje/2/2898201/lietuvoje-tarp-sernu-plinta-afrikinis-kiauliu-maras-virusas-nustatytas-22-savivaldybese), [jp.lt](https://jp.lt/panevezio-rajone-plinta-afrikinis-kiauliu-maras-skaiciai-didziausi-salyje/), [ŽŪR/VMVT](https://zur.lt/informuoja-vmvt/) |
| Hunters' counts: **28,096 wild boar** at the start of 2023. Critics say the counts are very inaccurate and the error margin is never published ("Beprasmės pildomos žvėrių apskaitos"). The census is mandatory for hunting-ground users. | [AM](https://am.lrv.lt/lt/naujienos/medziojamuju-gyvunu-apskaita-visus-metus), [Miške.lt](https://www.miske.lt/straipsniai/beprasmes-pildomos-zveriu-apskaitos/), [Šilokarčema](https://www.silokarcema.lt/naujiena/13005_priminimas-medziotojams-privalu-atlikti-medziojamuju-gyvunu-apskaita.html) |
| **Game-damage methodology updated 2025-01-01**: commissions **may now use drones** to assess crop damage. The Kaunas district seeks "innovative solutions… drones, independent agronomists". VDU Agriculture Academy (K. Šimkevičius) says the current method is flawed, is read differently by different specialists (especially for irregular patches) and **leads to lost court disputes**. Hunting clubs pay for ungulate damage. There is a simplified farmer↔club negotiation step, with the municipal commission if they can't agree. Kėdainiai: >€100k damage (≈€62k owed by hunting clubs). A **€360k** 2026 state programme covers protected-species damage. A minister said in 2026 that "hunters, not farmers, must compensate". | [AM](https://am.lrv.lt/lt/naujienos/medziojamu-gyvunu-padaryta-zala-bus-nustatoma-tiksliau/), [ŽŪM](https://zum.lrv.lt/lt/naujienos/ukininko-laukuose-isbandyta-kaip-veikia-atnaujinta-medziojamuju-gyvunu-padarytos-zalos-vertinimo-metodika/), [Mano ūkis](https://manoukis.lt/naujienos/aplinka-miskai/laukiniu-gyvunu-padarytai-zalai-nustatyti-siulo-naudoti-dronus), [rinkosaikste](https://rinkosaikste.lt/kedainiu-krasto-ukininkams-zveriu-padaryta-zala-perkope-100-tukst-euru/), [LRT](https://www.lrt.lt/naujienos/verslas/4/2950303/ministras-laukiniu-gyvunu-padaryta-zala-turi-kompensuoti-medziotojai-o-ne-zemdirbiai), [APVA call 2026-02](https://apvis.apva.lt/paskelbti_kvietimai/medziojamu-gyvunu-padarytos-zalos-kompensaciju-ismokejimas-2026-02) |
| Beavers: **40–50k** counted (likely more). **15,218 km** of regulated streams and drainage ditches. Beavers dam them and re-waterlog land. Skuodas district spends **~€200k/yr** on ditch maintenance, which covers only ~10 km. | [Jonavos žinios / BNS](https://www.jonavoszinios.lt/naujiena/bebrai-gamtos-inzinieriai-kuriu-pavasarine-veikla-kelia-issukiu), [Ūkininko patarėjas](https://ukininkopatarejas.lt/naujienos/melioracijos-griovius-uztvenkia-bebrai-ir-gamtosaugininkai/) |
| Forest fires: VMU runs 82 detectors, 23 centres and 20 towers. It is **building a new AI system with 151 detectors, fully live by end of 2027** → a saturated space for us. | [15min](https://www.15min.lt/naujiena/aktualu/lietuva/miskininkai-diegia-vieninga-gaisru-stebejimo-sistema-aptiksiancia-ju-zidinius-56-2660384), [Bernardinai](https://www.bernardinai.lt/lietuvoje-didelis-misko-gaisru-pavojus-valstybiniu-misku-uredijos-miskininkai-dorojasi-su-issukiu/) |
| EU Nature Restoration Law: **national restoration plans due 1 Sep 2026**. Drained peatlands under agricultural use: restore **30% by 2030** (a quarter rewetted), 40% by 2040 and 50% by 2050. LT RRF: **€16M for 8,000 ha** of agricultural drained peatland by 2026. LT is called an "EU frontrunner" in peatland recovery. | [EC](https://environment.ec.europa.eu/topics/nature-and-biodiversity/nature-restoration-regulation_en), [Succow/DESIRE](https://www.succow-stiftung.de/fileadmin/Ablage/Dokumente/DESIRE/RRF_measure_final.pdf), [Greifswald Mire Centre](https://greifswaldmoor.de/news/lithuania-eu-frontrunner-in-peatland-recovery.html) |
| Hogweed: Environment Ministry gave municipalities >€0.5M. State/municipal land only; private plots excluded [older programme]. Applications were so low the deadline was extended. "Millions for hogweed unreachable". Municipalities had to report infested hectares. See also local-data.md: 166 ha cleared in state forests 2025 and a new 2025–29 programme that includes private owners. | [15min](https://www.15min.lt/verslas/naujiena/agronaujienos/aplinkos-ministerija-savivaldybems-skyre-puse-milijono-euru-sosnovskio-barsciui-naikinti-313-1418326), [Valstietis](https://www.valstietis.lt/telsiu/milijonai-sosnovskio-barsciui-naikinti-nepasiekiami/108756), [LRT](https://www.lrt.lt/naujienos/lietuvoje/2/1198660/nesulaukus-paraisku-del-sosnovskio-barsciu-naikinimo-pratestas-ju-priemimas), [15min 2026](https://www.15min.lt/verslas/naujiena/nt-ir-interjeras/pavojingu-invaziniu-augalu-naikinimas-pleciamas-juos-salins-ir-privaciuose-sklypuose-971-2727826) |
| TBE: LT has the **highest incidence in Europe** (12.9/100k in 2022). **642 cases in 2025**. Vaccine effectiveness 99.6%. | [ScienceDirect 2025](https://www.sciencedirect.com/science/article/pii/S2772707625001626), [LRT](https://www.lrt.lt/en/news-in-english/19/1085913/lithuania-reports-highest-tick-borne-encephalitis-spread-in-europe) |

---

## 2. Long list: 26 ideas, filtered

Criteria abbreviations: **C** = collapse test, **A** = adoption loop, **P** = proven blocks, **M** = measurable, **S** = not saturated, **D** = demo in 6 weeks, **L** = local evidence.

| # | Idea | Verdict | One-line reason |
|---|---|---|---|
| 1 | **BriedisStop**: thermal camera + edge AI at fence ends and crossings flashes a sign only when an animal is at the verge, and logs crossings | **KEEP (#1)** | Passes all 7. One deployer (Via Lietuva) and a handful of units at known hotspots. RADS is proven abroad. Best live-demo wow. |
| 2 | **ŽalosDronas**: drone orthophoto → AI damage segmentation → € and a commission report per the 2025 LT methodology | **KEEP (#2)** | The law already allows drones, and a named municipality is asking for this. Collapse is clear (hand-measuring irregular patches). Weakest on "green" framing. |
| 3 | **Šernų skaitliukas**: camera-trap AI species ID + REM density for hunting clubs' mandatory census and ASF | **KEEP (#3)** | Cameras are already deployed by hunters, and REM is EFSA-validated. Prior art exists (Agouti, Wildlife Insights), so novelty is the LT census/ASF integration. |
| 4 | **BarštisScan**: phone on the dashboard of municipal/road-maintenance vehicles detects hogweed and builds a map + regrowth check | **KEEP (#4)** | Deployment is free (vehicles already drive). Seasonal risk: the Oct–Nov pilot has to use dead stalks and rosettes. |
| 5 | **PelkėsPulsas**: Sentinel-1/2 + loggers to verify rewetting and estimate CO₂ for NRL reporting | **KEEP (#5)** | Strong policy hook (NRL plan, RRF 8,000 ha) and real historical pilot data are possible. Low wow, dashboard-only. |
| 6 | Thermal-drone + AI boar-carcass search for ASF zones | Kill (runner-up) | Proven (Rietz 2023, ≤80% detection in open habitat above 3 °C), but it fails under canopy and in cold. There are no carcasses to pilot on, and thermal drones cost several thousand € (price unverified). |
| 7 | Beaver-dam detector on the national orthophoto + Sentinel for drainage-ditch triage (keep the dam as NRL wetland, or clear it) | Kill (honourable mention) | A creative conflict→restoration angle. But deep-learning beaver-dam detection is only partly proven **[unverified]** and the buyer (municipal melioration) is poorly funded. |
| 8 | Camera-trap AI monitoring of Via Lietuva green bridges and underpasses (effectiveness reports) | Merged into #1 | Same hardware and customer. It's the "monitoring mode" of BriedisStop. |
| 9 | Dashcam AI on municipal fleets auto-detects roadkill (ASF reporting + hotspot map) | Kill | Useful data layer, but the adoption loop is weak and the action for road carcasses is unclear. Could be folded into #1/#4 later. |
| 10 | Hotspot/time risk model pushed to navigation apps (Waze-style wildlife alerts) | Kill | Collapse test is weak: a hotspot map is spreadsheet-able, and static warnings are known to habituate drivers. |
| 11 | AI pheromone-trap beetle counter (phone photo of the trap cup) for bark-beetle monitoring | Kill | Close to a wrapper: foresters estimate by volume (ml) anyway. |
| 12 | Sentinel-2 bark-beetle "red/grey-attack" early map for private forest owners | Kill | Saturated: many commercial and state services, and VMU likely has one **[unverified]**. |
| 13 | AI fire-smoke cameras | Kill | VMU is already building a 151-detector AI system (live 2027). |
| 14 | Sentinel-1 windthrow mapping after storms | Kill | Mature science. Users (VMU) have in-house GIS. No wow. |
| 15 | BirdNET bioacoustics on upcycled Galaxy phones for NRL bird indicators and migration counts | Kill (close) | Proven tech, cool Samsung angle (old phones) and October night-migration data is possible. But nobody clearly *pays* or *acts* on the output. |
| 16 | Bat acoustic smart curtailment for LT's new wind farms | Kill | Commercial products exist (e.g. ProBat **[unverified]**), and developers buy from them, not students. |
| 17 | AI insect camera for municipal "no-mow" meadows (pollinator evidence) | Kill | Great NRL link (pollinator article), but zero pollinators in Oct–Nov means no pilot data before Nov 6. |
| 18 | Smart trap alerts (LoRa) for invasive raccoon dog / American mink in bird-colony reserves | Kill | Proven (NZ predator-free traps **[unverified]**), but the LT user base is tiny and the collapse test is soft. |
| 19 | Amphibian-migration night predictor for volunteer patrols | Kill | Temperature + rain rule = spreadsheet. Fails collapse. |
| 20 | Tick/TBE risk forecast app or AI tick-photo ID | Kill | Wrapper and saturated. The TBE fix is vaccination (99.6% effective), not tech. |
| 21 | Stork-nest detection on ESO power poles from inspection imagery | Kill | ESO's own contractors do inspection AI. No student leverage. |
| 22 | Bird–glass collision audit of bus stops/noise barriers via AI | Kill | The fix (stickers/patterns) doesn't need AI. Collapse fails. |
| 23 | Light-pollution mapping by phone/night-sky camera | Kill | Weak action loop, and satellite VIIRS data already exists. |
| 24 | Urban tree canopy/heat inventory from street view | Kill | Saturated (i-Tree, many city tools). |
| 25 | Acoustic chainsaw detection vs illegal logging | Kill | Illegal logging is not a major LT problem. Rainforest Connection is already the prior art. |
| 26 | Thermal "human-in-line-of-fire" alert for hunters (hunting accidents) | Kill | Thermal scopes already exist, and the liability is scary. |
| 27 | AI wildlife-damage forecasting for forest plantations (browsing by moose/deer) | Kill | Needs years of data. Hard to demo. |

---

## 3. Detailed profiles

### #1 BriedisStop: a warning that only lights up when a moose is actually there

**One-line pitch:** A €300–600 **[estimate, unverified]** thermal-AI unit at the end of a wildlife fence or at a crossing sees a moose or deer approaching the road at night and flashes a warning sign within a second. Drivers slow down because the sign is only ever lit when an animal is really there. The same unit reports every crossing to Via Lietuva.

**Problem (LT evidence):**
- Police-registered wildlife collisions tripled from **342 (2017) to 1,000 (2025)**, with a record 119 in Dec 2025 ([Reidas/Via Lietuva](https://reidasofficial.lt/eismas/gyvunai-kelyje-pavasaris-lietuva-kaip-isvengti-susidurimo/)). Insured damage is **>€5M** ([77.lt](https://77.lt/susidurimu-su-laukiniais-gyvunais-zala-virsijo-5-mln-euru)).
- Research counts ~4,000 wildlife accidents a year. **Moose cause two-thirds of the deaths** ([PubMed 38791668](https://pubmed.ncbi.nlm.nih.gov/38791668/)).
- Via Lietuva's answer is fences (~90 km more in 2026). But fences cannot go everywhere: junctions, driveways and regional roads stay open, and **animals funnel around fence ends**, a well-known hotspot effect in road ecology **[unverified in this session; check Huijser / Swedish Trafikverket studies]**. Static "deer" signs are ignored because they are always on.

**What the tech does / why it collapses without it:**
- A cheap thermal sensor (e.g. FLIR Lepton 3.5 or MLX90640-class) plus an RGB camera feeds a Raspberry Pi 5 / Jetson running YOLO. The model classifies moose, deer, boar, human and car within ~50–150 m **[range to be measured in pilot]**.
- It triggers the LED sign (or Via Lietuva's existing variable message sign) and logs species, time and direction to a dashboard.
- **Collapse:** no human can watch 50 road verges every night, and a PIR sensor alone false-triggers on cars and warm air. Without AI, you are back to the static sign drivers already ignore.

**Adoption loop:** Driver sees a flashing sign that is only lit when an animal is present → slows down → fewer and less severe collisions. **Who deploys/pays:** Via Lietuva (state road manager, already budgets for wildlife protection and already runs variable message signs). Secondary payers: municipalities for regional roads, and insurers (BTA etc., who publish the damage figures) as co-funders or PR partners. **How it reaches them:** Via Lietuva already publishes collision hotspots and fence projects. We pitch "put 10 units at the 10 worst fence ends". **First partner to approach:** Via Lietuva's road-safety / environment unit. Scientific partner: Nature Research Centre (Gamtos tyrimų centras, authors of the LT collision papers).

**Where the core tech is proven:**
- Roadside Animal Detection Systems (RADS) cut vehicle speeds in Florida's Big Cypress (peak season) ([ScienceDirect 2017](https://www.sciencedirect.com/science/article/abs/pii/S0001457517303597)).
- Sweden has evaluated animal-detection + driver-warning systems on secondary roads ([Transport Ecology](https://transportecology.info/research/effectivness-addws-in-sweden)).
- A review of sensor/ML systems for wildlife collisions exists ([PMC9003022](https://pmc.ncbi.nlm.nih.gov/articles/PMC9003022/)).
- Thermal + YOLOv8n roadside animal detection was evaluated in *Sensors* 2025 ([PMC12473846](https://pmc.ncbi.nlm.nih.gov/articles/PMC12473846/)).
- **[unverified]**: widely cited reviews (Huijser et al.) report collision reductions of roughly 33–97% for working detection systems. The EU Biodiversity & Infrastructure handbook covers driver warnings ([handbook 5.3](https://www.biodiversityinfrastructure.org/handbook/5-solutions/5-3-driver-warnings/)).

**Prior art and how ours differs:** Commercial systems (break-beam, radar, thermal) exist in the US, Switzerland and Scandinavia. They are expensive and not in LT. Ours differs in three ways:
- (a) a low-cost edge-AI unit that tells species apart, so a moose alert can be more urgent than a roe-deer one;
- (b) it's placed specifically at **fence ends and gaps of LT's growing fence network**;
- (c) **dual use**: the same unit monitors how well Via Lietuva's underpasses and green bridges work. Today that needs manual camera-trap review.

**Measurable impact + pilot by Nov 6:**
- *Pilot (legal, no sign needed):* mount 2 units (thermal + ordinary trail camera as ground truth) at a known crossing near a forest road or school land for 3–4 weeks in October (peak rut/dusk activity).
- *Metrics:* detection precision/recall against the trail camera, detection range, false alarms per night, crossings per night by species.
- *Optional:* radar-gun speed of cars with a demo sign lit vs unlit on a private/closed road.
- *Deployment metric:* collisions per km per year at treated fence ends vs the police/insurer baseline.

**Demo:** A thermal feed on screen. A warm "moose" (a heated dummy, or a team member walking on all fours) enters the frame → a bounding box with "MOOSE 0.91" appears → a mini road sign flashes → the dashboard logs it. Then show a map of real pilot detections from the October forest.

**Top 3 judge risks and answers:**
1. *"Detection systems have mixed results. Drivers still don't slow down."* The evidence says the effect is strongest when the warning is *credible* (only on when an animal is there) and paired with a temporary speed limit. We would integrate with Via Lietuva's existing variable speed signs, and our pilot measures false-alarm rate precisely because credibility is everything.
2. *"Weather, snow and maintenance."* Thermal works in the dark and in fog. Snow downtime is documented (one US system had 40% downtime in a snowstorm), so we budget for it and self-report sensor health to the dashboard. Units are solar + LTE, the same class as existing traffic counters.
3. *"Why not just more fences?"* Fences are the backbone, and we're not replacing them. We protect exactly the places where a fence can't go (ends, junctions, regional roads), and we tell Via Lietuva which crossings animals actually use.

**Self-score (1–10):** Collapse 8 · Adoption 7 · Proven 8 · Measurable 8 · Not saturated 7 (not in LT and not student-typical, but commercial prior art exists abroad) · Demo 9 · Local evidence 9. AI + IoT bonus: yes.

---

### #2 ŽalosDronas: fair, fast measurement of wildlife crop damage

**One-line pitch:** One drone flight over a field damaged by boar or deer becomes, in minutes, a map of every damaged m², a € amount computed by the official 2025 methodology and a pre-filled report for the municipal commission. The figure is neutral enough that farmers and hunting clubs stop fighting in court.

**Problem (LT evidence):**
- Hunting clubs must compensate farmers for ungulate damage, and the Minister publicly insisted on this in 2026 ([LRT](https://www.lrt.lt/naujienos/verslas/4/2950303/ministras-laukiniu-gyvunu-padaryta-zala-turi-kompensuoti-medziotojai-o-ne-zemdirbiai)).
- The 2025-01-01 methodology **explicitly allows drones** ([ŽŪM](https://zum.lrv.lt/lt/naujienos/ukininko-laukuose-isbandyta-kaip-veikia-atnaujinta-medziojamuju-gyvunu-padarytos-zalos-vertinimo-metodika/), [AM](https://am.lrv.lt/lt/naujienos/medziojamu-gyvunu-padaryta-zala-bus-nustatoma-tiksliau/)). Kaunas district says it is looking for innovative drone-based solutions.
- A VDU scientist says the manual method is read differently by different people on irregular patches, which leads to lost court cases ([Mano ūkis](https://manoukis.lt/naujienos/aplinka-miskai/laukiniu-gyvunu-padarytai-zalai-nustatyti-siulo-naudoti-dronus)).
- Scale example: Kėdainiai >€100k per year ([rinkosaikste](https://rinkosaikste.lt/kedainiu-krasto-ukininkams-zveriu-padaryta-zala-perkope-100-tukst-euru/)). A national total was not found **[gap]**.

**What the tech does / collapse:**
- A consumer drone (DJI Mini-class) flies an automatic grid → photogrammetry (OpenDroneMap) builds the orthomosaic.
- A segmentation model (U-Net / YOLO-seg) marks damaged vs healthy crop or rooted grassland → damaged area × crop yield × price per methodology → PDF act.
- **Collapse:** a commission walking an irregular 20 ha maize field with tape measures cannot measure scattered patches accurately. That is the documented source of the disputes.

**Adoption loop:** A farmer files a claim → the municipal commission (all 60 municipalities have one) flies the drone or orders a flight → objective area + € → the hunting club accepts or disputes with data. **Payer:** the municipality (a per-assessment service fee, or it buys the software). Hunting clubs and the Hunters' and Fishers' Association benefit from fewer inflated claims. Farmers get paid faster. **First partner:** Kaunas district municipality (public call for innovation). Scientific partner: VDU Agriculture Academy (Šimkevičius).

**Proven:** Belgium's drone assessment of boar damage ([Rutten 2018, Wildlife Soc. Bull.](https://wildlife.onlinelibrary.wiley.com/doi/abs/10.1002/wsb.916), [ScienceDaily](https://www.sciencedaily.com/releases/2017/12/171212141841.htm)). US corn ([Friesenhahn 2023](https://wildlife.onlinelibrary.wiley.com/doi/10.1002/wsb.1437)). Maize: DL accuracy 92.9% / DSM 94.7% ([Agronomy 2025](https://doi.org/10.3390/agronomy15010238)). GEOBIA 84.5% maize, 94.4% grassland ([Agriculture 2023](https://www.mdpi.com/2077-0472/13/8/1627)).

**Prior art / difference:** Commercial drone damage services exist in Germany **[unverified, likely]**, and VDU researchers have proposed the idea. What's new: an end-to-end tool that outputs the **LT-methodology-compliant act** (the legal form commissions must file) and handles LT crops (maize, winter cereals, rapeseed, grassland rooting).

**Metric + pilot:** In October, boar rooting in meadows/stubble and late maize is common. Fly 3–5 real damaged plots with a local hunting club or farmer and compare AI area vs a careful GPS-walk ground truth. Metrics: area error %, time per assessment (hours → minutes), € difference vs the manual estimate.

**Demo:** Upload a real flight from the pilot on stage → the damage heat-map and a € figure appear in about 60 seconds. Optionally fly a small drone indoors over a printed "field" with damage patches.

**Risks:**
1. *"Is this sustainability?"* It is human–wildlife coexistence: fair compensation reduces illegal killing and pressure to overcull, and the damage data feeds hunting quotas and boar management (ASF). But it's honestly the weakest "green" link of the five.
2. *"Drone rules."* EU Open category A1/A3 needs an online certificate, which a 16+ student or the teacher can get **[check LT TKA rules]**. Farmland is not restricted, except near the border and military areas.
3. *"Commissions won't trust student AI."* The output keeps the methodology's 1 m² control plots for verification, and the AI only speeds up the area measurement.

**Self-score:** Collapse 8 · Adoption 8 · Proven 9 · Measurable 8 · Not saturated 8 · Demo 7 · Local evidence 9. AI: yes.

---

### #3 Šernų skaitliukas: real wildlife numbers from the cameras hunters already own

**One-line pitch:** Hunting clubs drop their trail-camera SD cards into an app. AI finds and identifies every animal (boar, roe deer, red deer, moose, wolf, fox, raccoon dog), and the EFSA-validated Random Encounter Model turns the photos into density per km². That replaces the snow-track census critics call "pointless" and gives ASF managers real boar numbers.

**Problem:**
- The annual census is mandatory, yet critics say it is inaccurate with unknown error ([Miške.lt](https://www.miske.lt/straipsniai/beprasmes-pildomos-zveriu-apskaitos/), [AM](https://am.lrv.lt/lt/naujienos/medziojamuju-gyvunu-apskaita-visus-metus)).
- ASF: 939 boar cases in Q1 2025 ([LRT](https://www.lrt.lt/naujienos/lietuvoje/2/2898201/lietuvoje-tarp-sernu-plinta-afrikinis-kiauliu-maras-virusas-nustatytas-22-savivaldybese)).
- Quotas and damage (see #2) depend on these numbers.

**Tech / collapse:** MegaDetector (Microsoft AI for Earth) crops the animals, a European species classifier (e.g. DeepFaune, France) identifies them, and the REM/CTDS density math runs on the result. A season produces thousands to tens of thousands of photos per club, and density needs statistics. Neither is doable by eye.

**Adoption loop:** Hunting club → places cameras by an app-generated random protocol → uploads → gets the census report + species trends → submits to the ministry. **Payer:** the Hunters' and Fishers' Association (LMŽD) or the ministry (a shared national tool), or VMVT for ASF zones. **Reach:** clubs already own cameras (sold widely in LT: [vga.lt](https://www.vga.lt/stebejimo-sistemos/medziokles-medziotoju-kameros)).

**Proven:** ENETWILD/EFSA ran harmonised camera-trap REM for boar in 19 European areas (densities 0.35–15.25/km²) ([EFSA 2022](https://www.efsa.europa.eu/en/supporting/pub/en-7214)), followed by the European Observatory of Wildlife ([EFSA 2024](https://efsa.onlinelibrary.wiley.com/doi/abs/10.2903/sp.efsa.2024.EN-9084)). MegaDetector and DeepFaune are well published **[links to add]**.

**Prior art:** Agouti (BE/NL), Wildlife Insights and Trapper do AI tagging. **Our difference:** a hunter-facing workflow that outputs the **LT statutory census form** plus ASF boar density maps, in Lithuanian.

**Pilot:** 8–10 cameras (borrowed from a hunting club) for 3–4 weeks in October → a real density estimate for roe deer and boar in one hunting area, compared with the club's last census. Metrics: density ± CI vs the census figure, and hours of photo sorting saved.

**Demo:** Drop an SD card of real October photos into the app → a count by species and a density map in a minute.

**Risks:**
1. REM assumptions (random placement, speed/day-range parameters): we use the ENETWILD protocol and published day-range values, and bait-site cameras count only as presence data.
2. "Hunters won't change habits": the output *replaces* a mandatory chore they dislike.
3. Prior art: we build on open models and only the LT legal output is new, which judges could see as integration rather than invention.

**Self-score:** Collapse 8 · Adoption 6 · Proven 9 · Measurable 7 · Not saturated 6 · Demo 8 · Local evidence 8. AI: yes.

---

### #4 BarštisScan: municipal vehicles map the hogweed as they drive

**One-line pitch:** A Galaxy phone on the dashboard of vehicles that already drive every road (road maintenance, waste collection, school buses) runs on-device AI that detects Sosnowsky's hogweed along the roadside and geotags it. Municipalities get a live, dated map of every colony and can check whether contractor-treated sites regrew.

**Problem:** Hogweed control is "inconsistent, keeps regrowing" (local-data.md, [LRT](https://www.lrt.lt/naujienos/lietuvoje/2/2303244/stoja-i-kova-su-sosnovskio-barsciais-naikinamas-nenuosekliai-vel-atsinaujina)). Money goes unused ("Millions for hogweed unreachable", [Valstietis](https://www.valstietis.lt/telsiu/milijonai-sosnovskio-barsciui-naikinti-nepasiekiami/108756)). Municipalities must report infested hectares ([15min](https://www.15min.lt/verslas/naujiena/agronaujienos/aplinkos-ministerija-savivaldybems-skyre-puse-milijono-euru-sosnovskio-barsciui-naikinti-313-1418326)). The programme now extends to private plots ([15min 2026](https://www.15min.lt/verslas/naujiena/nt-ir-interjeras/pavojingu-invaziniu-augalu-naikinimas-pleciamas-juos-salins-ir-privaciuose-sklypuose-971-2727826)).

**Tech / collapse:** YOLO on the phone NPU at 10–30 fps with GPS logging. Hundreds of km of roadside can't be re-surveyed by people every month, and a vehicle does it as a side-effect.

**Proven:** Hogweed deep-learning detection from UAVs reaches ROC AUC 0.96, running in real time on a Jetson ([IEEE 2021](https://ieeexplore.ieee.org/document/9359491/)), with >95% accuracy in flowering stage ([Springer 2022](https://link.springer.com/article/10.3103/S106836742201013X)). Vehicle/street-level invasive-plant detection **[unverified: several studies on knotweed/roadside weeds from street-view imagery exist; check]**.

**Adoption loop:** Municipal environment department → attaches phones to contracted vehicles → map → orders removal and verifies it. **Payer:** the municipality, from hogweed programme funds.

**Key risk:** season. By Oct–Nov only dead stalks and basal rosettes remain, so the pilot must train on summer iNaturalist photos and test on dead-umbel skeletons. Other risks: shaky roadside imagery, and competing with drone mapping. **Self-score:** C 8 · A 7 · P 7 · M 7 · S 7 · D 7 (seasonal) · L 8.

---

### #5 PelkėsPulsas: proof that restored peatlands are really wet

**One-line pitch:** Satellite radar (Sentinel-1) and optical data (Sentinel-2), calibrated by 3–5 DIY water-level loggers, give a monthly "wetness score" for every rewetted peatland in LT and convert it into tonnes of CO₂ avoided. That supports reporting under the Nature Restoration Law, whose national plan was due Sep 2026.

**Problem/evidence:** NRL peatland targets (30% by 2030) and the LT RRF measure (8,000 ha, €16M) ([EC](https://environment.ec.europa.eu/topics/nature-and-biodiversity/nature-restoration-regulation_en), [Succow](https://www.succow-stiftung.de/fileadmin/Ablage/Dokumente/DESIRE/RRF_measure_final.pdf)). Whether rewetting "worked" (water table near the surface) is today checked with sparse piezometers **[unverified for LT]**.

**Tech / collapse:** Google Earth Engine time series + an ML regression from Sentinel-1 backscatter to water table (the loggers give ground truth) + IPCC Wetlands Supplement emission factors. Nobody can walk thousands of ha monthly.

**Proven:** Sentinel-1 peatland moisture/water-table estimation is an active and successful research area **[unverified specifics; e.g. Finnish/German studies]**. MoorFutures (DE) carbon credits exist **[unverified]**.

**Adoption:** State Service for Protected Areas / Environment Ministry / Lithuanian Fund for Nature (restoration projects) as reporting users. Possible payer: companies buying peatland carbon credits.

**Pilot:** Analyse real historical satellite data for known LT rewetted bogs → before/after wetness change. No field season needed. **Risk:** low wow, pure dashboard, and researchers may already do this. **Self-score:** C 8 · A 6 · P 7 · M 8 · S 6 · D 7 · L 8.

---

## 4. Strongest pick: **BriedisStop**

Why it wins over the others:
- **Numbers a jury feels:** tripled collisions, >€5M damage, moose = two-thirds of the deaths.
- **One obvious deployer** that already spends on exactly this category (Via Lietuva: 90 km of fences this year, already using variable message signs). Units go only at hotspots, so the realistic count is dozens, not "every tree".
- **Proven concept** (RADS abroad + thermal-YOLO papers), with a new, cheap edge-AI twist and a dual monitoring use.
- **The best stage moment** of all five ideas (a warm "moose" walks in, the sign lights up), and IoT + AI both count toward the bonus.
- **Real pilot data is feasible in October** (dusk rut activity, legal because no sign goes on a public road).
- **The main weakness to prepare for:** mixed evidence on driver response. We'd frame the pilot around credibility (false-alarm rate) and propose the pairing with Via Lietuva's variable speed limits.

Close second: **ŽalosDronas**. It has the tightest policy hook (the law literally allows drones, and a municipality is asking), but a weaker sustainability story and a less dramatic demo.

---

## 5. Sources

- Via Lietuva / police stats: https://reidasofficial.lt/eismas/gyvunai-kelyje-pavasaris-lietuva-kaip-isvengti-susidurimo/ · https://77.lt/susidurimu-su-laukiniais-gyvunais-zala-virsijo-5-mln-euru · https://alkas.lt/2025/10/04/daugeja-susidurimu-su-gyvunais-i-ka-svarbiausia-atkreipti-demesi/ · https://reidasofficial.lt/eismas/susidurimai-su-laukiniais-gyvunais-lietuvoje-brangsta-viena-akimirka-gali-kainuoti-desimtis-tukstanciu-euru/
- LT collision research: https://pubmed.ncbi.nlm.nih.gov/38791668/ · https://www.sciencedirect.com/science/article/abs/pii/S0301479720310975 · https://doi.org/10.3390/f14061224 · https://pmc.ncbi.nlm.nih.gov/articles/PMC10603749/ · https://data.mendeley.com/datasets/4y8t78dsxy/2
- Via Lietuva fences: https://vialietuva.lt/naujienos/via-lietuva-plecia-apsaugos-sistemas-nuo-laukiniu-gyvunu-siemet-ju-bus-irengta-dar-apie-90-kilometru · https://alkas.lt/2026/07/17/keliuose-pleciamos-apsaugos-sistemos-nuo-laukiniu-gyvunu/ · https://www.15min.lt/verslas/naujiena/saugukelyje-lt/nematoma-kelio-vilnius-utena-puse-kaip-isvengti-briedziu-1662-2672500
- RADS / detection tech: https://www.sciencedirect.com/science/article/abs/pii/S0001457517303597 · https://pmc.ncbi.nlm.nih.gov/articles/PMC9003022/ · https://pmc.ncbi.nlm.nih.gov/articles/PMC12473846/ · https://transportecology.info/research/effectivness-addws-in-sweden · https://www.biodiversityinfrastructure.org/handbook/5-solutions/5-3-driver-warnings/
- ASF: https://www.lrt.lt/naujienos/lietuvoje/2/2898201/lietuvoje-tarp-sernu-plinta-afrikinis-kiauliu-maras-virusas-nustatytas-22-savivaldybese · https://jp.lt/panevezio-rajone-plinta-afrikinis-kiauliu-maras-skaiciai-didziausi-salyje/ · https://zur.lt/informuoja-vmvt/ · https://vmvt.lrv.lt/lt/veiklos-sritys/gyvunu-sveikata/gyvunu-ligos/uzkreciamosios-gyvunu-ligos/afrikinis-kiauliu-maras/
- Carcass drones: https://onlinelibrary.wiley.com/doi/10.1155/2023/5517000 · https://www.biodiversitymanifesto.com/2026/07/30/hunters-supporting-the-fight-against-african-swine-fever-with-new-drone-technology/ · https://www.cbc.ca/news/canada/edmonton/alberta-wild-boar-drones-9.7159112
- Game damage: https://am.lrv.lt/lt/naujienos/medziojamu-gyvunu-padaryta-zala-bus-nustatoma-tiksliau/ · https://zum.lrv.lt/lt/naujienos/ukininko-laukuose-isbandyta-kaip-veikia-atnaujinta-medziojamuju-gyvunu-padarytos-zalos-vertinimo-metodika/ · https://manoukis.lt/naujienos/aplinka-miskai/laukiniu-gyvunu-padarytai-zalai-nustatyti-siulo-naudoti-dronus · https://www.lrt.lt/naujienos/verslas/4/2950303/ministras-laukiniu-gyvunu-padaryta-zala-turi-kompensuoti-medziotojai-o-ne-zemdirbiai · https://rinkosaikste.lt/kedainiu-krasto-ukininkams-zveriu-padaryta-zala-perkope-100-tukst-euru/ · https://apvis.apva.lt/paskelbti_kvietimai/medziojamu-gyvunu-padarytos-zalos-kompensaciju-ismokejimas-2026-02 · https://www.researchgate.net/publication/342673886_Laukiniu_zveriu_padarytos_zalos_zemes_ukio_paseliams_vertinimas_skirtingais_metodais
- Drone damage research: https://wildlife.onlinelibrary.wiley.com/doi/abs/10.1002/wsb.916 · https://wildlife.onlinelibrary.wiley.com/doi/10.1002/wsb.1437 · https://doi.org/10.3390/agronomy15010238 · https://www.mdpi.com/2077-0472/13/8/1627 · https://www.sciencedaily.com/releases/2017/12/171212141841.htm
- Census / camera traps: https://am.lrv.lt/lt/naujienos/medziojamuju-gyvunu-apskaita-visus-metus · https://www.miske.lt/straipsniai/beprasmes-pildomos-zveriu-apskaitos/ · https://www.efsa.europa.eu/en/supporting/pub/en-7214 · https://efsa.onlinelibrary.wiley.com/doi/abs/10.2903/sp.efsa.2024.EN-9084
- Hogweed: https://ieeexplore.ieee.org/document/9359491/ · https://link.springer.com/article/10.3103/S106836742201013X · https://www.valstietis.lt/telsiu/milijonai-sosnovskio-barsciui-naikinti-nepasiekiami/108756 · https://www.15min.lt/verslas/naujiena/agronaujienos/aplinkos-ministerija-savivaldybems-skyre-puse-milijono-euru-sosnovskio-barsciui-naikinti-313-1418326 · https://www.15min.lt/verslas/naujiena/nt-ir-interjeras/pavojingu-invaziniu-augalu-naikinimas-pleciamas-juos-salins-ir-privaciuose-sklypuose-971-2727826
- Beavers: https://www.jonavoszinios.lt/naujiena/bebrai-gamtos-inzinieriai-kuriu-pavasarine-veikla-kelia-issukiu · https://ukininkopatarejas.lt/naujienos/melioracijos-griovius-uztvenkia-bebrai-ir-gamtosaugininkai/
- Fire detection: https://www.15min.lt/naujiena/aktualu/lietuva/miskininkai-diegia-vieninga-gaisru-stebejimo-sistema-aptiksiancia-ju-zidinius-56-2660384 · https://www.bernardinai.lt/lietuvoje-didelis-misko-gaisru-pavojus-valstybiniu-misku-uredijos-miskininkai-dorojasi-su-issukiu/
- NRL / peatlands: https://environment.ec.europa.eu/topics/nature-and-biodiversity/nature-restoration-regulation_en · https://www.succow-stiftung.de/fileadmin/Ablage/Dokumente/DESIRE/RRF_measure_final.pdf · https://greifswaldmoor.de/news/lithuania-eu-frontrunner-in-peatland-recovery.html
- TBE: https://www.sciencedirect.com/science/article/pii/S2772707625001626 · https://www.lrt.lt/en/news-in-english/19/1085913/lithuania-reports-highest-tick-borne-encephalitis-spread-in-europe

### Verification to-do (before any slide)
1. The Huijser et al. collision-reduction range for animal detection systems (33–97%) and the Swedish ADDWS results.
2. Fence-end hotspot literature.
3. Whether Via Lietuva already runs any animal-*detection* (not just static/VMS) system, e.g. on the Vilnius–Utena reconstruction. The article [15min: Vilnius–Utena](https://www.15min.lt/verslas/naujiena/saugukelyje-lt/nematoma-kelio-vilnius-utena-puse-kaip-isvengti-briedziu-1662-2672500) mentions "modern solutions". **If they already have detection there, BriedisStop's novelty drops and it becomes "cheap AI version + monitoring".**
4. National annual game-damage compensation total.
5. Drone rules for students (LT TKA).
6. Thermal sensor prices and detection range.
