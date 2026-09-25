# Red-team A: agriculture and water ideas (DrainScope, ManureWatch, ŽalosDronas)

> Reviewer role: a hostile but fair evaluator. Written 2026-09-25.
> **Evidence labels.** **[S]** means verified in a scout file (scout-water-agri.md, scout-policy.md, scout-nature.md), i.e. taken from a search snippet by the scout. **[K]** means my own domain knowledge (remote sensing, EU agri and environmental law); it is probably right, but check it before it goes on a slide. **[?]** means unverified or a guess.
> No new web evidence was added. The WebSearch budget is exhausted, and WebFetch to govtechlab.lt was blocked by the egress proxy (tried once, for the Radviliškis challenge).

---

## TL;DR

| Idea | Verdict | Why |
|---|---|---|
| **DrainScope / Fix or Rewet** | **GO, with a re-sharpening** | It passes all 7 hard criteria and it's the only one of the three with a published institutional problem statement (Radviliškis GovTech) **[S]**. There are two weaknesses to fix: the pitch has **three different owners mixed up in one output** (farmer, municipality, Environment Ministry), and the demo is "a map". The fix: localise the fault on the **drainage network** so each flag goes to the one party responsible for it, and verify the flags with a drone. |
| **ManureWatch** | **KILL as a standalone** (keep as a slide-level "same pipeline, next use case") | **Fatal technical flaw:** Sentinel-2 is effectively blind over Lithuania for most of the Nov 15 – Mar 20 ban. Cloud, snow, and the Sun only ~10–12° above the horizon at noon in December **[K]** all get in the way. The signal also lasts days at most and vanishes when the soil is tilled. On top of that, "teenagers build a satellite snitch on farmers" is a bad jury image. |
| **ŽalosDronas** | **MAYBE, leaning KILL** | Solid tech and a real legal hook (the 2025 methodology allows drones **[S]**). But it half-fails the **collapse test**: a drone orthophoto plus a human drawing polygons does ~80% of the job. The link to sustainability is weak, and commercial drone game-damage services already exist in DE/PL **[K/?]**. It's the best *demo*, but it's an agri-economics tool dressed as green. |

**My bet: DrainScope, re-sharpened as "the 7-day puddle radar" (details in §1.7).** This is the only idea of the three where satellites + AI do something no person can do, the user has publicly asked for it, and the green payoff (rewetting peat, cutting N runoff) is measurable in t CO₂e and hectares.

---

## 1. DrainScope / "Fix or Rewet"

### 1.1 Recap
Sentinel-1 radar and Sentinel-2 optical imagery, plus AI, flag drained fields that stay wet abnormally long after rain, and flag beaver-flooded ditches. The output is a ranked repair list for the municipal melioration specialist. Failing drainage on peat is labelled "rewet candidate" for the Nature Restoration Regulation.

### 1.2 (a) Skeptical Samsung SfT jury member
- **First reaction:** "Melio... what?" The word *melioracija* is a snooze for a Samsung marketing person. For the expert jurors it signals a team that did real homework. The pitch has to open on the **picture** (a satellite time-lapse where one field stays blue for three weeks while its neighbours dry out), not on the word.
- **Exciting?** Moderately. "Satellites + AI + beavers + climate" is a good story; a 16-year-old explaining radar backscatter credibly is *very* impressive. The risk is that it sounds like a university/GIS-company project that students just fronted. Credibility comes from **the team's own field visits and drone footage**. Without them, the jury assumes a teacher or parent did it.
- **Clear?** It's clear only if it's told as one sentence about one user. The two current scout versions juggle repair, rewet, beaver, CAP grants and N runoff. That is five stories, and juries punish that.
- **Novel?** Yes, against the SfT field. Nobody in the known Baltic finalists did Earth observation (past-winners.md lists apps, QR codes, orienteering **[S]**). It's also novel against the research: tile-drain *mapping* exists, drainage-*failure* scoring over time plus a rewet triage is at least uncommon **[S, scout claim; ?]**.
- **National TOP 5 out of ~70?** Likely, if they show real pilot numbers ("we visited 30 flagged sites; 19 were really waterlogged; random sites: 4 of 15") and a letter from a municipality. Without field data it's a generic "AI on satellites" deck, and it sits around place 6–12.
- **Baltic final?** A strong contender. The local relevance transfers directly: Latvia and Estonia have similarly huge Soviet-era drainage estates **[K]**, and so do Finland, Poland and the US Midwest. The English pitch works because "beavers flood farms, satellites find it, broken peat drains become climate wins" needs no Lithuanian context. The weakness against a flashy hardware team is **demo wow**.

