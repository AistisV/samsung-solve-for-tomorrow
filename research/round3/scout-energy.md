# Scout report: Energy, buildings, heating and the grid (Lithuania)

> Round 3 scout, domain: energy/buildings/heating/grid. Research done with WebSearch (EN + LT). The shared search budget ran out partway through, so a few supporting facts are marked **[unverified]** and need checking before the Oct 16 form.

## TL;DR

- **Strongest pick: "HeatTwin", a Leanheat-style AI for unrenovated Soviet-era blocks.** A handful of cheap indoor temperature sensors in volunteer flats plus a model of the building tell the building's maintainer (*pastato šildymo sistemos prižiūrėtojas*) what heating curve to set on the automated substation, and which risers are over- or under-heated. It is proven at scale in Finland and Germany (Danfoss Leanheat: 100k+ apartments, 6–20% savings). It has a legal hook: every block had to have an automated substation by **1 July 2026**, and maintainers are legally obliged to keep operation economical. The obvious payer is the maintainer or heat utility. The team can collect real pilot data in their own buildings, because the heating season starts in October.
- Runners-up: **ChimneyWatch** (camera-AI smoke-opacity ranking of chimneys, where residential burning is 70–80% of LT PM2.5 emissions), **LeakPatrol** (a thermal camera on a municipal vehicle plus AI finds district-heating pipe leaks; Vilnius has a 758 km network whose average age is over 30 years), and **GridPulse** (frequency-responsive water heaters for the post-desync Baltic grid; policy facts partly unverified).

---

## 1. Key local evidence collected

