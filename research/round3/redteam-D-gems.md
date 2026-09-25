# Red team D: gem hunter (overlooked ideas, hybrids, pattern check, overall top 7)

> Round 3, written 2026-09-25. Inputs: `BRIEF.md`, all eight `scout-*.md` reports (~200 ideas), `ideas/round2-tech-first.md`, `research/past-winners.md`.
> **No web searches were used here** (the session budget was exhausted). Every fact comes either from the scout files, with their links and their own verification tags, or from my background knowledge. Background-knowledge claims are marked **[unverified]**. Nothing new is invented as a statistic.
> The front-runners (DrainScope/Fix-or-Rewet, ManureWatch, ŽalosDronas, HopperGuard, HeatTwin, ChimneyWatch, BriedisStop, ArtiMetras/OvertakeSense, SchoolGate) are **not re-evaluated** here. They appear only in the pattern check, the hybrids and the final ranking.

Score key (1–10): **Col** = collapse test · **Adp** = adoption loop · **Prv** = proven blocks · **Mea** = measurable · **Nov** = novelty/not saturated · **Demo** = demo wow · **Loc** = local evidence · **Jury** = jury appeal.

---

## 0. TL;DR

- **Gem 1: Druskos radaras → "MedžiųSargas" (road salt vs city trees). GO.** It is the most underrated idea across all scouts: it's a nature story in a city, the evidence is emotive and local (dying Vilnius trees, a protest, salt still visible in summer 2026), the physics is proven (road-surface thermal mapping), and the sensor is a €10–15 IR thermometer. The team can collect real data in October: a thermal "fingerprint" of the streets plus soil salinity at street trees.
- **Gem 2: FishPass Counter → "Lašišų skaitliukas". MAYBE, and GO if a fish-pass access letter arrives within 2 weeks.** It's the team's favourite kind of idea (nature, hardware, a live-fish demo). The official LT method is literally humans watching fish-pass video, and the salmon run happens during the pilot window. Its fatal risk is access, not the tech.
- **Gem 3: Šernų skaitliukas (camera-trap AI census). MAYBE alone, but GO as part of Hybrid H1.** On its own the novelty is integration only. Combined with ŽalosDronas it gives the hunting club two pains that the same product solves, and that is a much stronger adoption loop than either idea has alone.
- **Best hybrids:** **H1 "Šernas 360"** (ŽalosDronas + camera census, with one user who pays twice), **H2 "MedžiųSargas"** (salt + street-tree soil + canopy, one causal chain from the spreader to the NRL), and **H3 "Dviračio radaras"** (the OvertakeSense bike box plus a downward IR thermometer: close passes in autumn, bike-path ice in winter).
- **Overall top 7:** 1 BriedisStop · 2 HopperGuard · 3 ŽalosDronas (as H1) · 4 ArtiMetras/OvertakeSense (as H3) · 5 MedžiųSargas (Druskos radaras, as H2) · 6 DrainScope/Fix-or-Rewet · 7 HeatTwin. Wildcard: FishPass Counter.

---

## 1. The gem hunt: which low-ranked ideas deserve a second look?

I re-read every idea a scout killed or ranked below its top 2 and asked one question: *did the scout kill it for a real fatal flaw, or for a fixable one?*