### 1.3 (b) The end user: the municipal melioration specialist
What they'd say in the first 30 seconds, honestly:
1. **"I already know where it's wet. Farmers call me."** This is the killer objection. Farmers are the best sensors of their own fields. The specialist's bottleneck is **money** (a €1 B need against small ŽŪA allocations **[S]**), not detection.
   - *Answer:* the tool's value is not "discovering" wet fields. It's (i) **ranking** objectively when 40 complaints compete for money for 5 repairs, (ii) telling **whose fault it is** (a state-owned collector or ditch vs a private field drain), and (iii) producing **documented evidence** for funding applications and for the 3-yearly inspection duty **[S]**. Also, complaint-driven maintenance favours loud farmers, and absentee landowners/renters never call.
2. **"Half of what you flag isn't mine."** **[K, verify]** In LT, drain lines inside a parcel belong to the landowner. The state owns the main ditches, larger collectors and hydrotechnical structures. A single wet field usually means a *private* problem.
   - *This is the most important fix* (§1.7). Localise the fault on the network. If many parcels in one drainage system stay wet, the shared collector, ditch or outlet (a state asset) is suspect, and that's the municipality's job. If one parcel is wet, it's private: notify the farmer and point them to the CAP reconstruction grant.
3. **"Beavers: I know where they are, and I can't legally remove them anyway."** **[S]** says municipalities often can't. The beaver layer is useful as evidence for permits and for the hunting-ground users. It's not a headline.
4. **"Rewetting isn't my department."** Correct. Rewetting decisions sit with the Environment Ministry (AM) / the national restoration plan and the landowner. The rewet layer has to go to a *second* user (AM/APVA, peatland LIFE projects), not to the drainage engineer, who is institutionally there to keep land drained.
5. **What they use today [K/?]:** Mel_DR10LT in the GIS (via ŽŪDC/geoportal), paper and Excel inspection logs, farmer complaints, the orthophoto. Possibly nothing satellite-based. The Radviliškis challenge **[S]** implies there's no off-the-shelf tool.

Would they use it? **Yes, if it's a free web map that exports a PDF/Excel list and costs them zero hours to learn.** No, if it needs QGIS skills or has more than ~40% false positives. The Radviliškis specialist is the natural first user because they literally wrote the problem down.

### 1.4 (c) Domain scientist: does it actually work?
**What works [K]:**
- Sentinel-1 C-band VV/VH backscatter responds to soil moisture and strongly to **standing water** (specular reflection means very low backscatter). Open-water/pooling detection at 10–20 m is operational (flood mapping, Copernicus EMS).
- Revisit: Sentinel-1B failed in Dec 2021. Sentinel-1C was launched in Dec 2024 and Sentinel-1D in late 2025 **[K; check operational status]**, so a revisit of roughly 6 days or better over LT (with multiple relative orbits) is plausible in 2026.
- Sentinel-2 NDWI/MNDWI on clear days gives clean confirmation. Pooling of ≥0.1 ha is 10+ pixels, so it's detectable.
- **Failing drains are spatially persistent.** A collapsed collector makes the *same* patch wet after every heavy rain and every snowmelt, year after year. This is the key scientific gift: **the team can mine the historical archive (2017–2026 spring snowmelts) and doesn't depend on autumn 2026 weather.**