| Fact | Source |
|---|---|
| About **38,000** apartment buildings in LT house more than half the population; most were built before 1993 and are energy-inefficient. | [NIB](https://www.nib.int/articles/lower-heating-bills-to-tackle-climate-change-in-lithuania) |
| Target: **9,882** buildings renovated by 2030 (ILTE needs about €2.4bn). | [ILTE / Sustainable Fitch SPO](https://ilte.lt/en/doclib/ynzl8ikmdouhh8ya6guxv7bsatm944yz) |
| Actual pace: **359** blocks renovated in 2025 (614k m², about 13k flats). Renovated blocks pay about **half** as much for heat as unrenovated ones. | [APVA](https://apva.lrv.lt/lt/naujienos-24316/daugiabuciu-renovacija-2025-m-35-modernizuoti-namai-isirenge-atsinaujinancius-energijos-saltinius-h3T/) |
| Klaipėda district: more than 600 blocks waiting, only 37 renovated (5.7%). | [Gargždai](https://gargzdai.lt/klaipedos-rajone-renovacijos-laukia-per-600-daugiabuciu-renovuoti-vos-37) |
| So even at the fastest pace, **tens of thousands of blocks will stay unrenovated through the 2030s**, and they need cheap, non-construction savings. | derived from the rows above |
| Elevator-type (non-automated) substations had to be replaced with automated ones by **1 July 2026**. At the end of 2022 there were 3,446 left, 1,916 of them in apartment blocks. An automated substation plus a modernised internal system saves **15–25%**. | [Gimtasis Rokiškis](https://grokiskis.lt/aktualijos/iki-termino-liko-savaite-ne-visi-daugiabuciai-spejo-modernizuoti-silumos-punktus), [LŠTA](https://lsta.lt/aktualijos/daugiabucio-sildymo-sistemos-renovacija/), [Panevėžio energija](https://www.pe.lt/silumos-punkto-modernizacija) |
| Unbalanced heating in old blocks means **"some residents open windows in winter while others plug in electric heaters."** Causes: flats swapping in bigger radiators, and flats near the substation getting more flow. The fix is hydraulic balancing. | [15min](https://www.15min.lt/verslas/naujiena/nt-ir-interjeras/nekilnojamasis-turtas/sildymo-sistemos-pertvarka-daugiabutyje-mazesnes-saskaitos-ir-didesnis-komfortas-973-1507076), [Vilnius municipality](https://vilnius.lt/lt/savivaldybe/aplinkosauga-ir-energetika/siluma/silumos-punkto-ir-sildymo-sistemos-modernizavimas-balansavimas-2/) |
| The law requires the **maintainer** to keep heating and hot-water equipment running in an economical, rational mode and to give owners **annual energy-saving recommendations**. | [Vilnius municipality: mistakes residents make](https://vilnius.lt/lt/2022/01/27/klaidos-kurias-daro-gyventojai-noredami-taupyti-siluma/) (search summary) |
| Many old blocks split heat **by floor area**. Allocators cost €1.27/month, meters €6.47/month. Allocator tampering is a known complaint. | [LRT](https://www.lrt.lt/naujienos/verslas/4/2394997/naujai-statomu-vilniaus-daugiabuciu-gyventojams-ruosiamas-6-5-euro-menesinis-mokestis), [kresiti.lt](https://www.kresiti.lt/naujienos/silumos-dalikliai-ir-apskaita-uz-suvartota-siluma-sildymui/) |
| Heating payments are **up to 80%** of household energy spending. | [Klaipėdos energija](https://www.klenergija.lt/energijos-taupymas/) (search summary) |
| Average residential heat use in 2022 was **135 kWh/m²**. Some utilities publish per-building consumption and cost (e.g. Šiauliai "Namo šildymo informacija"). | [LŠTA](https://lsta.lt/silumos-ukis/silumos-suvartojimas/), [mano.senergija.lt](https://mano.senergija.lt/NamoInfo/) |
| Heating compensation: about **190k recipients** and about **€100M** expected for the 2025–26 season. The system caps heating spending at 10% of income. The Social Climate Plan counts about **300k households** as vulnerable or in energy poverty. | [MadeinVilnius](https://madeinvilnius.lt/en/news/Lithuanian-news/Applications-for-heating-compensation-can-now-be-submitted---what-is-important-for-residents-to-know/), [EC Social Climate Plan](https://employment-social-affairs.ec.europa.eu/policies-and-activities/funding/social-climate-fund/social-climate-fund-national-plans/lithuanias-social-climate-plan_en) |
| District-heating network losses are commonly **10–18%**; individual systems reach 17.9% (Joniškis), 24.7% (Gataučiai) and about 15.4% (Tauragė). | [LŠTA sector review](https://lsta.lt/silumos-ukis/cst-sektoriaus-apzvalga/), [GREN Joniškis plan](https://grenweb01.blob.core.windows.net/gren-web-prod/sites/3/2025/04/GREN-JONISKIS-DESIMTIES-METU-SILUMOS-UKIO-PLETROS-INVESTICIJU-PLANAS.pdf), [Tauragė](https://www.tauragesst.lt/uploads/pdf/2025%20veiklos%20ataskaita/2024-12-18-Tarybos%20sprendimas-Nr.%201-368.pdf) |
| The Vilnius network is **758 km**, with an average age of more than 30 years and some segments older than 50. Pipes rebuilt in 2025 averaged about 59 years old. Worn yard pipes melt the snow above them, and residents fear they will pay for the losses. | [chc.lt](https://chc.lt/rekonstrukcijos/), [LRT](https://www.lrt.lt/naujienos/verslas/4/1847989/del-nusidevejusiu-silumos-trasu-kiemuose-tirpsta-sniegas-vilnieciai-baiminasi-jog-nuostolius-padengti-tures-patys) |
| Residential combustion is **70–80% of PM2.5 emissions in LT** (with HR and LV, the highest shares in the EU). | [EGUsphere preprint 2023](https://egusphere.copernicus.org/preprints/2023/egusphere-2023-1194/egusphere-2023-1194.pdf) (the source cites EEB) |
| In the cold season, **all LT air-quality stations** record PM daily-limit exceedances. Burning waste in stoves is banned, and fines can reach thousands of euros. | [kaipkada.lt](https://www.kaipkada.lt/lietuva/ekspertai-perspeja-gyventojus-lietuvoje-namu-sildymas-draudziamomis-atliekomis-gali-kainuoti-iki-keliu-tukstanciu-181023/), [Biržai](https://www.birzai.lt/ekologija/atlieku-tvarkymas/atlieku-deginimas/406?lang=lt) |
| The state funds replacement of polluting boilers with heat pumps or class-5 biomass boilers, with rolling calls in 2025–26. | [Energy Ministry](https://enmin.lrv.lt/lt/zaliau/suzinok/parama-tarsiu-katilu-keitimui-i-efektyvesne-sildymo-iranga-tesiama-ir-bus-finansuojama-seserius-metus/), [APVIS](https://apvis.apva.lt/paskelbti_kvietimai/iskastinio-kuro-ir-nusidevejusiu-biokura-naudojanciu-katilu-keitimas-naujais-biokura-ar-kitais-atsinaujinancius-energijos-isteklius-naudojanciais-silumos-gamybos-irenginiais-2026-04) |
| Baltic grid desynchronised from BRELL in Feb 2025. In Oct 2025 Nord Pool LT prices spiked to about **€1/kWh** at peaks. Negative-price hours in June 2025 were up 294% on June 2024. | [cleantechlithuania](https://www.cleantechlithuania.lt/en/naujienos/inion---elektros-kainu-suoliai-lietuvoje), [Ignitis market overview](https://ignitis.lv/en/business/articles/electricity-market-overview-june-2025) |
| Home battery subsidy: €15M from the Energy Ministry via APVA. Prosumers can choose 1-, 2- or 4-zone tariffs, and there is a storage fee. | [APVA](https://apva.lrv.lt/lt/naujienos-24316/parama-gyventojams-isirengusiems-elektros-kaupiklius-jau-balandzio-8-d/), [Litsol](https://litsol.lt/elektros-tarifai-ir-pasaugojimo-mokestis-gaminantiems-vartotojams-ka-svarbu-zinoti-2026-metais/) |
| Classroom CO₂ reaches 3,000–4,000 ppm in LT lessons, and 5,152 ppm was measured in a Vilnius school. It is worse in renovated, airtight schools. | [sildymas-vedinimas.lt](https://sildymas-vedinimas.lt/naujienos/vilniaus-mokyklose-oro-kokybe-neatitinka-normu/), [VU thesis](https://epublications.vu.lt/object/elaba:16131213/16131213.pdf) |

---

## 2. Brainstorm: 24 ideas, filtered

Hard criteria: C = collapse test · A = adoption loop · P = proven blocks · M = measurable · S = not saturated · D = demo in 6 weeks · L = local evidence.

| # | Idea | Verdict | One-line reason |
|---|---|---|---|
| 1 | **HeatTwin**: indoor sensors in a sample of flats plus an ML building model tune the block's substation heating curve and flag riser imbalance (Leanheat for Soviet blocks) | **KEEP (#1)** | Passes all 7. Proven (Leanheat, 100k+ apartments). Legal payer (the maintainer). New substations since 1 Jul 2026 make it controllable. Real pilot data possible in October. |
| 2 | **ChimneyWatch**: rooftop camera plus AI measures chimney smoke opacity and duration across a private-house district and ranks the top polluters, so the municipality can target advice and boiler subsidies | **KEEP (#2)** | Proven blocks (ASTM D7520 camera-opacity method, EPA ALT-082; Kraków/Katowice smoke policing). Strong LT stat (70–80% of PM2.5). One camera covers a neighbourhood. The risks are privacy and night-time smoke. |
| 3 | **LeakPatrol**: thermal camera on a municipal or utility vehicle, AI finds district-heating leak hotspots and matches them to pipe routes | **KEEP (#3)** | Aerial DH leak AI is proven (98.6% of true leaks detected). Utility is the payer. The vehicle-mounted version itself is unproven, and snow-melt is sometimes visible by eye. |
| 4 | **GridPulse**: ESP32 frequency sensing in electric water heaters and heat pumps, which shed load in under a second when Baltic grid frequency drops (a dynamic-demand reserve for the isolated Baltic grid) | **KEEP (#4, with caveats)** | Proven in the UK and Sweden. Timely after desync. A household aggregator route in LT is **[unverified]**, and residential electric water heating share is unknown. |
| 5 | **School heating autopilot**: timetable (Tamo/Eduka) plus smart TRVs plus CO₂ sensors run room-by-room heating and ventilation | Keep as backup | Pilot is easy in their own school. Collapse is only moderate (a caretaker can set schedules), classroom CO₂ monitors are a common student project, and TRVs don't work in single-pipe schools. |
| 6 | Home battery and heat-pump optimiser for Nord Pool 15-min prices | Kill | Saturated (Tibber, Ngenic, Home Assistant, supplier apps). |
| 7 | Renovation-vote persuader: thermal photos of your block and € per flat to win the renovation vote | Kill | Collapse is weak (any auditor takes thermal photos), and we couldn't verify that the vote is the bottleneck. |
| 8 | Aerial or satellite thermal map of all city roofs to prioritise renovation | Kill | Needs an aircraft, which students can't do, and the building registry already gives age and series. |
| 9 | Street-view AI predicts building energy class | Kill | A spreadsheet of registry data (year, series) gets most of the way there. |
| 10 | Utility-side substation fault detection from heat-meter return temperatures | Kill (merged into #1) | Proven (Swedish work), but students have no data access. |
| 11 | Energy-poverty detection from meter data (underheated elderly) | Kill | Privacy and data access, and the 10%-of-income compensation already exists. |
| 12 | AI that reads heat or water meter photos | Kill | A wrapper. |
| 13 | Solar-panel fault detection for prosumers | Kill | Inverter apps already do this. |
| 14 | Smart EV-charging scheduler | Kill | Saturated. |
| 15 | Dry-firewood certification app (moisture meter plus QR code) | Kill | Fails the collapse test: a €15 moisture meter does the job, and it copies the UK "Ready to Burn" scheme. |
| 16 | Allocator-tampering detector | Kill | Niche and adversarial toward residents. |
| 17 | Hot-water circulation ("gyvatukas") loss optimiser | Kill | Niche, and little public evidence. |
| 18 | Stairwell door or window-open sensors | Kill | Trivial, and fails the collapse test. |
| 19 | Private-house heat-loss rating from smart-meter data (UK SMETER-like) | Kill | LT houses mostly heat with wood or gas, not electricity, and smart gas meters are rare. |
| 20 | Data-centre waste heat into district heating matchmaking | Kill | Not doable by students, and the market is tiny. |
| 21 | Remote solar-park share marketplace | Kill | Already a commercial product (ESO / remote parks), and no AI role. |
| 22 | Heat-pump fault detection by sound | Kill | Niche, and weak LT evidence. |
| 23 | Community battery sizing for renovated blocks | Kill | A spreadsheet task. |
| 24 | EPBD "renovation passport" generator for blocks | Kill | Paperwork, and an LLM wrapper. |

---

## 3. Detailed profiles

### #1 HeatTwin: "Leanheat for the Soviet block" (STRONGEST PICK)

**One-line pitch:** €100 of sensors in 8 flats lets AI heat a whole Soviet-era block to 21°C instead of 25°C with the windows open. It is the proven Finnish method, adapted to the roughly 28,000 Lithuanian blocks that won't be renovated this decade.

**Problem (LT evidence):**
- About 38k blocks exist, and only 359 were renovated in 2025 against a 9,882-by-2030 target ([APVA](https://apva.lrv.lt/lt/naujienos-24316/daugiabuciu-renovacija-2025-m-35-modernizuoti-namai-isirenge-atsinaujinancius-energijos-saltinius-h3T/), [ILTE](https://ilte.lt/en/doclib/ynzl8ikmdouhh8ya6guxv7bsatm944yz)). Most unrenovated blocks will stay that way for years.
- In unbalanced old systems some flats overheat and open windows while others use electric heaters ([15min](https://www.15min.lt/verslas/naujiena/nt-ir-interjeras/nekilnojamasis-turtas/sildymo-sistemos-pertvarka-daugiabutyje-mazesnes-saskaitos-ir-didesnis-komfortas-973-1507076)).
- Many blocks pay by m², so nobody has a personal incentive to turn heat down.
- Since 1 Jul 2026 all blocks must have automated substations ([Rokiškis](https://grokiskis.lt/aktualijos/iki-termino-liko-savaite-ne-visi-daugiabuciai-spejo-modernizuoti-silumos-punktus)). Those substations run a **weather-compensation curve set by a maintainer who never sees the indoor temperature**. The maintainer is legally obliged to ensure economical operation ([Vilnius](https://vilnius.lt/lt/2022/01/27/klaidos-kurias-daro-gyventojai-noredami-taupyti-siluma/)).
- The state spends about €100M per season on heating compensation ([MadeinVilnius](https://madeinvilnius.lt/en/news/Lithuanian-news/Applications-for-heating-compensation-can-now-be-submitted---what-is-important-for-residents-to-know/)), so every kWh saved in low-income blocks is also saved public money.

**What the tech does:**
1. Wireless temperature and humidity sensors (ESP32 or BLE, about €10–15 each) go into 6–10 volunteer flats spread across risers and floors (top/bottom, near/far). They could also be old Galaxy phones reused as sensor hubs.
2. The substation's supply and return temperatures and heat-meter data come in through the controller or utility portal, or through a clamp-on sensor in the pilot. Weather forecast data comes from the LHMT API.
3. An ML model (grey-box RC building model plus gradient boosting) learns the building's thermal response in about 2 weeks. That is the Leanheat method.
4. **Outputs:**
   - (a) An optimal heating curve and pre-heating schedule for tomorrow's forecast, sent to the maintainer, or written directly to controllers that support it.
   - (b) A **riser imbalance map** showing which risers are over- or under-heated, with suggested balancing-valve settings.
   - (c) kWh and € saved, tracked against a weather-normalised baseline.

**Why it collapses without the tech:** the maintainer has no indoor data at all, and even with data a person can't solve a building's thermal dynamics against a 48-hour weather forecast every hour. Without sensors and a model, the only choices are "set it hot so nobody complains" (today's situation) or guessing.

**Adoption loop (one breath):**
- **User:** building maintainers (heat utilities' service arms or private maintainers) and chairs of homeowner associations.
- **Why:** they're legally obliged to run the system economically, complaints from cold flats cost them call-outs, and the utility's peak load drops.
- **Who pays:** a service fee of about €1–2 per flat per month from the building maintenance budget. A savings-share model or municipal energy-poverty budgets are alternatives.
- **How it reaches them:** through the maintainer, who already visits every substation each season. Volunteer flats are recruited through the homeowner association.
- **First partner:** the team's local heat utility or maintainer, e.g. Šiaulių energija, which already publishes per-building heating data, or the municipality's energy department.

**Where the core tech is proven:**
- Danfoss Leanheat Building: "100,000 apartments". Espoon Asunnot fitted all 15,000 flats and saw −6% energy and −17% peak over 3 years. Asuntosäätiö saw −10% energy costs. A 2018 pilot saved up to 10% ([Danfoss](https://www.danfoss.com/en/about-danfoss/news/cf/artificial-intelligence-provides-comfort-for-apartments-residents/), [Espoo / Avain case](https://www.danfoss.com/en/service-and-support/case-stories/dcs/danfoss-leanheat-building-helps-avain-deliver-energy-efficient-heating-to-residents-throughout-finland/), [enercity 50k units](https://www.danfoss.com/en/service-and-support/case-stories/dhs/roll-out-in-50-000-housing-units-enercity-ag-optimizes-district-heating-supply-with-leanheat-building/)).
- Data-driven supply-temperature optimisation ([ScienceDirect 2023](https://www.sciencedirect.com/science/article/pii/S036054422302577X)).
- Hydraulic balancing saves "15% and more" ([review](https://www.sciencedirect.com/science/article/abs/pii/S2352710219310617)).

**Prior art and how we differ:**
- Leanheat is sold to large Nordic and German landlords that own thousands of flats and have sensors in every flat.
- **We found no LT deployment [unverified; one search].** A related LT example is AI-controlled boiler houses in Pakruojis ([LRT](https://www.lrt.lt/naujienos/mokslas-ir-it/11/2411020/pakruojo-gyventoju-namus-nuo-siol-sildo-dirbtinio-intelekto-valdomos-katilines)), but that is on the production side, not the building side.
- Our differences:
  - (1) **Sparse sampling**: 6–10 volunteer flats rather than every flat, because LT blocks are fragmented and privately owned.
  - (2) **Riser-imbalance diagnosis** for Soviet single-pipe systems.
  - (3) Built around the new mandatory substations and LT maintainers' legal duty.
  - (4) An energy-poverty lens: target blocks with many compensation recipients.

**Measurable impact:**
- Primary: **indoor overheating (degree-hours above 21°C)**, then **kWh/m² per month against a weather-normalised baseline**, then € and t CO₂. Per-building consumption data is public from some utilities, e.g. [mano.senergija.lt](https://mano.senergija.lt/NamoInfo/).
- Rule-of-thumb savings of about 5–6% per 1°C lower indoor temperature are commonly cited **[unverified; cite a proper source before use]**.

**Pilot plan (by Nov 6):**
- Early October: install 6–10 sensors in team members' and neighbours' flats in 2–3 blocks. The heating season starts about then.
- Log 3–4 weeks of data and pull the building's monthly consumption from the utility portal.
- Output: an overheating map, an imbalance map, and the curve the model recommends, with an estimated kWh saving.
- Stretch goal: ask the maintainer to apply the recommended curve in one block for 1–2 weeks and compare against the baseline, holding weather constant.

**Demo:**
- A live dashboard: a 3D block with each flat coloured by temperature (a heatmap) and tomorrow's forecast curve against the "blind" curve.
- On stage, a tabletop mini-block with 2 "risers": resistor-heated aluminium "radiators", an ESP32 "substation" and sensors. The judge turns a "weather" knob, and the AI pre-adjusts before the room overshoots.
- Wow moment: "this is the actual data from Flat 12 in our building, 25.4°C with the window open, last Tuesday."

**Top 3 judge objections:**
1. *"Danfoss already sells this."* True, and we cite it. That is why it's proven. It isn't deployed for fragmented LT homeowner-association blocks **[unverified]**. Our sparse-sensor, imbalance-diagnosis version is designed around LT law and substations, and it is open and cheap.
2. *"Why would residents let you put sensors in?"* A €10 sensor with no camera or microphone, which only reads temperature. Residents who are too cold are the most motivated volunteers, and the homeowner association decides for the building.
3. *"Can a maintainer even change the curve remotely?"* Most new automated controllers accept a curve setting. In the pilot the output is a weekly recommendation the maintainer types in. Remote control is phase 2.

**Self-score (1–10):** C 9 · A 8 · P 10 · M 9 · S 8 · D 8 · L 9. **AI/IoT bonus: yes.**

---

### #2 ChimneyWatch: camera AI that finds the smokiest chimneys

**One-line pitch:** one camera on a school roof watches 300 chimneys and measures smoke opacity with an EPA-approved camera method. The municipality then sends advice and subsidy offers to the 10 worst houses instead of fining everyone or no one.

**Problem:**
- Residential combustion causes 70–80% of LT's PM2.5 emissions ([EGUsphere](https://egusphere.copernicus.org/preprints/2023/egusphere-2023-1194/egusphere-2023-1194.pdf)).
- Every monitoring station records cold-season exceedances. Burning waste is illegal but enforced only on complaint ([kaipkada](https://www.kaipkada.lt/lietuva/ekspertai-perspeja-gyventojus-lietuvoje-namu-sildymas-draudziamomis-atliekomis-gali-kainuoti-iki-keliu-tukstanciu-181023/)).
- Boiler-replacement subsidies exist, but nobody targets them at the worst emitters ([Energy Ministry](https://enmin.lrv.lt/lt/zaliau/suzinok/parama-tarsiu-katilu-keitimui-i-efektyvesne-sildymo-iranga-tesiama-ir-bus-finansuojama-seserius-metus/)).

**Tech:**
- A fixed camera (RGB by day, plus an optional low-cost thermal sensor to detect plumes at dusk) on a tall building.
- Chimneys are registered on a map. An AI segments each plume and estimates opacity and duration (DCOT/ASTM D7520 logic).
- A low-cost PM2.5 sensor mesh confirms the neighbourhood impact.
- Output: a weekly "top emitters" list and a neighbourhood PM map.

**Collapse:** nobody can watch hundreds of chimneys 24/7 and quantify opacity consistently. Human "smoke readers" (EPA Method 9) are exactly what the camera method replaced.

**Adoption:**
- **User:** the municipal environment department or AAD inspectors.
- **Why:** complaint-driven enforcement is blind, and they must meet AQ limits.
- **Who pays:** the municipality's environment programme budget (*SAPP*) **[unverified name]**.
- **How:** one camera per problem district. The first action is a friendly letter with a wood-moisture tip and a link to the boiler subsidy. Inspection comes only for repeat heavy emitters.

**Proven:**
- ASTM D7520 camera opacity, approved by EPA as ALT-082 ([ASTM](https://www.astm.org/d7520-13.html), [CT DEEP](https://portal.ct.gov/-/media/DEEP/air/ALTMethod082pdf.pdf)).
- Kraków and Katowice drone smoke policing with fines ([TheMayor](https://www.themayor.eu/en/a/view/drones-monitor-compliance-with-ban-on-burning-coal-and-wood-in-krakow-3685), [PlanetSave](https://planetsave.com/2018/02/05/katowice-poland-using-drones-locate-illegal-emissions-sources/)).

**Prior art gap:** the drones need a crew per flight. Continuous, fixed-camera ranking of residential chimneys is not something we found in LT.

**Metric and pilot:** plume-minutes per chimney per evening and neighbourhood PM2.5. Pilot: film a private-house district from a high point for 3 October evenings, label the plumes, and produce the ranking.

**Demo:** live smoke-machine plume with an opacity readout, and a timelapse of a real LT neighbourhood.

**Risks:**
- (1) Privacy and "snitch camera". Answer: plumes are publicly visible emissions, the output is advice before fines, and data is kept per chimney, not per face.
- (2) Night burning. Answer: add thermal plume detection plus the PM mesh, and **verify feasibility early**.
- (3) Opacity isn't the same as toxicity (waste burning). Answer: pair with the PM mesh, and flag likely waste-burning by colour and odour complaints.

**Self-score:** C 8 · A 6 · P 7 · M 8 · S 9 · D 8 · L 9.

---

### #3 LeakPatrol: district-heating leak finder on a municipal vehicle

**One-line pitch:** a €300 thermal camera on a vehicle that already drives every street, plus AI trained on public drone leak datasets, finds hot spots over the 758 km Vilnius heating network every week instead of every few years.

**Problem:**
- The Vilnius network is 758 km, with an average age over 30 years and replaced pipes averaging about 59 years ([chc.lt](https://chc.lt/rekonstrukcijos/)).
- Network losses are 10–25% by system ([LŠTA](https://lsta.lt/silumos-ukis/cst-sektoriaus-apzvalga/), [GREN Joniškis](https://grenweb01.blob.core.windows.net/gren-web-prod/sites/3/2025/04/GREN-JONISKIS-DESIMTIES-METU-SILUMOS-UKIO-PLETROS-INVESTICIJU-PLANAS.pdf)).
- Worn yard pipes melt the snow, and residents fear paying for the losses ([LRT](https://www.lrt.lt/naujienos/verslas/4/1847989/del-nusidevejusiu-silumos-trasu-kiemuose-tirpsta-sniegas-vilnieciai-baiminasi-jog-nuostolius-padengti-tures-patys)).

**Tech:** a vehicle-mounted radiometric thermal camera, GPS and IMU, with the images matched to the pipe-route GIS. A segmentation model (TASeg-style) flags anomalies, and repeated passes separate persistent leaks from sun-heated or parked-car artefacts.

**Collapse:** passes. No person can survey 758 km weekly and tell a leak from a manhole or a warm car. Snow-melt is visible by eye only when there's snow.

**Adoption:** the heat utility's network department pays, because losses above the regulated norm are its own cost. The camera rides on a utility van or a municipal garbage truck, the MIT City Scanner model ([MIT](https://senseable.mit.edu/cityscanner/)).

**Proven:**
- UAV DH leak CNN: 243k images, 98.6% of true leaks detected ([Pattern Recognition Letters](https://www.sciencedirect.com/science/article/abs/pii/S0167865520302038)).
- TASeg open models and dataset ([GitHub](https://github.com/emvollmer/TASeg)).
- Drive-by thermography at city scale (Essess, [MIT News](https://news.mit.edu/2015/startup-essess-heat-mapping-cars-0105)).

**Weakness:** oblique street-level leak detection is **not itself proven**, and LT drone thermography contractors already exist ([Aerodetect](https://aerodetect.lt/)).

**Metric and pilot:** hotspots found and confirmed by the utility, with estimated MWh per year per leak. Pilot: drive DH routes in the team's town in October.

**Risks:** the unproven vehicle angle, access to GIS pipe routes, and "the utility already flies drones".

**Self-score:** C 7 · A 8 · P 6 · M 8 · S 7 · D 8 · L 8.

---

### #4 GridPulse: water heaters that steady the Baltic grid

**One-line pitch:** after desynchronisation the Baltics must hold their own frequency. A €15 add-on makes home electric water heaters switch off within a second when frequency dips, like UK "dynamic demand" and Swedish FFR from heat pumps.

**Evidence:**
- Desync happened in Feb 2025, and price spikes reached about €1/kWh in Oct 2025 ([cleantechlithuania](https://www.cleantechlithuania.lt/en/naujienos/inion---elektros-kainu-suoliai-lietuvoje)).
- Balancing and reserve costs rising after desync and being passed to consumers is **[unverified; searches ran out]**.
- Whether LT allows household aggregation into Litgrid reserves is **[unverified]**.

**Tech:** ESP32 zero-crossing frequency measurement plus relay logic, fleet aggregation, and ML deciding which heaters can safely drop load given their tank temperature.

**Collapse:** passes, because no person can react in under a second.

**Adoption:** an aggregator or electricity supplier pays households for the reserve. Weak until the regulatory route is confirmed.

**Demo:** great. A live grid-frequency "heartbeat" and a simulated trip event.

**Self-score:** C 10 · A 4 · P 8 · M 7 · S 8 · D 9 · L 5 (pending verification).

---

### Backup: School heating autopilot

This connects Tamo/Eduka timetables with smart TRVs and CO₂ sensors in classrooms. It is easy to pilot in the team's own school, and the school owner (the municipality) pays the bill. It scores lower on collapse (a caretaker can set schedules) and on saturation (classroom CO₂ monitors), and TRVs don't work on single-pipe systems. Self-score: C 5 · A 7 · P 8 · M 8 · S 5 · D 9 · L 7.

---

## 4. Recommendation

**Go with HeatTwin (#1).**
- It is the only idea here that scores at least 8 on every hard criterion.
- The core tech has hard, large-scale results: 100k+ apartments and −6% energy / −17% peak across 15,000 Espoo flats.
- The Lithuanian angle is specific and timely: tens of thousands of unrenovated blocks, a renovation pace far behind target, the 1 July 2026 substation deadline, maintainers' legal duty and €100M a year in heating compensation.
- The adoption loop fits in one breath: maintainer, building, fee.
- It is IoT plus AI, and the team can show **real data from their own buildings** on Nov 6, because the pilot window matches the start of the heating season.

**Things to verify before the Oct 16 form:**
1. That Leanheat or an equivalent isn't already deployed in LT (email Danfoss LT or LŠTA).
2. A solid source for the % saving per °C.
3. Which automated substation controllers are common in LT and whether they accept remote curve changes.
4. A letter of intent from one utility or maintainer.

## 5. Sources (all consulted via search)

- APVA 2025 renovation results: https://apva.lrv.lt/lt/naujienos-24316/daugiabuciu-renovacija-2025-m-35-modernizuoti-namai-isirenge-atsinaujinancius-energijos-saltinius-h3T/
- APVA call extended to Apr 2026: https://modernizuok.apva.lt/apie-naujienos/pratestas-daugiabuciu-namu-modernizavimo-kvietimas-paraiskas-galima-teikti-iki-2026-m.-balandzio-1-d.:161
- NIB, 38k apartment buildings: https://www.nib.int/articles/lower-heating-bills-to-tackle-climate-change-in-lithuania
- ILTE SPO, 9,882 target: https://ilte.lt/en/doclib/ynzl8ikmdouhh8ya6guxv7bsatm944yz
- Klaipėda district renovation: https://gargzdai.lt/klaipedos-rajone-renovacijos-laukia-per-600-daugiabuciu-renovuoti-vos-37
- Substation deadline: https://grokiskis.lt/aktualijos/iki-termino-liko-savaite-ne-visi-daugiabuciai-spejo-modernizuoti-silumos-punktus ; https://lsta.lt/aktualijos/daugiabucio-sildymo-sistemos-renovacija/ ; https://www.pe.lt/silumos-punkto-modernizacija
- Imbalance and open windows: https://www.15min.lt/verslas/naujiena/nt-ir-interjeras/nekilnojamasis-turtas/sildymo-sistemos-pertvarka-daugiabutyje-mazesnes-saskaitos-ir-didesnis-komfortas-973-1507076 ; https://vilnius.lt/lt/2022/01/27/klaidos-kurias-daro-gyventojai-noredami-taupyti-siluma/ ; https://vilnius.lt/lt/savivaldybe/aplinkosauga-ir-energetika/siluma/silumos-punkto-ir-sildymo-sistemos-modernizavimas-balansavimas-2/
- Allocators and meters: https://www.lrt.lt/naujienos/verslas/4/2394997/naujai-statomu-vilniaus-daugiabuciu-gyventojams-ruosiamas-6-5-euro-menesinis-mokestis ; https://www.kresiti.lt/naujienos/silumos-dalikliai-ir-apskaita-uz-suvartota-siluma-sildymui/
- Heat consumption data: https://lsta.lt/silumos-ukis/silumos-suvartojimas/ ; https://mano.senergija.lt/NamoInfo/
- Heating compensation: https://madeinvilnius.lt/en/news/Lithuanian-news/Applications-for-heating-compensation-can-now-be-submitted---what-is-important-for-residents-to-know/ ; https://employment-social-affairs.ec.europa.eu/policies-and-activities/funding/social-climate-fund/social-climate-fund-national-plans/lithuanias-social-climate-plan_en ; https://www.lrt.lt/en/news-in-english/19/3055083/lithuanian-households-brace-for-painful-heating-season-as-energy-costs-soar
- DH losses: https://lsta.lt/silumos-ukis/cst-sektoriaus-apzvalga/ ; https://grenweb01.blob.core.windows.net/gren-web-prod/sites/3/2025/04/GREN-JONISKIS-DESIMTIES-METU-SILUMOS-UKIO-PLETROS-INVESTICIJU-PLANAS.pdf ; https://www.tauragesst.lt/uploads/pdf/2025%20veiklos%20ataskaita/2024-12-18-Tarybos%20sprendimas-Nr.%201-368.pdf
- Vilnius network: https://chc.lt/rekonstrukcijos/ ; https://www.lrt.lt/naujienos/verslas/4/1847989/del-nusidevejusiu-silumos-trasu-kiemuose-tirpsta-sniegas-vilnieciai-baiminasi-jog-nuostolius-padengti-tures-patys
- Leanheat: https://www.danfoss.com/en/about-danfoss/news/cf/artificial-intelligence-provides-comfort-for-apartments-residents/ ; https://www.danfoss.com/en/service-and-support/case-stories/dcs/danfoss-leanheat-building-helps-avain-deliver-energy-efficient-heating-to-residents-throughout-finland/ ; https://www.danfoss.com/en/service-and-support/case-stories/dhs/roll-out-in-50-000-housing-units-enercity-ag-optimizes-district-heating-supply-with-leanheat-building/ ; https://www.danfoss.com/en/service-and-support/case-stories/cf/leanheat-makes-buildings-smart/
- Pakruojis AI boilers: https://www.lrt.lt/naujienos/mokslas-ir-it/11/2411020/pakruojo-gyventoju-namus-nuo-siol-sildo-dirbtinio-intelekto-valdomos-katilines
- Hydraulic balancing research: https://www.sciencedirect.com/science/article/abs/pii/S2352710219310617 ; https://www.sciencedirect.com/science/article/pii/S036054422302577X
- DH leak AI: https://www.sciencedirect.com/science/article/abs/pii/S0167865520302038 ; https://github.com/emvollmer/TASeg ; https://www.sciencedirect.com/science/article/pii/S0924271625002321
- Drive-by thermography: https://news.mit.edu/2015/startup-essess-heat-mapping-cars-0105 ; https://senseable.mit.edu/cityscanner/
- LT thermal drone services: https://aerodetect.lt/ ; https://www.termodronas.lt/
- Residential PM2.5 share: https://egusphere.copernicus.org/preprints/2023/egusphere-2023-1194/egusphere-2023-1194.pdf
- Waste-burning fines and PM: https://www.kaipkada.lt/lietuva/ekspertai-perspeja-gyventojus-lietuvoje-namu-sildymas-draudziamomis-atliekomis-gali-kainuoti-iki-keliu-tukstanciu-181023/ ; https://www.birzai.lt/ekologija/atlieku-tvarkymas/atlieku-deginimas/406?lang=lt
- Boiler replacement support: https://enmin.lrv.lt/lt/zaliau/suzinok/parama-tarsiu-katilu-keitimui-i-efektyvesne-sildymo-iranga-tesiama-ir-bus-finansuojama-seserius-metus/
- Camera opacity: https://www.astm.org/d7520-13.html ; https://portal.ct.gov/-/media/DEEP/air/ALTMethod082pdf.pdf
- Polish smoke drones: https://www.themayor.eu/en/a/view/drones-monitor-compliance-with-ban-on-burning-coal-and-wood-in-krakow-3685 ; https://planetsave.com/2018/02/05/katowice-poland-using-drones-locate-illegal-emissions-sources/
- Grid prices: https://www.cleantechlithuania.lt/en/naujienos/inion---elektros-kainu-suoliai-lietuvoje ; https://ignitis.lv/en/business/articles/electricity-market-overview-june-2025
- Battery subsidy and tariffs: https://apva.lrv.lt/lt/naujienos-24316/parama-gyventojams-isirengusiems-elektros-kaupiklius-jau-balandzio-8-d/ ; https://litsol.lt/elektros-tarifai-ir-pasaugojimo-mokestis-gaminantiems-vartotojams-ka-svarbu-zinoti-2026-metais/
- Classroom CO₂: https://sildymas-vedinimas.lt/naujienos/vilniaus-mokyklose-oro-kokybe-neatitinka-normu/ ; https://epublications.vu.lt/object/elaba:16131213/16131213.pdf
