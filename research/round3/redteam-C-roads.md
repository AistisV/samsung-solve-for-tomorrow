# Red-team C: road ideas (BriedisStop · OvertakeSense · SchoolGate)

Evaluator stance: hostile but fair. Sources are tagged in three ways:
- **[S]**: verified in a scout file (the scout's own cited link). Many scout figures come from search snippets, not opened pages.
- **[K]**: my own domain knowledge (road ecology, sensors, computer vision). I believe it is correct, but it was not re-checked in this session.
- **[U]**: unverified. It is a guess or a claim that must be checked before stage 1.

No web searches were run for this report. The search budget was exhausted, and the scout files were the evidence base.

---

## TL;DR

| Idea | Verdict | One-line reason |
|---|---|---|
| **BriedisStop** | **MAYBE, leaning GO** (the one I'd bet on, with 3 conditions) | Highest jury ceiling: a visceral LT problem, one obvious deployer, AI+IoT and a great demo. The risks are the thermal optics, getting real pilot data, and a theme fit that has to be *argued* (biodiversity) rather than assumed. |
| **OvertakeSense / ArtiMetras** | **MAYBE** (safe fallback) | The tech is proven, the collapse test is strong, a live law debate gives it a policy hook, and the pilot data is guaranteed. But the novelty is "OpenBikeSensor in Lithuania", and it drifts towards "sensor, map… and then what?". |
| **SchoolGate** | **KILL** | Telraam already does the counting, and YOLO car-counting is the most common student CV demo there is. "Idling" can't be seen by a camera, and "near-misses" from a window are noisy research-grade work. A teacher with a clicker nearly passes the collapse test. The privacy fight with parents comes built in. |

---

## 1. BriedisStop: thermal edge-AI "animal on the road" warning plus a crossing log

### Evidence recap
- **[S]** Police-registered wildlife–vehicle collisions went from 342 (2017) to 1,000 (2025), with a record 119 in Dec 2025. Insured damage is over €5M. Roe deer are 53% of cases. Moose cause about two-thirds of the deaths (PubMed 38791668). Via Lietuva is adding about 90 km of fences in 2026 and already uses variable message signs (VMS).
- **[S]** Proven abroad: Roadside Animal Detection Systems (RADS) in Florida, the Swedish animal-detection driver-warning system (ADDWS) evaluation, and a 2025 *Sensors* paper on thermal + YOLOv8n roadside detection.
- **[K]** Huijser et al. (US FHWA reviews, 2006–2009) surveyed about 30–35 animal-detection systems in North America and Europe. Where a system worked and was maintained, reported collision reductions were large (often cited as 33–97%, 80%+ at several sites). But many systems were unreliable, with outages and false alarms. Driver speed reductions were usually **modest (a few km/h)**. They were bigger at night, on low-visibility roads, and when paired with an advisory or variable speed limit.
- **[K]** Swedish and Finnish trials (Trafikverket and others) found similar results. Speeds dropped several km/h when the warning was on. The effect was stronger when the sign also lowered the limit (e.g. 90→70 km/h).
- **[K]** Car makers ship thermal night vision with animal detection (BMW, Audi, Volvo's large-animal detection, Veoneer/Autoliv). A juror may say "cars already do this". The answer: only on a small share of expensive cars, while roadside units protect every car.

### (a) Skeptical Samsung SfT juror
- **First reaction:** "A moose through the windscreen: I get it in 3 seconds." It is emotional, local and visual, with a clear number. AI and IoT are both genuinely at the core. **Top 5 nationally: likely, if the demo works and there is any real field data.**
- **Doubts they will voice:**
  - "Is this *sustainability*? It sounds like road safety." This is the biggest non-technical risk.
  - "Doesn't Via Lietuva / Estonia / Sweden already have this?"
  - "Can 15-year-olds really detect a moose at 100 m with a €50 sensor?"
- **Baltic final:** strong. Moose and deer collisions are a pan-Baltic and Nordic problem (Estonia and Latvia have the same animals and roads **[K]**), so the "transferable" criterion is easy to meet. English pitch: "The only sign drivers believe is one that's only on when a moose is there."
- **Credibility from students:** high if they show a real thermal clip of a real roe deer from their own pilot. Low if the demo is only a person on all fours.

### (b) End user: Via Lietuva road-safety / environment engineer
- **Their first 30 seconds:**
  - "We already have fences, green bridges and VMS. Detection systems abroad have reliability problems. Who maintains your box in January at -20 °C with snow on the lens?"
  - "Anything that drives a sign on a state road has to meet road-equipment standards and go through public procurement. We don't buy from a school."
  - "But the fence-end and underpass monitoring is interesting. Today we pay ecologists to go through camera-trap photos."
- **What they already use:**
  - **[S]** Fences, green bridges, underpasses, amphibian systems and VMS.
  - **[S]** The Vilnius–Utena reconstruction article mentions "modern solutions". **[U]** It is unknown whether an active detection system already exists anywhere in LT. **This is the #1 fact to check.** If one exists, novelty shifts to "10× cheaper, species-aware, plus monitoring", which is still a valid pitch, but it must be stated honestly.
  - **[K]** Post-construction monitoring of wildlife passages (camera traps, track beds) is normally contracted to scientists. In LT that likely means the Nature Research Centre (Gamtos tyrimų centras) team that wrote the collision papers **[U]**.
- **Would they pay?** They won't pay for the sign unit soon, since procurement and liability stand in the way. They *might* engage on **monitoring**: "tell us how many animals use underpass X and how many walk around fence end Y". A letter of interest for a pilot is plausible, and a purchase is not.

### (c) Domain engineer
- **Thermal optics are the hidden fatal flaw of the "cheap" version [K].**
  - **MLX90640** (32×24 px) is useless beyond about 10–15 m.
  - **FLIR Lepton 3.5** has 160×120 px over a ~57° field of view, which is about 6 mrad per pixel. At 100 m, one pixel covers about 0.6 m, so a moose is about 3×3 px and a roe deer about 2×1 px. That is detection at best and not species ID.
  - By the Johnson criteria (about 6+ px across the target for recognition), a Lepton classifies a deer out to roughly **20–35 m**, not 50–150 m.
  - A 256×192 core (InfiRay P2 Pro / HIKMICRO class, about €250–400 **[U price]**) roughly doubles that. A 384×288 core with a narrower lens gets to about 100 m but costs €600–1,500+ **[U]**.
  - **Fix:** fence ends are *short-range, known-geometry* sites. The animal comes around the fence end within 10–40 m of the camera, so a 256-px wide-angle core works there. Pitch the fence end, not "watch 150 m of highway".
- **Weather [K]:**
  - Long-wave infrared (LWIR) sees through darkness and smoke and does better than visible light in light haze.
  - Heavy fog, heavy rain and wet snow attenuate it and lower the contrast.
  - Wet fur and snow crust on the animal cut the temperature difference.
  - Snow or ice on the lens window causes total outages (the scout already notes a documented US outage of about 40% in a snowstorm).
  - In daytime summer, sun-heated asphalt and rocks produce false positives. Collisions peak at dusk, night and dawn in autumn and winter, which is exactly when thermal contrast is best. That's a good match.
- **False alarms:** people, dogs, cars' hot engines and tyres. The class list must include "car" and "human", and the unit must ignore targets *on* the carriageway moving at vehicle speed. Tracking plus direction (verge → road) is more important than the classifier.
- **Latency:** detection plus a sign within 1 s is easy. The real issue is sign placement. The sign has to sit far enough upstream (about 150–300 m at 90 km/h) for drivers to react, so the unit needs a radio link or a cable to the sign.
- **Does the sign reduce collisions? [K]** Yes, where the system is reliable and the warning is credible. The effect is mostly *speed plus alertness*, and it is strongest with a temporary speed limit. The honest claim is "reduces risk at the site". A pilot can't claim "saves X lives", because collisions per site are too rare (single digits per year) to show a change in months. **The pilot proxy metrics** are:
  - detection recall and precision against a trail-camera ground truth;
  - crossings per night;
  - (later) the drop in driver speed while the sign is lit, measured with a radar gun or speed logger.
- **Power:** a Pi 5 with a thermal core draws about 6–8 W, which is about 150–190 Wh a day **[K]**. That is not a small solar panel in a Lithuanian November. Fixes:
  - a low-power pipeline (PIR/radar wake-up, or a Pi Zero 2 / ESP32-S3 + Lepton);
  - a mains-powered pilot site.
- **Verdict:** not fatal, but **the €50 "MLX sensor" version is fatal**. The team must budget about €300 for a proper thermal core and design for short range.

### (d) The 16-year-old team, 6 weeks
- **Build:**
  - an InfiRay/HIKMICRO USB thermal core on a Raspberry Pi 5 or an old Android phone;
  - YOLOv8n fine-tuned on public thermal wildlife sets plus their own clips **[U: dataset availability; the Sensors 2025 paper may share data]**;
  - a tracker with "verge → road" direction logic;
  - an ESP32 + LoRa link to an LED "BRIEDIS" sign;
  - a web dashboard.
- **Hardest part:** getting real animal footage fast. Roe deer are abundant at LT forest/field edges at dusk **[K]**, so this is doable at a **farmstead with mains power** overlooking a field edge. They also need about 2–3 weeks of clips for fine-tuning and an honest precision/recall table.
- **Real pilot data by Nov 6?** Yes for detection logs (roe deer, fox, boar, maybe moose), if hardware is in hand by about Oct 5. No for a roadside sign, which needs no legal permission only if it isn't on a road, and no for any collision effect.
- **Stage demo:**
  - a live thermal feed of the audience;
  - a hot-water-bottle "deer" on a toy road, or a team member;
  - the box flashes the mini sign, with a speed-limit drop shown;
  - then a **real clip from their own pilot: a roe deer at night, boxed and labelled**, plus a precision/recall table;
  - the "moose vs roe deer = different urgency" slide.
- **Fun?** Very. Night-time field work, thermal cameras, animals. This is the most "cool" project of the three.

### Fatal flaws
- None that can't be fixed. Two conditional kills:
  1. Via Lietuva already runs an equivalent thermal detection system and the team can't articulate the difference.
  2. The team can't get a ≥256-px thermal core and a powered pilot site by early October.

### Fixable weaknesses and fixes
| Weakness | Fix |
|---|---|
| Theme fit is "road safety" | Pick **Sustainability** and frame it as *biodiversity/coexistence*. Collisions are a major, measurable mortality source for ungulates. The monitoring mode proves whether Via Lietuva's green infrastructure (green bridges, underpasses, fences) actually keeps animals alive and connected, with an EU biodiversity and Nature Restoration hook **[K]**. Lead with animals saved and crossings used, then human safety. |
| Range and price claims | Claim a **fence-end / short-range** use case, a €300–500 BOM, and publish measured range per species. |
| Driver response is mixed | Say it first: "Detection systems work when drivers trust them, so the key metric is false alarms per night." Pair the design with VMS speed reduction (90→70). |
| Adoption blocked by procurement | Stage 1 product = **monitoring**, bought or contracted as a study with an ecology partner. Stage 2 = the warning sign, once the false-alarm rate is proven. That is an evidence ladder, which judges like. |
| Power and weather | Wake-up sensor, lens heater/hood, health heartbeat to the dashboard, and an honest uptime figure. |

### Sharpened version: **"BriedisStop: the fence-end sentinel"**
A thermal edge-AI unit at the *end of a wildlife fence* (where animals funnel around), aimed at the 10–40 m zone. **Mode 1 (now):** it counts and classifies every animal that goes around the fence end or through the adjacent underpass, so Via Lietuva learns which fences leak and which passages work. **Mode 2 (when the false-alarm rate is proven):** it triggers the existing VMS or an LED sign with a temporary 70 km/h limit, but only when a moose/deer is heading towards the road. Pilot: 3 weeks at a field/forest edge with a trail camera as ground truth, giving real LT thermal detections, precision/recall and false alarms per night.

**One-sentence pitch:** "Lithuania now has 1,000 wildlife crashes a year and fences can't go everywhere, so our €400 thermal-AI sentinel watches where fences end, warns drivers only when a moose is really there, and tells Via Lietuva which of its green bridges and fences actually work."

### Scores (1–10)
| Collapse | Adoption loop | Proven tech | Measurable impact | Novelty | Demo wow | Local evidence | Jury appeal | Theme fit |
|---|---|---|---|---|---|---|---|---|
| 9 | 6 | 8 | 6 | 7 | 9 | 9 | 9 | 6 |

**VERDICT: MAYBE → GO if** (1) no equivalent Via Lietuva system is found (or the difference is sharp), (2) a thermal core ≥256 px is ordered this week, and (3) a powered field-edge pilot site is secured.

---

## 2. OvertakeSense / ArtiMetras: close-pass measurement for cyclists

### Evidence recap
- **[S]** LT road traffic rules (KET) since Dec 2024: 1 m at ≤50 km/h, 1.5 m above. In Sept 2026 an exception is being debated (the content of the exception is **[U]**, since the page was blocked).
- **[S]** Cyclists injured Jan–May 2026: 103 injured and 3 killed, vs 94 and 1 in 2025. Vilnius targets 7.5–10% cycling mode share by 2030.
- **[S]** OpenBikeSensor: an Austrian study of 11,399 overtakes found about 40% compliance in cities and about 19% in rural areas (Sensors 2026). SenseBike and a before/after advisory-lane study also exist.
- **[K]** UK police "Operation Close Pass" (West Midlands, from 2016) made close passing a public enforcement and education topic. Commercial devices exist too: C3FT (a US close-pass measurement device used by some police) and Garmin Varia (rear radar that warns the rider). **[U]** Whether OpenBikeSensor or anything similar is used in LT.

### (a) Skeptical juror
- **First reaction:** "Clear, measurable, a live law, teens riding. Nice." The heatmap and "X% broke the law" are headline material.
- **Doubts:**
  - "This is OpenBikeSensor with a new logo."
  - "Ten teens' commutes aren't representative."
  - "What happens after the map?"
- **Top 5:** plausible. It is solid, but it may read as a competent science-fair measurement project rather than a solution. **Baltic final:** transferable, but weaker on the "solution" axis. Another juror might say "just build bike lanes".
- **Theme:** Sport & tech (active living: safe enough to cycle to school) is the cleaner fit. Sustainability (mode shift) is secondary. Pick sport.

### (b) End user: municipal mobility department (Vilnius JUDU / Susisiekimo paslaugos / Kaunas) and TKA
- **First 30 seconds:**
  - "We know where we lack bike lanes. Our constraints are money, space and politics, not data."
  - "Interesting for the ministry's rule debate, though."
  - "Can police use it for fines?" (No: it isn't a certified measuring instrument.)
- **What they use:** traffic counters, crash data from the police/LAKD, surveys, Strava Metro-type data **[K; LT usage U]**. There is no close-pass data **[S, unverified]**.
- **Would they pay?** They are unlikely to buy boxes. More plausibly, TKA or a cycling NGO co-signs a **one-off study**, or the ministry cites the data in the exception debate. The adoption loop is "campaign-shaped", not product-shaped. That is the WellWatch 2.0 trap ("sensor… then what?") in softer form.
- **The real hook:** before/after evaluation. When the city paints a lane, sets 30 km/h or builds a separator on street X, ArtiMetras measures whether passes got wider. Cities do buy evaluations.

### (c) Domain engineer
- **Sensor choice matters [K]:**
  - **VL53L1X-class ToF fails in sunlight.** Its range collapses outdoors to about 1–1.3 m, which is exactly the threshold being measured. Don't use it.
  - Ultrasonic (JSN-SR04T / MaxBotix, which OBS uses) works but has a wide beam, is slow in cold air, and has temperature-dependent speed of sound (compensate for it).
  - **Small single-point lidar (TF-Mini Plus / TF-Luna, about €20–40)** is sunlight-tolerant and runs at 100+ Hz. It is the best choice.
  - Accuracy of ±5–10 cm is achievable after subtracting the handlebar-to-sensor offset. Validate on a tape-marked lane.
- **Event detection:** parked cars, poles, hedges and cyclists in the next lane all look like "an object at 0.8 m". OBS historically relied on the **rider pressing a button** to confirm an overtake **[K]**. A rear-facing phone camera running YOLO + tracking that sees the vehicle *approach and pass* can auto-confirm overtakes. That is a genuine, demonstrable improvement, and it removes the human from the loop.
- **Which rule applies (1 m vs 1.5 m)** depends on the vehicle speed. Estimate it from the rear camera (bounding-box growth rate plus rider speed from GPS), or use the posted limit as a proxy.
- **Data volume:** in Vilnius, teens often ride on bike paths or sidewalks where there are *no* overtakes **[K]**. Expect far fewer events than "1,000". Plan routes with road-riding segments, and recruit adult commuters and cycling clubs.
- **Nothing fatal.** The science is solid and published.

### (d) Team, 6 weeks
- **Build:**
  - ESP32 + TF-Mini lidar + GPS + button fallback in a 3D-printed box;
  - an old Android phone as the rear camera with on-device YOLO (TFLite);
  - a BLE sync app and a map dashboard with per-segment stats.
- **Hardest part:** robust overtake segmentation (fusing camera and distance) and getting enough overtakes in wet, dark October. Rider safety and parental consent come with it.
- **Real data by Nov 6:** yes, almost guaranteed, if 3–5 boxes ride from about Oct 10. That's a few hundred passes.
- **Demo:** bike on a trainer, a cardboard car on a trolley, red/green beeps. The **real wow is the ride video with a live overlay: "0.74 m, 46 km/h, ILLEGAL"**, plus their city's map.
- **Fun?** Yes. It's sporty and outdoors, with a moderate cool factor.

### Fatal flaws
- None technical. **The strategic near-fatal flaw:** novelty is low (it is openly OBS) and the loop ends in "a map". Against demanding judges who rejected "sensor… then what?", this is exposed.

### Fixable weaknesses and fixes
| Weakness | Fix |
|---|---|
| "It's OpenBikeSensor" | Make AI the contribution. The camera auto-detects overtakes (no button), classifies bus/truck/car, and estimates overtaking speed so the correct 1 m / 1.5 m rule is applied. Publish the LT dataset openly. |
| "Then what?" | Tie it to a **decision**: (1) data for the Ministry of Transport's Sept 2026 exception debate (deadline-driven); (2) a before/after measurement on one street the city is changing in 2026. Get a TKA or cycling-community letter. |
| Few overtakes | Recruit adult commuters and a cycling club. Target road segments. |
| Theme ambiguity | Pick Sport & tech: "parents allow cycling to school when the roads are proven safe". |

### Sharpened version: **"ArtiMetras: evidence for the 1 m law"**
An auto-detecting close-pass box (lidar plus a rear phone camera with AI) that measures every overtake, applies the correct legal threshold using the estimated car speed, and produces the **first Lithuanian compliance figure**, delivered to the ministry during the exception debate and to the city as a before/after tool for new bike infrastructure.

**One-sentence pitch:** "Lithuania just made 1 m the law for passing cyclists, and nobody knows whether drivers obey it, so our AI bike box measured N overtakes on our streets, found X% were illegal, and showed the city exactly which streets keep kids off their bikes."

### Scores (1–10)
| Collapse | Adoption loop | Proven tech | Measurable impact | Novelty | Demo wow | Local evidence | Jury appeal | Theme fit |
|---|---|---|---|---|---|---|---|---|
| 9 | 5 | 9 | 7 | 5 | 7 | 7 | 7 | 7 |

**VERDICT: MAYBE** (the safest executable fallback, but a lower ceiling).

---

## 3. SchoolGate: window counter for school drop-offs

### Evidence recap
- **[S]** Kids driven to school up 200% over 30 years, and 182 children injured within 100 m of schools in 2022–25 (Vilnius / 15min).
- **[S; K]** Telraam (BE, Raspberry Pi window counter, used across Europe) and the WeCount EU project already do citizen window counting of cars, bikes, pedestrians and heavy vehicles, including speed. Vivacity (UK) and others sell near-miss analytics commercially.
- **[U]** Whether Vilnius or Kaunas run School Street pilots.

### (a) Skeptical juror
- **First reaction:** "A camera counting cars with YOLO. I've seen this." Object counting is the most common student computer-vision project **[K]**. The local problem is real and relatable, but the tech looks generic.
- **Top 5:** possible on sheer completeness (they *will* have real data), but it is unlikely to stand out. Baltic final: weak on novelty.
- **Theme:** it straddles both themes and has to choose one. Either way it feels like mobility/safety, not a strong fit for either.

### (b) End user: school director, parents, municipality
- **Director's 30 seconds:** "A camera filming our pupils? I need the data protection officer, the parents' council and probably the municipality to sign off. We already have CCTV at the gate. Why can't the duty teacher just count cars for a week?"
- **Parents:** half will support a School Street, and the half who drive will be hostile to being "counted". Politically messy.
- **Municipality:** a School Street is a traffic-management decision. They need a *justification* once, not continuous counting. A one-week manual count by staff or a contractor is the standard tool **[K]**.
- **Pays?** Barely. A €60 box is cheap enough, but nobody has a budget line or a strong need for it.

### (c) Domain engineer
- **Counting:** easy and proven (Telraam-grade). No issue.
- **"Idling": not observable by camera [K].** A stationary car looks the same with the engine on or off. Converting "stationary time" into CO₂ is an assumption presented as a measurement. A juror or engineer will catch it. **Drop it.**
- **"Child–car near-misses":** surrogate safety measures (time-to-collision, post-encroachment time, the Swedish Traffic Conflict Technique) are real science. But doing them from a single oblique window camera needs ground-plane calibration (homography), handles occlusion by parked cars badly, and tracks small children poorly. True conflicts are rare while false ones are frequent. It is a research project in itself, and students would present noisy numbers as findings. That is exactly the "hopefully the science works" pattern the team rejects.
- **Collapse test:** only partly passes. A human counts a morning just fine. The "continuous plus before/after" argument is real but weak for a single school.
- **CO₂ impact:** the trips are short, so the effect is small in tonnes. Removing 100 drop-offs a day of about 2 km each is roughly 5–7 t CO₂ a year per school **[K, rough estimate]**. Honest, but not impressive.

### (d) Team, 6 weeks
- **Build:** a phone or Pi with YOLO + ByteTrack, zone logic and a dashboard. It is technically easy, which is the problem: little to be proud of beyond the pilot.
- **Real data:** yes, the easiest of the three, if the school approves the camera. The approval may take longer than the build.
- **Demo:** a live count of the audience or toy cars. Pleasant, but it doesn't wow.
- **Fun?** Low to medium.

### Fatal flaws
1. **Saturation plus prior art:** Telraam does it, and car counting is ubiquitous. That fails hard criterion 5.
2. **The collapse test is borderline** for the parts that work (counting). The parts that would pass it (idling, near-misses) either don't work (idling) or are research-grade (near-misses).
3. The privacy and politics of filming children at school are a first-30-seconds objection from every stakeholder.

### Could it be rescued?
The only rescue is to fold it into ArtiMetras as a *module*: "the gate counter measures whether the School Street changed mode share". That adds complexity without adding wow. **Don't.**

**Sharpened version (if forced):** "Mokyklos gatvė trial kit": a no-image counter plus a one-week closure protocol that a municipality can run at any school. **Pitch:** "Our €60 box lets any school prove, with a week of data, whether closing its street at 8 am takes cars off the road and puts kids on bikes."

### Scores (1–10)
| Collapse | Adoption loop | Proven tech | Measurable impact | Novelty | Demo wow | Local evidence | Jury appeal | Theme fit |
|---|---|---|---|---|---|---|---|---|
| 4 | 5 | 9 | 6 | 3 | 4 | 8 | 4 | 5 |

**VERDICT: KILL.**

---

## Final call

**Bet on BriedisStop, reframed as the "fence-end sentinel" (monitoring first, warning second), entered under Sustainability with a biodiversity framing.** It has the strongest story, a single realistic deployer, both bonus technologies, and a stage demo nobody else will have. It is Baltic-transferable (moose and deer everywhere).

**Before committing (this week):**
1. Confirm whether Via Lietuva (or Estonia's Transport Administration) already runs thermal/radar animal *detection*. **[U]**
2. Order a ≥256-px thermal core, not an MLX90640 or a bare Lepton.
3. Secure a mains-powered field/forest-edge pilot site with roe deer traffic.
4. Email Via Lietuva's environment unit and the Nature Research Centre for a letter of interest.

**If any of 1–3 fails, fall back to ArtiMetras** with the AI auto-overtake + speed-aware legal threshold sharpening, aimed at the 2026 exception debate.