| Idea (scout) | Scout verdict | Real fatal flaw? | My call |
|---|---|---|---|
| **Druskos radaras** (mobility #2) | backup | No. "Salt number needs winter" is fixable: October gives the thermal fingerprint and last winter's soil salt is measurable now | **GEM 1** |
| **FishPass Counter** (water #3; killed by global #13 as "season over") | backup / kill | The global scout's "season over" is **wrong**: the water scout says salmon and sea trout run upstream in Oct–Nov, which matches the pilot. The real risk is access | **GEM 2** |
| **Šernų skaitliukas** (nature #3) | #3 | Novelty is integration only, which fusing with ŽalosDronas fixes | **GEM 3 (via H1)** |
| ActiveLens (sport #1) | top sport | Partly. A judge sees "phone on a tripod + pose AI in PE", the exact pattern the brief bans (KneeGuard), and SkillFit already won Europe with AI in PE. Video-based MVPA validity has no citation yet | MAYBE (best sport fallback) |
| Geltonas algoritmas, school-bus routing (mobility #3) | keep | No fatal flaw (C9, P9, M9, and Boston saved $5M), but no hardware, no nature and no wow. It's the opposite of the team's taste | MAYBE (honourable mention) |
| CanopyZero (policy P3) | keep | As a standalone it's a dashboard, and Copernicus may publish the official baseline | KILL alone → **module of H2** |
| PelkėsPulsas (nature #5) | #5 | It duplicates DrainScope's rewet layer | MERGE into DrainScope |
| LeakPatrol (energy #3) | #3 | Street-level oblique thermography for DH leaks is **not proven** (the scout admits it), and LT drone-thermography firms exist | KILL alone → module of H4 |
| BarštisScan (nature #4) | #4 | Yes for this season: by Oct–Nov hogweed is dead stalks, so no honest pilot data | KILL for 2026 → summer module of H4 |
| StreamWarn (global #4) | top 4 | LT small-stream flood evidence is weak (Loc 4), and there's no flood before Nov 6, so impact is unprovable | KILL |
| GridPulse (energy #4) | caveats | Adoption 4: the household aggregation route into Litgrid reserves is unverified, and it needs an electrician inside every water heater (safety) | KILL |
| Vape-back (waste #5) | maybe | Yes: why would a teen bother, and there's no deposit | KILL |
| BirdNET on old Galaxy phones (nature #15) | kill (close) | Yes: nobody pays and nobody acts on the output. The Samsung upcycling angle is cute, though | KILL (reuse the "old Galaxy as sensor" line in any hardware pitch) |
| Beaver-dam detector (nature #7, water #4) | merge | Already a DrainScope feature | MERGE |
| Smoky-car screener (mobility #4) | risky | Yes: student-grade PM/CO₂ sensors are likely too slow for single-car plumes, which is "hopefully the science works" | KILL |
| Thermal-drone ASF carcass search (nature #6) | runner-up | Yes: fails under canopy, no carcasses to pilot on, drone cost | KILL |
| Live Sorting Index (waste #2) | #2 | Needs plant access, and the camera sees only the top layer | MAYBE-KILL (a HopperGuard mode at best) |
| OpenHall, LeagueMesh, HoopStats, PulseClass (sport) | mid | OpenHall replaces a person (weak collapse). LeagueMesh has no wow. HoopStats and PulseClass are commercial (Pixellot, Polar) | KILL |
| Ice-safe 2.0 (round 2) | runner-up | No ice before Nov 6, and liability | KILL for this timeline |

---

## 2. The three gems, given a fair but brutal hearing

### GEM 1: Druskos radaras → "MedžiųSargas" (precision salting to save street trees)

**One-line pitch.** *"Vilnius spreads salt on every street because it can't see which ones will freeze. Our €15 sensor on vehicles that already drive at night maps road-surface temperature street by street, so salt goes only where ice will form, and we measure the result in the soil around the trees that are dying from it."*

**What the tech physically does.**
- An IR thermometer (MLX90614-class, ~€10–15 **[price unverified]**) points at the asphalt. With an air temperature/humidity sensor (dew point) and GPS on an ESP32 or an old Galaxy phone, it logs the surface temperature every few metres.
- Repeated night drives build a **thermal fingerprint** of the city. Bridges, shaded courtyards and underpasses freeze first, and the *relative* pattern stays stable from night to night. That stability is the principle behind UK-style route-based road-weather forecasting ("thermal mapping") **[well known in road-weather literature; unverified here]**.
- A gradient-boosting model combines the fingerprint with the LHMT forecast to predict tonight's freeze risk per segment and output a salt / reduced dose / gravel / nothing plan.
- The loop closes with a €20 soil EC meter at street trees, and with Vilnius's existing >500 soil conductivity sensors (mobility scout) to measure salt in the soil after each decision.

**Collapse test.** Passes. Surface temperature and black ice are invisible, and crews decide per district from the *air* forecast. You can't do sub-street resolution by eye or with a spreadsheet.

**Adoption loop (one breath).** The city's street-maintenance operator gets a nightly per-street salting plan on a tablet. The municipality pays, because it pays for salt, spring tree washing (≥70 L per tree) and tree replacement, and it is under public pressure after the tree protest. The sensors ride on vehicles that already drive at night. *Check:* whether Vilnius salting is done by a municipal company (I believe "Grinda" **[unverified]**) or by contractors paid per tonne. If contractors are paid per tonne, the incentive is reversed and the plan has to go into the contract (the scout flags this too).

**Where it's proven.** MnDOT "Salt Solutions": pavement-temperature-driven salting, with accidents down 6% in year 1 ([MnDOT](https://mdl.mndot.gov/_flysystem/fedora/2023-06/199820.pdf)). Research on spreader automation ([arXiv 2010.12983](https://arxiv.org/pdf/2010.12983)) and on ML precision dosing ([ScienceDirect 2025](https://www.sciencedirect.com/science/article/pii/S2095756425000820)). Commercial mobile sensors exist (Vaisala and others, at €1k+ **[unverified]**). The cheap-sensor, city-sidewalk, tree-outcome combination is the new application.

**Real pilot data before Nov 6 (this is why it's a gem).**
1. **Soil salt survey now:** EC at 30 street trees on heavily salted vs lightly salted streets vs a park control. That gives "X g/L salt is still in the soil in October" (the arborist measured 0.5–8 g/L). Add leaf-scorch photos. It's real nature data.
2. **Thermal fingerprint:** 4–6 October night drives on the teacher's car (October night frosts are common in LT **[unverified climatology; check LHMT]**). The key output is "segments of the same street differ by X °C", which is the number that makes precision salting credible.
3. The salt-saving number is honestly scoped as the "pilot for winter 2026–27", with a *simulated* saving: re-run last winter's LHMT nights against our fingerprint to show how many street-nights didn't need salt.

**Demo.** A tabletop street of tiles, one chilled with an ice pack. A toy truck carrying the real sensor drives over them, the map turns the frozen tile red, and a "salt only here" plan appears. Then show the real thermal map of our town, and a jar of soil from a dying linden with its EC reading.

**Fatal-flaw check.**
- ⚠️ **"The city already fixed it"**: salt went 85,000 t → 38,300 t → 23,500 t. A judge could say the problem is solving itself. *Answer:* those cuts were blanket cuts, salt was *still* visible in summer 2026, and precision is how you cut further without a safety trade-off. **This is the objection to rehearse.**
- ⚠️ The scope of the salt figures (Vilnius only?) needs confirming (the scout flags it).
- ⚠️ Liability for under-salting. The model only *reduces* salt where the surface is provably above freezing, and the default stays "salt".
- ✅ Not a sensor-on-every-tree problem: a handful of vehicles.
- ✅ Not saturated: no student or LT municipal precedent found (unverified).

**Scores.** Col 8 · Adp 6 · Prv 8 · Mea 7 · Nov 8 · Demo 7 · Loc 9 · Jury 8 → **61/80**. **Verdict: GO** (as a top-6 candidate, strongest as Hybrid H2).

---

### GEM 2: FishPass Counter → "Lašišų skaitliukas" (an AI that counts every fish climbing LT's fish passes)

**One-line pitch.** *"Lithuania checks whether its 25 fish passes work by having people watch hours of underwater video. Our €150 edge-AI camera counts, measures and identifies every fish 24/7, and it caught this autumn's salmon run."*

**What the tech physically does.** A waterproof camera (Pi HQ or a phone in a housing) watches the fish-pass viewing window or a narrow slot, with an LED backlight for murky water. YOLO detection plus tracking decides the *direction* (up or down), estimates length from a known reference grid, and classifies species (salmon, sea trout, lamprey, cyprinids). Only clips and counts are uploaded over LTE/LoRa.

**Collapse test.** Borderline-pass, at 7. Humans *can* count video, and that's the official method ([e-seimas methodology](https://e-seimas.lrs.lt/rs/legalact/TAD/TAIS.262038/)). But they can't do it 24/7 for a whole season across 25 passes, which is why monitoring is sparse. This is "automation of a legal method", the same logic that made Minova win (humans *can* forecast demand, just badly).

**Adoption loop.** The Environmental Protection Agency (AAA), its monitoring contractor (Gamtos tyrimų centras, which wrote the fish-pass evaluation report [PDF](https://aaa.lrv.lt/uploads/aaa/documents/files/Zuvitakio+vertinimo+galutine+ataskaita.pdf)), and hydropower operators who must keep passes working install one box per pass. The output is continuous counts plus the legal efficiency metric (>90% = efficient, <75% = not). That becomes evidence for fixing or removing barriers under the NRL free-flowing-rivers target. That means 25 units nationwide: a realistic deployment.

**Where it's proven.** Riverwatcher/Vaki fish counters (IS/NO) are commercial and widely used **[unverified details]**. Deep-learning fish counting in fishways is a well-published research area **[citations still to add; the water scout ran out of budget]**.

**Demo.** The team's taste wins here: **a small aquarium with live fish** (or fish models on rods) swims past a "fishway window" on stage, and the screen draws "Salmo trutta · 54 cm · ↑ upstream · count 17". Then show real footage and counts from an LT fish pass in October. Demo wow is high, and the jury is kids-and-nature friendly.

**Measurable.** Fish per species per week, pass efficiency %, and manual video hours replaced (ask the contractor for their hours per season).

**Fatal-flaw check.**
- ❌→⚠️ **Access** is the potential killer. Without a signed OK to put a camera in a real pass by ~Oct 10, there's no real pilot data. *Mitigation:* email AAA / Gamtos tyrimų centras / a small-HPP owner in week 1. The fallback is to ask for existing archived fish-pass video and show AI counts vs the official human count, which is still real LT data and arguably the stronger validation.
- ⚠️ **Tiny numbers:** LT salmon runs through one pass may be only tens of fish **[unverified]**, and the camera could see zero salmon in 3 weeks. Count all species, with salmonids as the highlight.
- ⚠️ **Prior art:** commercial counters exist, so the pitch is the cheap version plus an open model plus 25 LT passes. Don't claim invention.
- ⚠️ **"So what?"** (the global scout's objection): counting has to lead to a *decision*, meaning which passes fail the 75% test and which dams to prioritise for removal under the NRL. Frame it that way or it dies.
- ⚠️ Is video used at *all* 25 passes today? **[unverified]**

**Scores.** Col 7 · Adp 6 · Prv 8 · Mea 7 · Nov 7 · Demo 8 · Loc 7 · Jury 8 → **58/80**. **Verdict: MAYBE → GO only if access is secured in the first 2 weeks.** It's the best "wildcard" for the team's taste.

---

### GEM 3: Šernų skaitliukas (camera-trap AI census for hunting clubs)

**One-line pitch.** *"Lithuania sets hunting quotas, pays crop-damage claims and fights African swine fever using a snow-track census that its own critics call pointless. Hunters already own trail cameras, and our AI turns their SD cards into a real density per km²."*

**What the tech physically does.** MegaDetector crops the animals, a European species classifier (DeepFaune) labels them, and the **Random Encounter Model** (REM, EFSA/ENETWILD-validated) turns detections, camera field of view and animal day-range into density ± CI. An app generates a random camera-placement protocol, so the maths is valid.

**Collapse test.** Passes, at 8. Tens of thousands of photos per club per season, and density needs statistics. Neither is doable by eye.

**Adoption loop.** Hunting clubs must run the census (mandatory), already own cameras (sold widely in LT), and dislike the current chore. LMŽD (the hunters' association) or the ministry deploys it as a shared tool. VMVT gets boar density for ASF zones. **Weak point:** the ministry has to accept camera-based census as a valid method. That's a real *policy* change, which is also a jury plus ("could influence local policy").

**Where it's proven.** ENETWILD/EFSA harmonised camera-trap REM for boar in 19 European areas ([EFSA 2022](https://www.efsa.europa.eu/en/supporting/pub/en-7214), [EFSA 2024](https://efsa.onlinelibrary.wiley.com/doi/abs/10.2903/sp.efsa.2024.EN-9084)). MegaDetector and DeepFaune are published and open **[links to add]**.

**Pilot.** 8–10 borrowed cameras for 3–4 weeks in October gives a real roe-deer and boar density for one hunting area, compared with the club's last census. That's **self-measured numbers**, which judges reward.

**Demo.** Drop an SD card and get species counts plus a density map in a minute. It's solid rather than spectacular (Demo 7). The upgrade is to show a Galaxy-phone-based camera trap the team built.

**Fatal-flaw check.**
- ⚠️ **Novelty is integration.** Agouti, Wildlife Insights and Trapper already tag photos. Alone, a judge could call it "an LT form on top of open models".
- ⚠️ REM assumptions (random placement, day-range) need discipline. Bait-site photos are presence-only.
- ⚠️ "Is this sustainability?" Wildlife management and ASF sit closer to agriculture than to "green".
- ✅ Zero deployment problem: the cameras already exist.

**Scores (standalone).** Col 8 · Adp 6 · Prv 9 · Mea 7 · Nov 5 · Demo 7 · Loc 8 · Jury 6 → **56/80**. **Verdict: MAYBE alone. GO as the census layer of Hybrid H1**, where its weaknesses (novelty, adoption) are covered by ŽalosDronas's strengths.

---

### Quick fair hearing for the other named candidates

| Idea | Pitch | Why not a top gem | Col·Adp·Prv·Mea·Nov·Demo·Loc·Jury | Verdict |
|---|---|---|---|---|
| **ActiveLens** (automated SOFIT in PE) | Pose AI measures every kid's MVPA in PE and at break | A judge pattern-matches it to "phone on a tripod + AI in PE" (banned KneeGuard pattern; SkillFit already won Europe). Filming minors. Video-MVPA validity uncited. "Measuring doesn't make kids move" | 8·6·6·8·5·8·7·7 = 55 | MAYBE: the best *pure sport* option, but don't lead with it |
| **Geltonas algoritmas** (school-bus VRP) | Redraw yellow-bus routes when schools consolidate | Proven (Boston −$5M) and measurable, but no hardware, no nature, no wow; it's OR, not ML (weak AI bonus) | 9·7·9·9·7·5·8·5 = 59 | MAYBE (solid, not the team's taste) |
| **CanopyZero** | NRL "no net loss of urban canopy" baseline + felling watch | A dashboard; Copernicus may publish the baseline; LT news evidence not collected | 8·6·8·7·6·5·5·6 | KILL alone → module of H2 |
| **StreamWarn** | WarnMe (SJWP 2025) for LT small streams | Local flood evidence is weak, and no flood before Nov 6. Its *pattern* is perfect (see §4); its *problem* isn't LT's | 9·6·10·4·7·7·4·6 | KILL |
| **LeakPatrol** | Vehicle thermal camera finds DH pipe leaks | Street-level oblique detection is unproven; snow-melt is visible by eye; drone firms exist | 7·7·5·8·6·7·8·6 | KILL alone → winter module of H4 |
| **GridPulse** | Water heaters shed load when Baltic frequency dips | No legal route to market verified; electrician-in-every-home deployment | 10·3·8·6·8·9·5·7 | KILL |
| **BarštisScan** | Dashboard phone maps hogweed from municipal vehicles | No hogweed to see in Oct–Nov, so no honest pilot | 8·7·7·7·7·5·8·7 | KILL for this timeline → summer module of H4 |
| **PelkėsPulsas** | Sentinel + loggers verify peatland rewetting | Duplicates DrainScope's rewet layer; low wow | 8·6·7·8·6·4·8·6 | MERGE into DrainScope |
| **Vape-back** | Vape return box identifies the brand for EPR billing | No reason for a teen to bother; no deposit exists; vapes-in-schools optics | 6·4·6·7·8·8·7·5 | KILL |

---

## 3. Hybrids and combinations

### H1: "Šernas 360": one hunting club, two legal chores, one AI (ŽalosDronas + Šernų skaitliukas, plus BriedisStop's monitoring data as an optional layer)

**Pitch.** *"LT hunting clubs must count their animals every year and pay farmers for the damage those animals do. Both are fought over with tape measures and snow tracks. Our drone measures the damage and our camera AI counts the animals, so quotas, compensation and ASF control finally use the same honest numbers."*

- **Why the hybrid is stronger than either part:** the **same user has two pains**. Hunting clubs *pay* crop damage (the minister says hunters, not farmers, must compensate, per [LRT](https://www.lrt.lt/naujienos/verslas/4/2950303/ministras-laukiniu-gyvunu-padaryta-zala-turi-kompensuoti-medziotojai-o-ne-zemdirbiai)), so they want fair damage numbers. They also *must* run a census they dislike. One app, one account and one relationship (LMŽD or the municipality) serve both. The causal chain is also judge-friendly: **density → damage → quota → less damage**. A club can show the commission "our density went down after we met our quota, and here is the damage map".
- **Tech sharing:** a species-classification model, a geo-dashboard and the drone. The drone can also do thermal night counts in open fields later (**[unverified cost]**, so optional).
- **Adoption:** the municipal damage commission (the law allows drones since 2025-01-01; Kaunas district is looking for innovative solutions) is the policy customer, and the hunting club is the daily user.
- **Demo:** fly a drone over a printed "maize field" to get the damage € figure, then drop an SD card to get density, then show both on one map.
- **Fatal-flaw check:** ⚠️ two pilots in 6 weeks is a lot, so make ŽalosDronas the lead and the census a 10-camera side pilot with the *same* club. ⚠️ "Is it green?" It's human–wildlife coexistence plus ASF, and the pitch has to name that honestly.
- **Scores:** Col 8 · Adp 8 · Prv 9 · Mea 8 · Nov 7 · Demo 7 · Loc 9 · Jury 7 → **63/80. GO** (as the upgraded form of ŽalosDronas).

### H2: "MedžiųSargas": from salt spreader to dying linden to the NRL (Druskos radaras + street-tree soil sensing + CanopyZero)

**Pitch.** *"Salt from winter streets kills Vilnius's trees, and from 2030 the EU says cities may not lose tree canopy. We measure where the street really freezes, cut the salt there, and prove it with soil sensors under the trees."*

- **Why the hybrid is stronger:** Druskos radaras alone is a road-ops tool. With the tree outcome and the Nature Restoration Law's urban "no net loss of canopy vs 2024" obligation (policy scout L7 **[K: structure confident, % unverified]**), it becomes a **nature** story with a **legal deadline**, which is the team's taste. CanopyZero gets a *reason* (salt is a named cause of canopy loss) instead of being a dashboard.
- **Tech:** the IR surface sensor on vehicles, plus soil EC at trees (Vilnius's own 500 sensors and our €20 probe), plus annual canopy segmentation from orthophotos (optional stretch).
- **Adoption:** one customer, the municipality's green/environment unit together with street maintenance. **Tree activists** give free publicity and a letter.
- **Scores:** Col 8 · Adp 6 · Prv 8 · Mea 8 · Nov 8 · Demo 7 · Loc 9 · Jury 8 → **62/80. GO** (lead with salt + soil; canopy is a roadmap slide).

### H3: "Dviračio radaras": the sport idea hidden in two sustainability ones (OvertakeSense/ArtiMetras bike box + a downward IR thermometer)

**Pitch.** *"Teens stop cycling to school for two reasons: cars pass too close in autumn and paths are icy in winter. One €50 box on their bikes measures both, so the city knows where to build lanes and which paths to clear first."*

- **Hardware sharing (real, not decorative):** the same ESP32 + GPS box already has a side ToF sensor for lateral distance. A €10–15 downward IR thermometer plus a humidity sensor turns it into a **mobile bike-path ice sensor**, which is the Druskos radaras sensor on a bicycle (the mobility scout's killed idea #12, "winter bike-path ice", fits here).
- **Why it's stronger:** it fixes OvertakeSense's biggest weakness (*"teens don't bike in November"*) by making winter a feature rather than a gap. That gives a year-round data product for the municipal cycling unit, with **both themes** (sport: active commuting; sustainability: mode shift and salt).
- **Demo:** a bike on a trainer. A cardboard car passes and the display reads "0.74 m", then an ice-pack tile under the wheel turns "ICE RISK" red.
- **Fatal-flaw check:** ⚠️ the ice mode's pilot data before Nov 6 is only the thermal fingerprint of the bike network (no ice yet). ⚠️ Don't let the second mode dilute the crisp 1 m / 1.5 m legal story. Pitch it as "and in winter the same box…".
- **Scores:** Col 9 · Adp 7 · Prv 8 · Mea 8 · Nov 8 · Demo 9 · Loc 8 · Jury 8 → **65/80. GO** (as the upgraded form of ArtiMetras).

### H4: "Šiukšliavežis-skeneris": the garbage truck as a city sensor (HopperGuard lead + roof pod: winter road-surface/DH-leak thermal, summer hogweed)

**Pitch.** *"A garbage truck visits every street in town every week. We already put a thermal AI eye in its hopper to stop battery fires, so we pointed a second one at the street."*

- **The logic:** HopperGuard's fire-safety value *pays for the box* (the operator's own truck is at risk). Extra modes are then almost free: road-surface temperature (the salt plan), thermal DH-leak candidates in winter, hogweed and illegal-dump detection in summer. This is MIT's City Scanner model ([MIT](https://senseable.mit.edu/cityscanner/)).
- **Fatal-flaw check:** ❌ as a *pitch* it's unfocused, and judges reward one narrow user. ⚠️ LeakPatrol's street-level detection is unproven. ✅ As a **"what's next / scalability" slide** in a HopperGuard pitch, it answers "broader impact, transferable" very well.
- **Scores:** Col 8 · Adp 7 · Prv 6 · Mea 7 · Nov 8 · Demo 8 · Loc 8 · Jury 6 → **58/80. MAYBE**, as a roadmap slide only, never the headline.

### H5: "Aktyvi diena": an active-school-day indicator (SchoolGate + ActiveLens on one edge-AI stack)

**Pitch.** *"How many of our pupils arrive on foot or bike, and how many minutes do they actually move in PE and at break? One privacy-first camera stack gives every school its first honest 'active day' number."*

- **Sharing:** the same on-device YOLO person/pose pipeline serves the gate counter and the gym/yard.
- **Why it might be stronger:** it gives the Higienos institutas "Aktyvi mokykla" network a single school KPI (arrivals + MVPA), and the before/after "school street week" becomes a *health* result rather than a traffic count.
- **Fatal-flaw check:** ❌ it doubles the "cameras on children" GDPR surface. ⚠️ It inherits ActiveLens's "phone + pose AI in PE" pattern-match. ⚠️ It isn't nature, and it isn't the team's taste.
- **Scores:** Col 7 · Adp 6 · Prv 7 · Mea 8 · Nov 6 · Demo 8 · Loc 8 · Jury 6 → **56/80. MAYBE-KILL**, listed only as the best sport-only construction.

---

## 4. Pattern check: which ideas look like past winners?

Winning patterns (from `scout-global.md` Part A): **(1)** a narrow named user · **(2)** a physical prototype on the table · **(3)** self-measured numbers before the pitch · **(4)** cheap or reused parts ("10× cheaper than pro") · **(5)** deployment already underway (a partner letter or pilot). The closest analogue is **WarnMe (SJWP 2025)**: a cheap sensor under a bridge, a real network, scaling with partners.

✅ = strong, ~ = partial, ✗ = weak.

| Idea | 1 Named user | 2 Physical prototype | 3 Own numbers by Nov 6 | 4 Cheap/reused | 5 Deployment started | Pattern fit |
|---|---|---|---|---|---|---|
| **HopperGuard** | ✅ waste operator/driver | ✅ mini hopper + thermal | ✅ batteries-per-kg audit + model accuracy | ✅ €150 vs €100k X-ray | ~ needs operator letter | **5/5−** |
| **ArtiMetras / H3** | ✅ municipal cycling unit + teen riders | ✅ bike box | ✅ hundreds of real overtakes | ✅ €40–50 (OpenBikeSensor-class) | ~ school riders = deployment | **5/5−** |
| **BriedisStop** | ✅ Via Lietuva | ✅ thermal unit + mini sign | ✅ forest detections vs trail camera | ~ €300–600; ⚠️ see note | ~ needs Via Lietuva letter | **4.5/5** |
| **ŽalosDronas / H1** | ✅ municipal damage commission + hunting club | ✅ drone (bought, not built) | ✅ 3–5 real damaged plots | ✅ consumer drone vs commission walk | ✅ law already allows drones; Kaunas district asking | **4.5/5** |
| **HeatTwin** | ✅ building maintainer | ✅ mini-block model | ✅ own flats, October | ✅ €10 sensors vs Leanheat | ~ maintainer letter | **4.5/5** |
| **MedžiųSargas / H2** | ✅ municipal green/street unit | ✅ sensor on car + tile demo | ✅ soil EC + thermal fingerprint | ✅ €15 vs €1k+ pro sensors | ~ tree activists / city | **4.5/5** |
| **FishPass** | ✅ AAA + monitoring contractor | ✅ underwater camera box | ~ only with access | ✅ vs Riverwatcher | ~ access letter needed | **4/5** |
| **SchoolGate** | ✅ school + municipality | ✅ window box | ✅ own school, 4 weeks | ✅ old phone / Pi | ✅ own school = deployed | **4.5/5**, but the weakest collapse test |
| **DrainScope** | ✅ melioration specialist (Radviliškis asked on GovTech) | ✗ a map (a logger is a bolt-on) | ✅ field-verified flags | ✅ free satellite data | ✅ published GovTech challenge | **4/5**: missing the object on the table |
| **ManureWatch** | ✅ AAD | ✗ map only | ~ 40–60 fields verified | ✅ free satellite data | ✗ enforcement agency, slow | **3/5** |
| **ChimneyWatch** | ~ municipality/AAD | ✅ rooftop camera | ✅ 3 evenings | ✅ | ✗ politically toxic (ethics) | **3/5** |
| **Šernų skaitliukas** | ✅ hunting club | ~ SD-card app | ✅ 3–4 weeks of cameras | ✅ reuses hunters' cameras | ~ | **4/5** |
| ActiveLens | ✅ PE teacher / VSB | ~ phone on tripod | ✅ own gym | ✅ | ✅ own school | 4/5, killed by pattern-match to banned ideas |
| StreamWarn | ~ seniūnija | ✅ | ✗ no flood | ✅ | ✗ | 3/5 (perfect WarnMe form, wrong LT problem) |

**Pattern winners:** **HopperGuard** and **ArtiMetras/H3** match all five patterns most cleanly. **BriedisStop, ŽalosDronas/H1, HeatTwin and MedžiųSargas/H2** come right behind. **DrainScope** has the best policy hook of all (a published GovTech challenge) but lacks pattern 2 (no object on the table). Its fix is the scouts' LoRa water-level stake plus drone photos of the actual flooded field.

⚠️ **A hardware warning for BriedisStop** (not a re-evaluation, just a spec check the team should do): an MLX90640 (32×24 px, ~55° FOV) gives roughly 3 m per pixel at 100 m, so a moose is about 1 pixel. Real detection range with that sensor is probably ~20–30 m **[my estimate; verify]**. The 50–150 m claim needs a Lepton 3.5 (160×120) or a Hikmicro-class module, which raises the unit cost. Budget for this early.

---

## 5. The team's taste: overall top 7 (front-runners + gems + hybrids)

Weighting: team taste (nature ≥ other · measurable · realistic deployment · proven tech · non-obvious · hardware demo wow) together with the official criteria (usable tech, novelty, realism, local relevance, broader impact/policy, reach the audience, AI/IoT bonus). Front-runners are ranked on the scouts' evidence and my judgement, **without deep re-evaluation**.

| # | Idea (best form) | Theme | One-line reason |
|---|---|---|---|
| **1** | **BriedisStop** (thermal edge-AI moose/deer warning + crossing monitor for Via Lietuva) | Nature / safety | Hits every point of the team's taste at once: nature, hardware, a "warm moose walks in, sign lights up" demo, a single realistic deployer, proven RADS abroad and hard LT numbers (342 → 1,000 collisions, >€5M). Watch the thermal-resolution cost and whether Via Lietuva already runs detection on Vilnius–Utena. |
| **2** | **HopperGuard** (+ H4 roadmap slide) | Waste / safety | The cleanest collapse test in the whole pool (nobody can see inside a compacting hopper), fires tripling, a proven 2025 US award case and the best pattern fit. It loses first place only because it isn't "nature". |
| **3** | **ŽalosDronas as H1 "Šernas 360"** | Nature / agri | The law already allows drones and a municipality is asking. Adding the census gives the hunting club two chores solved by one tool, which is the strongest adoption loop in the nature set. Its "green" framing is the weak spot. |
| **4** | **ArtiMetras/OvertakeSense as H3 "Dviračio radaras"** | Sport + sustainability | The best demo in the pool ("0.74 m"), self-measured LT data by Nov 6, and a live legal debate (Sept 2026 exception). The winter-ice mode removes the "nobody bikes in November" objection. The obvious pick if the team goes sport. |
| **5** | **MedžiųSargas (Druskos radaras as H2)** | Nature in the city | The overlooked gem: an emotive local story (trees dying, a protest), cheap proven physics, real October data (soil salt + thermal fingerprint) and an NRL canopy hook. It's held back by the need for winter for the headline number and the "city already cut salt" objection. |
| **6** | **DrainScope / Fix-or-Rewet** | Nature / climate / agri | The strongest policy hook of anything (Radviliškis GovTech challenge, NRL peat, a 10× gap in the official data) and not saturated. It ranks lower on this team's taste only because the demo is a map. Adding a logger stake and drone footage would move it up. |
| **7** | **HeatTwin** | Energy | The most proven (Leanheat, 100k+ flats), with the clearest € number and legal payer, plus real flat data in October. It isn't nature and is less "non-obvious", but it's the safest realism score in the pool. |
| wildcard | **FishPass Counter** | Nature / rivers | Pure team taste (a live-fish demo, rivers, NRL barriers). Promote it into the top 7, replacing HeatTwin, *only* if a fish-pass access letter or archived video is secured by ~Oct 10. |

**Dropped from the top 7, and why (one line each):** **SchoolGate**, a Telraam copy with the weakest collapse test ("humans can count cars") and not the team's taste. **ManureWatch**, a map-only demo, winter clouds over the ban period and an enforcement image. **ChimneyWatch**, the same neighbour-surveillance ethics that killed round 2's smoke fingerprint. **ActiveLens**, pattern-matched to the banned KneeGuard / "phone on tripod" category.

### My bottom line

If the team wants **nature + hardware + wow**, the decision is **BriedisStop vs ŽalosDronas-H1 vs MedžiųSargas-H2**, all nature, all with October pilot data. If it wants the **safest win on the judging criteria**, it's **HopperGuard**. If it wants **sport**, it's **ArtiMetras as H3** and nothing else.

---

## 6. Must-verify list (from this report only)

1. Vilnius salt tonnage scope and years. Who salts Vilnius streets and how they're paid (municipal company vs per-tonne contractor).
2. That cheap IR surface thermometers track asphalt temperature well enough (emissivity, speed). Validate against a contact probe on the first night drive.
3. LT fish-pass list, which ones use video today, and the typical October salmonid counts per pass. Who to ask: AAA / Gamtos tyrimų centras.
4. MegaDetector/DeepFaune citations; whether the ministry would accept camera-based census (ask LMŽD).
5. The NRL Art. 8 urban canopy wording and LT's national restoration plan content.
6. The BriedisStop thermal module choice vs detection range (see §4 warning).
