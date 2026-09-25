# WellWatch (*Šulinio sargas*) — make Lithuania's invisible well pollution visible

**Theme:** Sustainability · **Working one-liner:** *"700,000 Lithuanians drink from wells nobody checks. We turned a €0.40 test strip, a phone and a school class into the country's first nitrate map."*

---

## 1. The problem (evidence)

| Fact | Source |
|---|---|
| Lithuania drinks ~**100% groundwater** — one of only two such countries in the EU (with Denmark). Groundwater *is* the national water supply. | [LRT](https://www.lrt.lt/en/news-in-english/19/1874780/europe-s-water-crisis-could-lithuania-become-water-exporting-country) |
| ~**700,000 people** (~1 in 4) get water from their own shaft wells or shallow boreholes, not from the network. | [tv3.lt](https://www.tv3.lt/naujiena/gyvenimas/sulinius-ir-grezinius-turintiems-lietuvos-gyventojams-svarbi-zinia-n1504919) |
| Nitrate contamination found in **every third** tested well; in early 2024, **45% of wells and 51% of boreholes failed** hygiene norms; NVSC cites ~15% over nitrate/nitrite limits. | [LRT](https://www.lrt.lt/naujienos/sveikata/682/2502311/gyventojai-raginami-tirti-vandens-is-suliniu-kokybe-uzterstas-vanduo-pavojingas-sveikatai), [NVSC](https://nvsc.lrv.lt/lt/naujienos/nvsc-kvieciame-pasirupinti-suliniu-ir-greziniu-vandens-tyrimais-4zcl/) |
| Nitrates have **no taste, smell or colour**. They impair blood oxygen transport. Especially dangerous for infants <6 months and during pregnancy. | [NVSC](https://nvsc.lrv.lt/lt/veiklos-sritys/visuomenes-sveikatos-saugos-uztikrinimas/suliniu-vandens-tyrimai-del-nitritu-nitratu/) |
| The **whole territory of Lithuania** is designated a nitrate-vulnerable zone under the EU Nitrates Directive. The source is agriculture (fertiliser, manure) plus septic systems. | [ŽŪM](https://zum.lrv.lt/lt/veiklos-sritys/zemes-ir-maisto-ukis/nitratu-direktyvos-igyvendinimas/) |
| The state offers **free** tests, but only for pregnant women and infants. In 2024 the national lab received **just 241 samples**, and 36 of them were over the nitrate limit. | [NVSC](https://nvsc.lrv.lt/lt/veiklos-sritys/visuomenes-sveikatos-saugos-uztikrinimas/suliniu-vandens-tyrimai-del-nitritu-nitratu/) |
| A lab test costs only **€5 for nitrate** + €20 to deliver the sample (or €27 for pickup). | [NVSPL](https://nvspl.lt/kainos/atmintines/vandens-tyrimai) |

**The real insight:** cost and technology aren't what stop people. **Awareness and hassle** do. The test is cheap, and even the free version gets almost no uptake. Rural, often elderly well owners don't know they are at risk, don't know nitrates are invisible, and won't drive a bottle to a lab within 24 h. **No map exists** that shows people "your area is risky". This is a coordination and visibility problem, which fits a student-led, tech-enabled campaign perfectly.

## 2. The solution

Three layers. Each can be built by a school team; each adds value on its own.

### Layer 1: Strip + phone screening (AI vision)
- A semi-quantitative nitrate/nitrite strip (e.g. MN Quantofix, colour steps **0 / 10 / 25 / 50 / 100** mg/L; the legal limit of 50 sits right on the scale) is dipped and photographed next to a **printed colour-reference card**.
- The app does white-balance correction against the card, then classifies the colour band. The aim is **triage** (below 25 / 25–50 / above 50), *not* lab precision.
- **We answer the known weakness head-on:** a Deltares citizen-science study found phone apps did *not* beat the human eye at reading strips (about ±30%) ([CSTP](https://theoryandpractice.citizenscienceassociation.org/articles/10.5334/cstp.346)). So (a) we only claim triage, (b) we send ~20 of our own samples to the NVSPL lab (€5 each ≈ €100) and **publish our own validation**, and (c) anything ≥25 mg/L is automatically routed to a lab confirmation.

### Layer 2: Risk map (AI / data)
- Open data → a per-grid-cell **nitrate risk score**: land use (arable/livestock density), soil permeability, depth to groundwater, distance to farms/manure storage, well type (shaft vs borehole), plus every strip result collected so far.
- Shows every rural resident *"your area is high risk: test now"*, including people who never heard of the campaign.
- Privacy: results are shown aggregated on a ~1 km grid. Exact well locations never go public (GDPR).

### Layer 3: The campaign (the human engine)
- **Schools are the distribution channel.** Chemistry/biology classes run a "test your grandparents' well" week. Each student tests 3–5 wells in their village. Teacher kit: 100 strips + reference cards + lesson plan.
- The results screen tells the owner what to do: *don't give it to infants*, *boiling does NOT remove nitrates*, lab confirmation, the real fixes (deeper borehole, reverse-osmosis filter, network connection, moving the manure pile).
- Aggregated data goes to the **municipality, NVSC and the Environmental Protection Agency**: target the free tests where they're needed, prioritise water-network extensions, and check farm compliance in hotspots.

## 3. Why it scores (vs. rubric)

| Criterion | Why WellWatch is strong |
|---|---|
| **38.1 Technology** | Computer vision (strip reading with colour calibration), a predictive risk model, a geospatial platform. |
| **38.2 Creativity + research** | Builds on real prior art (Deltares Nitrate App, US Nitrate Watch, WiseH2O) *and* fixes its known weakness. Nobody does this in LT. |
| **38.3 Quality / realism** | A clear causal chain: awareness → test → lab confirmation → action. The strips exist, the lab exists, the €5 price exists. |
| **38.4 Local relevance** | Couldn't be more local: 100% groundwater country, the entire territory a nitrate zone, 700k well users, a free test that nobody uses. |
| **38.5 Completeness** | **We can run a real pilot before Nov 6**: test 100+ wells in one district in October and show real data and a real map in the submission. |
| **38.6 Wider impact / policy** | Data that NVSC and municipalities currently *don't have*. A direct input to where water networks go and to Nitrates Directive enforcement. Could argue for extending free testing beyond pregnant women and infants. |
| **48.3 Global link** | UN SDG 6. Latvia, Estonia, Poland and the US (43M people on private wells) have the same problem. Scales with the same strips and app. |
| **48.4 Legal feasibility** | No medical claims (screening + lab referral); GDPR solved by aggregation; strips are consumer products. |
| **48.6 Reach** | Schools → families → villages. Every student has a grandparent with a well. |
| **48.7 AI/IoT** | AI vision + an AI risk model. IoT stretch goal: a continuous nitrate probe (ISE sensor) in 3–5 village monitoring wells. |

## 4. Prototype plan (fits the calendar)

| When | What |
|---|---|
| By Oct 16 (stage 1) | Short idea form. Order 200 strips (~€80–100). Pick a pilot district (a farming area, e.g. Pasvalys/Biržai/Joniškis karst region, or wherever the team is). |
| Oct 19–31 | App MVP: camera → reference card detection → colour classification → result + advice → anonymous upload. Stack: Flutter or Kotlin + OpenCV / TFLite; map on Leaflet/Mapbox; backend Firebase/Supabase. |
| Oct 19–Nov 3 | **Field pilot**: the team + one class test 100+ wells. Send 20 to the NVSPL lab for validation. |
| Nov 3–6 | Risk-map v0 from open data (CORINE land cover, Geological Survey groundwater maps, soil maps) + pilot results. Build the presentation around **real numbers** ("we tested 127 wells; 31% exceeded 50 mg/L; 4 households with infants"). |
| Stage 3 (mentoring) | Partner letters (municipality public-health bureau, NVSC regional office, school). Scale plan to 10 schools. Stretch: an IoT probe prototype. |

**Team split (3–5 people):** 1 app/CV developer · 1 data/map person · 1–2 field and partner leads (school, municipality) · 1 story/design/pitch lead.

## 5. Budget sketch
- Strips: ~€0.40–0.50 each → 1,000 wells ≈ €500.
- Lab validation: €5/sample + delivery.
- App and hosting: ~€0 (free tiers).
- The whole pilot for one district costs **< €500**. Scaling to 50 schools ≈ €10k/year. That's cheaper than one municipal water-network study.

## 6. Risks & answers (red team)

| Judge's question | Answer |
|---|---|
| "Isn't this health, not sustainability?" | It's **groundwater protection**. Nitrates come from how we farm and handle waste. Groundwater is LT's only drinking water. The map shows where land use is poisoning it. SDG 6 + 2 + 12. |
| "Strips are inaccurate." | Correct, and we measured it ourselves. We use them only for triage, and anything suspicious goes to the lab. |
| "Why doesn't NVSC already do this?" | They lack the reach: 241 samples a year. We bring the distribution channel (schools) and the data layer they lack. We're a helper, not a competitor. |
| "What happens after a bad result?" | A concrete action list + a lab referral + municipal data. Long-term, hotspots justify network extension/filters. |
| "Privacy — you're mapping people's homes." | The public map is aggregated to a ~1 km grid; raw points are only shared with public-health authorities, with consent. |
| "Will the campaign last after the contest?" | The school kit is built for a yearly "Water Week". Municipalities' public-health bureaus (*visuomenės sveikatos biurai*) already run school programmes, so they're the natural owner. |

## 7. Verdict
**Revised score: 88/100.** The strongest combination of *local truth + real data we can collect ourselves + policy hook + low risk*. Weakest point: AI "wow" is moderate. Fix it by making the risk map visually impressive and by (stretch) adding an IoT probe.

---

## 8. Round-2 upgrade: WellWatch 2.0 (fixing the "where's the tech?" problem)

**Honest reassessment:** in version 1.0, remove the phone and the idea mostly still works. People can read strips by eye just as well (Deltares). The real engine is a school campaign. It fails the collapse test. Honest tech score: 3/5 and 2/5 for the AI/IoT bonus.

**The upgrade: build our own sensor.** Nitrate strongly absorbs deep-UV light. Research groups have shown that **cheap UV-LEDs (235 nm + 275 nm for organic-matter correction) + a photodiode** can measure nitrate *without reagents*, at a fraction of the cost of commercial probes (which cost €10k+).
- [Low-cost 235 nm UV-LED detector (J. Chromatography A)](https://pubmed.ncbi.nlm.nih.gov/31151694/)
- [Miniaturised 235 + 275 nm UVC-LED nitrate spectrophotometer (ACS ES&T Water)](https://pubs.acs.org/doi/10.1021/acsestwater.1c00351)
- [UV diode–photodiode portable nitrate system (Sensors 2024)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11359284/)
- [Low-cost nitrate + DOC sensor for groundwater/soil/river water (Env. Sci. Europe 2026)](https://link.springer.com/article/10.1186/s12302-026-01397-6)

**WellWatch 2.0 =**
1. **A €50–80 in-well IoT probe** (UV-LEDs, photodiodes, ESP32, LoRa/NB-IoT) that measures nitrate **continuously**. Nitrate in shallow wells spikes after snowmelt, heavy rain and manure spreading, so a single yearly test misses the peaks. Continuous data shows *when* and *why*.
2. **A handheld version of the same sensor** for school campaigns: pour a sample in and get a number in 10 s. Much more accurate than strips.
3. **The AI risk map** (unchanged), now fed by real sensor data.

**Demo:** dissolve a pinch of garden fertiliser in tap water on stage; the reading jumps past 50 mg/L and the map pin turns red.

**Remaining risks:** deep-UV LEDs (235 nm) cost ~€50–150 each and are fragile; iron and turbidity in well water interfere (the 275 nm channel + calibration against NVSPL lab samples handles this); it takes real optics/electronics skill. **Revised score: 85.**