**What's hard / the confounders [K]:**
1. **Tillage and crop cover dominate backscatter.** In autumn, ploughing changes surface roughness abruptly, which shifts backscatter by several dB, as much as moisture does. Winter crops growing change VH. A naive "backscatter anomaly" = a "just-ploughed field" detector. *Mitigation:* use **ratios relative to neighbouring parcels on the same date and the same crop/tillage state**, focus on *standing water* (very low VV, strong signal) rather than subtle moisture, and use S2 on clear days to know the crop/tillage state.
2. **Natural depressions and heavy clay** stay wet even with perfect drainage. *Mitigation:* use a DEM (LT has LiDAR-derived elevation **[K/?]**), flag topographic sinks, and above all use **temporal change**: a patch that *used to* dry in 3 days and now takes 14 is a failure; a patch that was always wet is a sink.
3. **Frozen soil / snow** (Dec–Feb) makes SAR moisture signals meaningless. The useful windows are Mar–May (snowmelt, best) and Sep–Nov.
4. **Beaver dams themselves are invisible at 10 m.** Ditches are 1–5 m wide. Only the *upstream flooding* is visible, if it's large enough. Dams are visible on the national orthophoto (≈0.5 m or better **[K/?]**) or by drone. The EEAGER and Ontario results **[S]** used higher-resolution imagery and larger landscapes. So there's a resolution gap: "we find beaver ponds, not beaver dams."
5. **Cloud:** it's not fatal thanks to S1, but S2 confirmation in Oct–Nov will be rare (a few usable scenes a month, at best **[K]**).
6. **Ground truth is scarce.** No labelled dataset of failed drains exists. So the "AI" should be honest: an **anomaly detector with physically meaningful features** (days-to-dry after a rain event, relative to neighbours and to the parcel's own history), plus a small classifier trained on the team's own field labels. A deep net with 50 labels would be theatre.

**Is there a fatal technical flaw?** **No.** The claim has to be scoped to *"persistent surface waterlogging on drained land, relative to neighbours and history"*. It must not be *"we detect broken pipes"*. At that scope it's proven physics. A realistic precision is 50–70% on the top-ranked flags after tillage filtering **[my estimate, ?]**, which is still several times better than random inspection.

**The CO₂ number:** the IPCC 2013 Wetlands Supplement Tier 1 factor for temperate cropland on drained organic soil is on the order of ~8 t CO₂-C/ha/yr (≈29 t CO₂/ha/yr); grassland is lower **[K, check the exact table values]**. Rewetting 100 ha of failing peat cropland is then ~2,000–3,000 t CO₂e/yr. That's a big, credible, slide-worthy number, *if* the factor is cited properly.

### 1.5 (d) The 16-year-old team building it in 6 weeks
**What they'd build:**
1. **Google Earth Engine** (a free account for education/non-commercial use) plus Python (geemap). The S1 GRD and S2 SR collections are preprocessed, so they don't need SNAP.
2. The parcel layer: Mel_DR10LT drained systems and the soil map (peat) from geoportal.lt/ŽŪDC **[S; access conditions ?: may need registration]**. The LPIS parcels, or just a grid.
3. Rain events from the LHMT (Lithuanian Hydrometeorological Service) station data or ERA5 in GEE.
4. The feature: for each parcel and each rain event, *days until backscatter/NDWI returns to baseline*, as a z-score against parcels within 2 km, then a z-score against the parcel's own 2017–2025 history.
5. A small web map (Leaflet/Streamlit) with a ranked list, a time-lapse per parcel, and a "confirm / false alarm" button.
6. Field verification: **drone** (DJI Mini-class) and phone photos at 20–30 flagged sites and ~15 random controls.

- **The hardest part:** not the code. It's (i) **filtering out tillage/crop artefacts** so the first field trip doesn't return 80% false alarms, and (ii) **getting a municipal specialist on the phone** and into one field trip. Start calling Radviliškis in week 1.
- **Real pilot data by Nov 6? Yes.** It's the easiest of the three. The historical archive is available on day 1. October 2026 rains give live events. Flagged sites are fixed, public places (along ditches, visible from field roads), so the students need no access to any farm. Weekend field trips are enough.
- **The stage demo:** (1) a split-screen time-lapse after a real October 2026 rain, with neighbours drying and one field staying blue; (2) click it to see the official map say "drainage OK"; (3) cut to the team's own drone video of that field under water, with the specialist's quote; (4) press "rank" and the municipality's top-10 list appears with owner (state/private), estimated €, and "rewet: X t CO₂/yr".
  - *Optional IoT:* a €30–40 ultrasonic water-level logger (ESP32 + LoRa/LTE) in one flagged ditch shows live on stage as ground truth. It's a nice touch, but not required, and it must not become "we put sensors in every ditch".
- **Fun/cool?** For a team that likes code and maps, yes: real space data, drone flights, mud. It's less fun for a team that wants to solder a gadget. Honest take: the demo is 7/10, and it gets to 8/10 only with strong drone footage.

### 1.6 Fatal flaws and fixable weaknesses
**Fatal flaws:** none, if the claim is scoped correctly.

**Fixable weaknesses and fixes:**
| Weakness | Fix |
|---|---|
| "I already know, farmers call me" | Pitch it as **ranking + fault ownership + evidence**, not discovery. Show absentee-landowner fields that no one reported. |
| One wet field = private, not municipal | **Network fault localisation**: aggregate flags by drainage system/collector catchment. A cluster means a state asset, a single parcel means private. |
| Rewet ≠ the drainage engineer's job | Make it a **second output layer for a second user** (AM / restoration plan). The municipality benefits by *not* spending repair money there. |
| SAR is confused by tillage | Compare against neighbours with the same S2-derived tillage state; target standing water; use the snowmelt archive. |
| Beaver dams are sub-pixel | Say "beaver ponds". Confirm dams on the orthophoto/drone. |
| The Radviliškis challenge may already be solved by a company **[?]** | **Find out in week 1** (phone GovTech Lab / Radviliškis). If solved, partner with the winner or differentiate (the open, free, rewet-triage angle). If unsolved, it's the best possible evidence. |
| Map-only demo | Drone footage of the flagged field + a live rain-event time-lapse + an optional ditch-level logger. |
| Too many stories | One sentence, one user (see the pitch below). |

### 1.7 Sharpened version: "DrainScope: the 7-day puddle radar"
- The law already says pooling that lasts **>7 days** must be reported **[S]**. Nobody can watch 2.6 M ha **[S]** for 7 days. Satellites can.
- The core engine: for every rain/snowmelt event, radar measures **how many days each drained parcel stays waterlogged**, compared with its neighbours and with its own past years.
- **Fault localisation on the drainage network (the new part):**
  - *Many parcels in one drainage system got worse together* → a suspected **state collector/ditch/outlet/beaver pond** → the municipal repair list, ranked by hectares affected per € of repair.
  - *A single parcel got worse* → a private drain failure → a notice to the landowner plus a pointer to the CAP reconstruction grant.
  - *A failing system on peat soil* → a **"don't rebuild, rewet" candidate** → sent to the Environment Ministry / national restoration plan list, with t CO₂e/yr and € repair avoided.
- Verification: student drone flights and one ditch-level logger. The specialist's confirm/reject taps retrain the classifier.
- **One-sentence pitch:** *"Lithuania's Soviet-era drainage is collapsing under 2.6 million hectares, and no one can see where. Our satellite AI finds every field that stays flooded more than 7 days, works out whether a state ditch or a private pipe is to blame, and turns failing peatland drains into climate wins instead of repair bills."*

### 1.8 Scores
| Criterion | Score | Note |
|---|---|---|
| Collapse test | **9** | Time-series across thousands of parcels is impossible by eye |
| Adoption loop | **7** | The user and budget line are real **[S]**. Owner confusion and "I already know" cost points; the network fix brings it to 8 |
| Proven tech | **8** | S1/S2 water detection is operational; the failure-scoring application is new |
| Measurable impact | **8** | Precision vs random, inspector-hours per failure, ha, t CO₂e (IPCC factor) |
| Novelty | **8** | New to SfT; tile-drain research exists abroad; the Radviliškis status is unknown |
| Demo wow | **6** | 7–8 with good drone footage and a time-lapse |
| Local evidence | **9** | ŽŪM 74% worn, 171k vs 2 M ha gap, GovTech challenge, 7-day rule **[S]** |
| Jury appeal | **7** | Strong for expert jurors, less so for a general audience; English-final friendly |

**VERDICT: GO.**

---

## 2. ManureWatch

### 2.1 Recap
Sentinel-2 detects freshly spread manure/slurry during the ban period (Nov 15 – Mar 20 **[S]**) or near water, and gives AAD inspectors a target list.

### 2.2 (a) Jury
- Sustainability is obvious (nitrates, the Baltic Sea: 56% of LT's N load comes from agriculture **[S]**). But the framing is **surveillance of farmers by students**. In a country where many jurors and team families are rural, that lands badly. Samsung wants "hopeful tech", not a "catch-a-farmer app".
- Novelty against SfT is high. Against research it's moderate (Italy/France papers **[S]**).
- Would it make the TOP 5? Possibly, on novelty. But the first technical juror to ask "how many clear Sentinel-2 images of Lithuania do you get in December?" sinks it. A Baltic final win is unlikely.

### 2.3 (b) End user: the AAD inspector
- First 30 seconds: *"Nice. But in winter I get calls from neighbours about the smell, and that's how I find them. And where's your image from last December? Your satellite couldn't see through the clouds."*
- What the violations actually are **[K/?]**: many manure findings concern **storage** (leaking lagoons, heaps on the field edge, records), not only spreading timing. The 26% hit rate **[S]** doesn't say it's spreading-related.
- Legal use: a satellite flag can justify an inspection but likely isn't evidence alone **[K]**. Data-protection questions about per-parcel profiling by a non-state actor **[?]**.
- Would they use it? Maybe in the March/November shoulder weeks. It's not a year-round tool.

### 2.4 (c) Domain scientist: the fatal flaw
1. **Illumination and cloud [K]:** at 55°N, noon solar elevation in late December is ~11–12°. S2 passes at ~10:30 local solar time, so the Sun is even lower. Many acquisitions over LT in Nov–Jan are cloud- or snow-covered or have a solar zenith angle so high that surface reflectance is unreliable. **For the core of the ban period, the sensor is effectively blind.** SAR can't see manure.
2. **Short-lived signal:** slurry infiltrates or dries within days. Solid manure is often incorporated soon after spreading (incorporation rules exist **[K/?]**), and ploughing creates dark, moist soil, the same spectral direction as manure, so there are false positives. The EOMI studies **[S]** worked on bare soil in clear conditions, matching the image date to the spreading date.
3. **Injection** (increasingly common for slurry) leaves little signal.
4. The F1≈0.9 result **[S]** was obtained under good conditions on bare soil. Transfer to LT winter conditions is unproven, which is exactly the "hopefully the science works" pattern the team rejected.

**Fatal flaw: yes.** The ban period, the one time the detection matters legally, is when the sensor works worst.

### 2.5 (d) Team
- The pilot requires legal spreading events in Sep–Oct that happen to fall within 1–3 days before a clear S2 overpass, *and* a farmer who tells them the dates. It's possible with one cooperative farmer, but it's fragile.
- The demo: a spectral curve jump. Low wow.
- Proud? Probably not; it's an uncomfortable story to tell at school.

### 2.6 Fixes and sharpened version
- There isn't a fix that makes it a winning standalone. The best salvage: **ManureWatch becomes "feature #2" of the DrainScope pipeline**. "Fields that stay waterlogged are also the fields where spreading is banned; our wetness map tells a farmer *today* 'don't spread on parcels X, Y'." That's a *farmer-facing advisory*, not enforcement. It's a nice "platform" slide, not the pitch.
- Sharpened pitch (for the slide): *"The same wetness radar tells farmers which fields are too wet to spread manure this week, so nitrogen stays in the soil, not the Nemunas."*

### 2.7 Scores
Collapse **8** · Adoption loop **5** · Proven tech **4** (in LT winter conditions) · Measurable impact **6** · Novelty **8** · Demo wow **4** · Local evidence **7** · Jury appeal **4**.

**VERDICT: KILL** (fold it into DrainScope as a future feature).

---

## 3. ŽalosDronas

### 3.1 Recap
A drone flight plus AI segmentation produces a crop-damage map, a € value per the 2025 LT methodology, and a pre-filled report for the municipal game-damage commission.

### 3.2 (a) Jury
- **Best live demo** of the three: a real drone, a real field, a heat-map, a € number.
- But: **"How is this sustainability?"** The scout itself admits it's the weakest green link **[S]**. The theme is "a greener tomorrow", and boar damage accounting is agri-economics. The human-wildlife coexistence argument is a stretch the jury will see through.
- Novelty: drone crop-damage assessment is a known genre (agri insurers, DE game-damage appraisers **[K/?]**, Belgian research from 2017–18 **[S]**). A juror who Googles "Wildschaden Drohne" finds commercial services **[K]**. That's "applied in LT", not "new".
- National TOP 5: possible on demo strength and the legal hook. It's unlikely to win the Baltic final on the sustainability criteria.

### 3.3 (b) End user: the municipal commission, the farmer, the hunting club
- **Commission:** usually a municipal representative, a hunters' representative, the farmer and sometimes an agronomist **[K/?]**. First 30 seconds: *"Who flies it? Who's liable if the hunters contest the AI? We see maybe 10–40 claims a year **[?]**, and we walk them in an hour."* Area isn't the only disputed number. **Yield-loss severity**, crop stage, and *which species* did it are also disputed, and the AI doesn't settle those.
- **Hunting club (the payer of damage):** would love objective, smaller numbers. It would also fight any tool the farmer brings.
- **Farmer:** would like it if it raises the number, and oppose it if it lowers it.
- **Who buys:** unclear. The municipality doesn't pay the damage and has little incentive to buy software for a handful of claims. The realistic channel is *drone-agronomy service firms* that already exist **[?]**, which makes it a company service, not a student idea with an adoption loop.
- **What they use today:** tape measures, GPS walking, sampling plots per the methodology. Some already use drones **[S: the methodology allows them; Kaunas district is looking]**.

### 3.4 (c) Domain scientist
- Segmentation of lodged/eaten maize, rooted grassland and wallows from RGB orthomosaics is proven (84–95% accuracy **[S]**). Photogrammetry with OpenDroneMap on consumer-drone imagery works.
- Weak spots: (i) **partial damage** (grazed winter cereals, trampled but standing maize) is much harder than bare rooting; (ii) converting area to €, per the methodology, needs a yield-loss % the camera can't measure without a DSM/height model plus ground calibration; (iii) small winter-cereal browsing by deer is almost invisible in RGB.
- **Collapse test issue:** a human outlining polygons on the orthophoto in QGIS achieves most of the accuracy. AI saves minutes, not a capability. That's close to the "phone reads the nitrate strip" wrapper pattern the team rejected. **This is the core weakness**, not the technology.
- No fatal *technical* flaw. The flaw is **conceptual (collapse and green link)**.

### 3.5 (d) Team
- Build: a DJI Mini-class drone, an automatic grid flight (Litchi / DroneDeploy / the DJI app), OpenDroneMap, then label ~200 tiles and train YOLOv8-seg / U-Net, then crop × yield × price, then a PDF act.
- Hardest part: getting to **real damaged fields in October** (boar rooting on grassland is common in autumn **[S]**; maize is mostly harvested by then **[K]**). Also the drone rules: EU open category A1/A3, a minimum age of 16 unless the state lowers it **[K; check LT TKA]**. The teacher may need to be the pilot.
- Real pilot data by Nov 6: **Yes**, if a hunting club or farmer cooperates. 3–5 plots are realistic.
- Demo: fly a mini drone on stage over a printed field, and a damage map with a € figure pops out. It's genuinely fun. **The team would enjoy building this most.**
- Proud? Yes of the build, less so of the "why".

### 3.6 Fixes and sharpened version
- **Could it be made green?** The only credible pivot is **beaver damage → drainage** (links to DrainScope) or **"damage data → targeted, non-lethal prevention"** (e.g. which fields need electric fencing or deterrents, so fewer animals are culled). Both are weaker than the original's clean legal hook.
- Best use: **the drone becomes DrainScope's verification instrument**. The team keeps the fun drone-flying and the orthomosaic/segmentation skills, applied to *flooded patches and beaver ponds* on satellite-flagged fields. That merges the best demo with the best idea.
- Standalone sharpened pitch (if the team insisted): *"One 10-minute drone flight replaces a disputed tape-measure walk: AI maps every m² that boars destroyed and fills in the official compensation act, so farmers and hunters stop going to court."*

### 3.7 Scores
Collapse **5** · Adoption loop **6** · Proven tech **8** · Measurable impact **6** (time and € error, not environmental) · Novelty **5** · Demo wow **8** · Local evidence **8** · Jury appeal **5** (the green-link problem).

**VERDICT: MAYBE → effectively KILL as the SfT sustainability entry.** Keep the drone as a DrainScope component.

---

## 4. Combined recommendation

**Bet on DrainScope, sharpened to the "7-day puddle radar" with network fault localisation, using the drone from ŽalosDronas as the verification instrument and ManureWatch as a one-slide "what the same pipeline can do next".**

### Week-1 must-dos (these kill or confirm the bet)
1. **Phone Radviliškis district municipality's melioration specialist and GovTech Lab**: was the challenge solved, and by whom? Would they review 20 flags and sign a letter? *(If a company already runs this for them, the novelty story needs reworking.)*
2. **Check the ownership rule**: which drainage elements are state-owned (collector diameter threshold? ditches?) vs private. This decides the fault-localisation logic. **[K/?]**
3. **Get Mel_DR10LT and the soil/peat layer** (geoportal.lt / ŽŪDC): check licence and access.
4. **Run a quick feasibility test in GEE:** take one known flooded area from spring 2025 snowmelt (from news or the specialist) and confirm it stands out in S1 against its neighbours. If it doesn't show within 3 days of work, reconsider.
5. **Confirm the IPCC Wetlands Supplement emission factors** and LT's drained agricultural organic-soil area (the national GHG inventory) for the CO₂ slide.

### Kill criteria for DrainScope
- The GEE test shows no separable signal on known wet sites after tillage filtering.
- **Or** the first field trip gets fewer than 30% of the top-20 flags confirmed.
- **Or** Radviliškis/GovTech reveals an existing operational national tool (e.g. ŽŪDC already does satellite wetness monitoring).
