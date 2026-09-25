# Red-team B: HopperGuard · HeatTwin · ChimneyWatch (+ HeatLeak / 50-50 Watts)

> Evaluator role: hostile but fair. Sources: `BRIEF.md`, `scout-waste-circular.md`, `scout-energy.md`, `scout-policy.md`, `scout-global.md`, `../past-winners.md`.
> **No new web research was done** because the WebSearch budget was exhausted. Every claim has one of three tags:
> - **[S]**: verified in a scout file (the scout found a source for it)
> - **[K]**: evaluator's own domain knowledge, reliable enough to reason with but not checked this round
> - **[U]**: unverified or a guess, to be checked before the Oct 16 form

---

## TL;DR

| Idea | Verdict | Why, in one line |
|---|---|---|
| **HopperGuard** | **GO (conditional)** | The problem is visceral and in the news, the thermal alarm is proven (Goodyear) and the payer is clear. But the RGB "battery source map" is the weak half: most batteries are inside bags and devices. Make the idea thermal-first and treat the map as a hot-event map. The condition: an operator gives a ride-along or footage by ~Oct 20. |
| **HeatTwin** | **MAYBE (lean no for the jury)** | Strongest proven tech and the best real pilot data, but three problems: the "AI" is marginal (a maintainer with 8 loggers and a weekly curve tweak gets most of the benefit), incentives are split in m²-billed blocks, and the demo is a dashboard of slow temperatures. |
| **ChimneyWatch** | **KILL** | Camera opacity (ASTM D7520) needs daylight, a sky background and sun geometry. LT heating-season burning happens in the dark, under grey skies, in winters where condensing gas boilers make big white plumes. On top of that, a school camera filming neighbours' houses repeats the ethics problem that got the round-2 "smoke fingerprint" killed. |
| HeatLeak / 50-50 Watts | **MAYBE-low (fallback only)** | The easiest pilot and the cleanest money loop (50/50). But the collapse test is weak (tado-style window detection, a caretaker walk-round) and classroom sensor boxes are a student-contest cliché. It is best used as the *deployment venue* for HeatTwin, not as a separate idea. |

**Bet:** HopperGuard, sharpened as below. It is the only one of the three where a 15-year-old can open the pitch with a video of a burning garbage truck in Vilnius, the core tech is proven, and the collapse test is unarguable (nobody sees inside a compacting hopper).

---

## 1. HopperGuard: a thermal + AI camera over the garbage-truck hopper

### Facts the idea rests on
- LT battery-related fires: 12 → 21 → 33 (2023–25, PAGD). **This counts all battery fires, e-scooters included, not only waste fires.** [S]
- At least 5 waste-company fires in 3 months of 2025: Energesman (~7,500 m²), the Kaunas CHP fuel bunker (8 May 2025, lithium suspected) and a battery warehouse in Paneriai. Ecoservice truck fires in Vilnius. [S]
- The EU Battery Regulation requires 63% collection of portable batteries by end-2027 (45% today). [S]
- Goodyear (Arizona) thermal cameras on trash trucks, alarm at >200°F, 2025 safety award. [S] The exact camera placement (hopper only, or body as well) and the results (how many fires were caught) are **[U]**, so get them before the pitch.
- Plant-side AI battery detection uses **X-ray**, not visible light (Visia, PFU/Ricoh, LINEV). [S] That matters (see (c)).

### (a) Skeptical SfT jury member
- **Exciting?** Yes. Fire, explosions, news footage and a clear villain (the vape in the bin). It is the most "Samsung-video-friendly" problem of the three.
- **Clear?** Mostly. "A camera that sees the fire before it happens" lands in 5 seconds. The dual-purpose part ("…and it also maps where batteries come from") blurs it. Judges remember one thing.
- **Novel?** Moderate. The honest framing is "Goodyear did it in Arizona; we make it cheap, add AI and adapt it to LT shared container sites." Judges respect that, but will ask what *you* invented. The source map is the novel part, and it is also the weakest part (see (c)).
- **Credible from 15-year-olds?** Yes, as long as they never pretend to have tested with a real battery in thermal runaway. Saying "we tested on the bench with a resistor, for safety" is credible and responsible.
- **National TOP 5?** Likely, if they get even one operator letter or one real hopper video. The combination of the news hook, the policy hook (the 63% target) and AI+IoT is strong among ~70 teams, most of which will be apps.
- **Baltic final?** Competitive. The problem is pan-European (UK, US and DE all report rising battery truck fires [K]), so it passes "transferable to other communities" easily. The risk is a judge who knows the industry saying "thermal fire detection on waste is a mature product category". In waste bunkers it is (e.g. Orglmeister, Pyrosmart-type bunker monitoring [K]). The team must say clearly "plants have it; trucks don't".

### (b) End user: fleet manager at a waste operator (Ecoservice / a municipal company)
**First 30 seconds, realistically:** "Truck fires, yes, we've had them. The drivers smell it or see smoke and dump the load. How much does it cost? Does it survive the pressure washer, -25°C, and the lift arm hitting it? Who looks at the alarms? My drivers already ignore the reversing beeper."

- **What they already use [K]:** reversing and 360° cameras, GPS/telematics (route and lift counts), RFID bin identification on some contracts [U for LT], engine-bay fire suppression (Fogmaker/Dafo-type), and a fire extinguisher. Nothing looks into the hopper or body thermally [U for LT, but likely true].
- **Would they pay?** A garbage truck costs roughly €200–300k [K]. One total loss pays for a fleet-wide retrofit at €300–800 per truck. **But** in any given fleet a truck fire is rare, a few per year nationally at most [U; the scout has anecdotes, not a count]. Fleet managers buy against rare events only when an insurer or a regulation pushes. **Insurer discount = the real adoption lever.** The scout does not mention it, and it should be in the pitch.
- **What they'd actually value more:** hard evidence to take to the municipality and the EPR organisation: "your residents put X batteries a month in our trucks; you pay for collection boxes." That is the map, but only if it's credible.
- **The "who looks at alarms" problem:** the alarm must go to the driver (cab buzzer) and to dispatch (SMS/Telegram). The driver needs a procedure: stop, don't compact, call 112 or hot-dump at a safe spot. **Whether hot-dumping on public roads is allowed or practised in LT is [U]**. Ask the operator and PAGD. A PAGD quote ("we would rather get the call 10 minutes earlier") would be gold.

### (c) Domain engineer
**Thermal runaway physics [K]:**
- A cell crushed or punctured by the packer blade can reach venting (~150–200°C) in **seconds to a few minutes**. Many damaged cells instead **smoulder or ignite with a delay of minutes to hours**. So a large share of truck fires start *inside the body*, after the waste has left the hopper, or later on the tipping floor.
- **A hopper-only camera watches a ~20–40 s window per compaction cycle.** It catches the fast crush-to-flame events, which are the dramatic "explosion in the hopper" cases in the Vilnius news, but it misses delayed ignition deep in the load.
- **Fix:** add a second, cheap sensor in the body headspace: a thermal array at the top of the tailgate looking forward over the load, or simple thermocouple + CO/H₂ gas sensors in the headspace. Electrolyte vent gas (and later CO) *precedes* flame. Off-gas detection is the principle behind Li-ion Tamer-type products [K; the scout lists it as U]. A body that is 90% full leaves little headspace, so the reading is imperfect, but it covers the "burning while driving" case.

**Surface vs buried:**
- Thermal IR sees surfaces only. A battery under 20 cm of wet paper and food is invisible until heat or flame reaches the surface.
- Fast-developing fires do reach the surface quickly, so detection is still earlier than a driver's nose, but "we see it before it's a fire" overstates the case.
- **Honest claim:** "we see it at the first visible hot spot, minutes before the driver would, while the fire is still small and still in the hopper."

**False positives [K]:**
- Summer sun on black plastic gives ~60–70°C surfaces. A threshold around 90–100°C plus a rate-of-rise check handles that (Goodyear uses >93°C [S]).
- **Hot stove ash in winter.** In LT private-house and mixed areas, people dump ash into containers. The camera will fire on it. **Spin this as a feature:** hot ash is itself a classic container and truck fire cause [K].
- Engine exhaust and hydraulic oil are out of the field of view if the camera is mounted correctly.

**Environment:** water jets, freezing slush and vibration. A MLX90640 sensor behind a germanium or HDPE window gets dirty. That is solvable in the product version with an IP67 automotive-camera housing, and irrelevant for the prototype.

**RGB source map is the weak half. It is not fatal to the idea, but close to fatal to the "map" claim:**
- LT **mixed waste is mostly bagged**. Batteries in bags and batteries inside devices (toys, toothbrushes, vapes in a bag) are invisible to an RGB camera. **That is exactly why industry uses X-ray** [S: Visia/PFU are X-ray].
- In the loose **packaging (yellow) stream**, loose vapes and power banks are sometimes visible. Even there, a tip lasts ~2–3 s with motion blur and occlusion, so recall will be low.
- **Statistics:** if a visible battery appears once every N tips (N possibly 50–500 [U]), and each container site is emptied 1–3 times a week, a *site-level* rate needs months of data before it separates from noise. A **district- or route-level** map is statistically realistic within weeks.
- **Verdict:** keep detection, but drop "site-level attribution" as the headline. Rank routes and districts, and let the *thermal events* (rare but unambiguous) carry a site-level pin.

**Truck variety:** LT uses rear loaders for 1,100 L wheeled bins, top-loading crane trucks for underground/semi-underground (Molok-type) containers, and some side loaders [K]. On a crane truck the waste drops into an open top, so the "hopper" camera position differs. **Scope the pilot to rear loaders.**

**Fatal technical flaw?** No. The thermal alarm is proven in the field abroad and physically sound for fast events. The dangerous overclaims are (1) catching buried or delayed fires and (2) a site-accurate RGB source map. Remove those overclaims and the idea holds.

### (d) The 16-year-old team, 6 weeks
**Build:**
- Raspberry Pi 5 (or an old Galaxy phone as the RGB and upload hub)
- MLX90640 (32×24, ~€50–70) or a TOPDON/InfiRay USB thermal core (~€150–250, far nicer images) [K prices]
- USB RGB camera
- GPS module
- Buzzer/LED "cab unit"
- Web dashboard with a map

**Software:** thermal anomaly logic (threshold + rate-of-rise + blob tracking), a YOLO battery/vape detector fine-tuned on BatSort/TACO plus their own photos [S], and a map backend.

**Hardest parts:**
1. Getting **real truck access**. Operators are cautious about minors near compactors, so ask for footage from the operator's own cameras, or a static camera over a container during a collection.
2. Making the RGB detector work on realistic cluttered, bagged waste, not staged photos. **Expect a model that works in the lab and fails on real waste.**

**Real pilot data by Nov 6? Partly.**
- ✅ **Bench latency:** seconds from a hidden 120°C heat source reaching the surface to the alarm, at different burial depths. This is real, honest data that also *shows the limit*: "at 10 cm depth we can't see it; that's why we add the headspace gas sensor."
- ✅ **Battery-count audit** of the packaging stream. **Warning:** teens hand-sorting 50–100 kg of waste raises sharps and hygiene issues, and the yield may be 0–3 batteries (statistically meaningless). **Better:** partner with a sorting plant or RATC and count batteries pulled from the picking line or quarantine bin over 2 weeks (they often log this [U]), or run a school-wide "bring your dead vapes and batteries" count as a proxy.
- ⚠️ **Real hopper footage:** only if an operator agrees in the first 2 weeks. Without it, the key claim is untested on real waste.
- ❌ **Fires prevented:** impossible to measure in a pilot, because the events are too rare. The pitch needs a *modelled* impact instead (national truck fires × catch rate × € per fire) with the assumptions shown.

**Stage demo:** an acrylic mini-hopper and a cab unit.
1. A buried "battery" (resistor pack in an aluminium can, never a real cell) heats up. The thermal view blooms red, the buzzer sounds and a pin drops on the Vilnius map with "Route 14, Žirmūnai".
2. A vape is dropped in, a box appears and the route counter ticks up.

That is a very good demo: physical, loud, visible from the back row. **They'd be proud of it:** it's hardware plus AI plus a real emergency.

### Fatal flaws
None fatal. **The closest:** the "source map" rests on RGB detection that physics (bags, devices, occlusion) largely defeats. If the team leads with the map, a knowledgeable judge takes the idea apart.

### Fixable weaknesses and fixes
| Weakness | Fix |
|---|---|
| Novelty looks like a "Goodyear copy" | Name Goodyear proudly, then show the three LT adaptations: a <€300 open retrofit, a hopper + headspace **two-stage** sensor (thermal + gas), and an alarm routed to driver + dispatch + PAGD with GPS |
| RGB map is statistically weak | Downgrade it to route/district level and to the packaging stream. Make the **thermal-event map** the primary map, since every event is certain |
| Buried and delayed fires missed | Add a headspace gas + thermal sensor. Show the depth-vs-detection curve honestly |
| No fire counts for LT trucks | Ask PAGD for a data request (truck and waste-facility fires by cause, 2020–25). Students often get these answered. A real PAGD table beats any scout citation |
| Payer hesitates over rare events | Bring the **insurer** (truck and CASCO premiums) and the **EPR organisations** (the map serves the 63%-by-2027 target) in as co-payers. Get one quote from an operator: "we lost a truck in 20XX" |
| Safety ethics (teens + batteries) | State the rule on the first slide: never real cells in runaway; the heat source is a resistor. It earns credibility |

### Sharpened version: **"HopperGuard: a two-stage fire early-warning for garbage trucks"**
1. **Stage 1, hopper (thermal + AI):** catches crush-to-flame events at compaction and **hot ash**, with blob tracking to reject sun and steam.
2. **Stage 2, body headspace (gas + thermal, €30 of sensors):** catches delayed off-gassing and smouldering while driving. Lithium cells vent electrolyte vapour before flame.
3. **Output:** a cab alarm with a "don't compact, pull over" instruction, a dispatch SMS with GPS, and a **fire-risk map** of routes where thermal events and visible batteries occur. That map goes to the municipality and EPR organisation, which place collection boxes on those routes (the 63%-by-2027 hook).

The mapping becomes "a second job for the same box", not the headline.

**One-sentence pitch:** *"Lithuania's battery fires tripled in two years, and garbage trucks are where they start. Our €300 box watches the hopper and the load with thermal and gas sensors, warns the driver minutes before a fire, and shows the city which routes to target with battery collection boxes."*

### Scores (1–10)
| Collapse | Adoption loop | Proven tech | Measurable impact | Novelty | Demo wow | Local evidence | Jury appeal |
|---|---|---|---|---|---|---|---|
| 9 | 6 | 7 (thermal 8, RGB-in-bags 3) | 6 (rare events; pilot proxies only) | 6 | 8 | 8 | 8 |

**VERDICT: GO (conditional).** The condition: by ~Oct 20, one operator or RATC agrees to footage or a ride-along **or** PAGD or an operator provides fire data. Without either, the idea stays a well-built lab demo with borrowed evidence, and drops to MAYBE.

---

## 2. HeatTwin: "Leanheat for the Soviet block"

### Facts the idea rests on
- ~38k apartment blocks; 359 renovated in 2025 against a 9,882-by-2030 target. [S]
- Automated substations were mandatory by 1 July 2026. [S]
- Unbalanced systems: "some open windows, others plug in heaters." [S]
- The maintainer is legally obliged to keep operation economical and to give annual saving recommendations. [S]
- Many old blocks split heat by m². [S]
- Danfoss Leanheat: 100k+ apartments. Espoo: −6% energy, −17% peak. [S]
- Whether Leanheat or an equivalent is already offered in LT: **[U]**. Danfoss has a Vilnius subsidiary and a large LT substation market share [K], so the risk that Danfoss LT already sells Leanheat is **real**. Check this first.

### (a) Skeptical SfT jury member
- **Exciting?** Low to medium. "Heating curves" and "riser balancing" are engineering words. The human story (grandma opening the window at 25°C while the neighbour runs an electric heater) is good, but it isn't dramatic.
- **Clear?** Medium. The chain "sensors → model → curve → maintainer → savings" has four hops. Judges lose people at hop three.
- **Novel?** Honestly low. "Danfoss already does exactly this" will be said by at least one judge (engineering or energy jurors are common on SfT panels [K]). "Sparse sensors for fragmented LT blocks" is a real but subtle difference.
- **Credible from 15-year-olds?** The data is very credible ("our building, Flat 12, 25.4°C"). The control claim is not: nobody will let students change a real substation curve before Nov 6.
- **TOP 5?** Possible but not likely. It reads as a solid engineering project, not a stand-out. It risks being filed with the other "smart home sensor dashboards".
- **Baltic final?** Transferability is excellent (all post-Soviet housing stock). But the demo is weaker than other finalists' will be.

### (b) End user: a building maintainer company / heat utility service arm
**First 30 seconds, realistically:** "We already lower the curve when nobody complains. When people complain we raise it again. Your sensors are in 8 flats, but the complaint comes from the 9th, the corner flat on the top floor. And who installs and maintains sensors in private flats? Who answers when a battery dies? Also, if the building uses less, our fee doesn't change. Why would I bother?"

The incentive picture:
- **The maintainer's fee** is typically fixed per m² [K]. Saving energy doesn't pay them; complaints cost them. So their rational objective is *zero complaints*, which means keeping it hot. HeatTwin's AI must be sold as **"complaint prevention + legal compliance"**, not savings.
- **The heat utility** (often the same group) sells heat. Regulated pricing reduces the conflict, but a supplier won't push for lower sales. Leanheat's buyers in Finland are **landlords who pay the bill** (Espoo Asunnot). **LT's closest equivalents:** the municipal social-housing owner, or a **homeowner association (bendrija) chair** of an energetic block. Those are the realistic buyers, not maintainers.
- **Split incentive:** residents billed by m² save collectively, so the individual who opens a window pays 1/60th of the cost. The system helps the *building*, and the buyer has to be the building's decision-maker.
- **What they already use [K]:** remote substation monitoring/SCADA by larger utilities (supply/return temperatures, heat meter), and Danfoss ECL/Siemens/Regin controllers with weather compensation. Some LT maintainers already have remote read access. Remote *write* access for curve changes varies [U].

### (c) Domain engineer
- **Do LT substations accept remote curve changes?** Modern controllers (e.g. Danfoss ECL Comfort 310 with a network/Modbus module, Siemens Synco) technically support remote setpoint and curve changes [K]. Leanheat integrates with ECL [K]. **But** many 1990s–2010s units have no network module, and the maintainer decides. For the pilot, the output is a recommendation typed in by hand. That's fine.
- **The Soviet-system catch [K]:** many 1960s–80s blocks have **single-pipe (vienvamzdė) systems**, often without thermostatic valves and without riser balancing valves.
  - Lowering the supply curve cools **all** flats. The **coldest representative flat pins the curve**.
  - In an unbalanced block, a curve optimiser alone achieves little. Savings need **balancing first**, which means a plumber, valves and capital work.
  - So HeatTwin's real deliverable is **a diagnosis** ("risers 3 and 7 overheat by 3°C; install balancing valves here"). That is a one-off audit, not a continuous AI service.
  - This is a real weakness in the adoption story, though not a fatal one.
- **Can 6–10 sparse sensors infer the building?** Top floor, ground floor, corner and middle flats per riser: enough to detect imbalance and set a comfort floor [K]. Leanheat samples a large fraction of flats. Occupant behaviour adds noise with sparse sampling (a sensor next to the radiator, an electric heater, cooking), so placement protocols matter.
- **Physics timescales:** a Soviet panel block's thermal time constant is on the order of tens of hours (days for heavy blocks) [K]. The AI's genuine value is **predictive preheating/setback against the weather forecast** and **peak shaving**, which Espoo showed (−17% peak) [S]. That part does pass the collapse test. But the energy share (−6%) mostly comes from simply lowering the curve, which a human with data can do.
- **Collapse test, honestly:** "Remove the AI, give the maintainer 8 cheap loggers and a spreadsheet, and he lowers the curve 2°C in week 1 and gets most of the savings." **The sensors are essential. The AI is a nice-to-have.** That is uncomfortably close to the team's "wrapper" rejection pattern.
- **Hygiene norm [U]:** LT hygiene norm HN 42:2009 sets indoor temperatures in the heating season (roughly 18–22°C for living rooms [U]). The optimiser needs that floor, and the pitch should cite it.

**Fatal technical flaw?** None fatal. The main flaw is that the continuous-AI claim adds only marginal value over "sensors + a rule", and single-pipe blocks without balancing valves limit what control alone can do.

### (d) The 16-year-old team, 6 weeks
**Build:**
- 8–10 ESP32 + SHT31/BME280 nodes (~€10 each)
- Optionally a clamp-on sensor on the substation supply/return pipes (needs basement access from the maintainer)
- An LHMT weather API feed
- A grey-box RC model in Python
- A 3D block visualisation

**Hardest parts:**
1. **Recruiting volunteer flats in the right positions**, not just "team members' flats". Team flats cluster in one riser.
2. **Getting substation data** (supply/return temperatures, heat meter). Without it, the model sees only indoor temperatures and weather, and the curve recommendation is guesswork.
3. Heating may start only mid-October [K: municipalities start heating after 3 days below 10°C], which leaves **~3 weeks of data**. That's enough for an overheating map, thin for a thermal model, and zero for a validated saving.

**Real pilot data by Nov 6?** Yes: indoor temperature distributions and overheating degree-hours, and possibly visible window-opening events (sharp temperature drops). **No:** any measured saving. A curve change needs the maintainer, then weeks of comparison.

**Stage demo:** a 3D block heatmap plus a tabletop mini-block with resistor "radiators". Heat is **slow**: on stage nothing visibly happens in 3 minutes unless the model is tiny and heavily sped up, and then it looks fake. **Wow factor is low.** The emotional moment ("Flat 12, 25.4°C, window open, last Tuesday") is good but lands on a slide.

**Fun and proud?** Moderately. It's real engineering with real data from their own homes, but "we made a dashboard" is what many teams will show.

### Fatal flaws
None technical. For **this contest**, the combination of (1) a Danfoss product doing exactly this, (2) an AI that adds only marginal value over sensors and a rule, and (3) a slow, dashboard-shaped demo is close to fatal for jury ranking. It fails the team's own "tech is a wrapper" smell test more than the scout admits (the scout self-scored collapse 9; realistic is ~6).

### Fixable weaknesses and fixes
| Weakness | Fix |
|---|---|
| "Danfoss does this" | Email Danfoss LT **this week**. If Leanheat is not deployed in LT, get that in writing, because it becomes a strength. If it is, KILL |
| AI is marginal | Make the AI do what humans can't: **infer which risers or flats are under- or over-heated from sparse sensors plus the substation return temperature** (a virtual sensor for unmeasured flats), and **forecast-driven peak shaving**. Show a baseline: "rule-based lowering saves X, forecast AI adds Y" |
| Wrong buyer | Sell to the **bendrija chair / municipal social-housing owner** ("your building overheats by 3°C; here's €X/yr"), with the maintainer as executor and the energy-poverty lens (heating compensation) for the municipality |
| Single-pipe + no valves | Make the product output a **"balancing prescription"** (which riser, how much). It turns a vague AI promise into a plumber's work order, and savings follow |
| Slow demo | Pre-record a real time-lapse of 3 weeks in their block and show the "what if" curve replay live. Don't try to heat something on stage |

### Sharpened version: **"HeatTwin: the overheating X-ray for unrenovated blocks"**
- 8 sensors for 3 weeks, together with the utility's public per-building consumption data. The AI infers a **temperature map of every flat** (virtual sensors) and a **balancing + curve prescription** with € per flat per year.
- Delivered as a **€100 audit kit the bendrija rents from the municipality's energy agency**, not a subscription.
- The first 1–2°C are recovered by the prescription. The forecast AI then handles peaks.

**One-sentence pitch:** *"28,000 Lithuanian blocks won't be renovated this decade, and many are heated to 25°C with the windows open. Eight €10 sensors and our AI find which risers overheat and tell the maintainer exactly what to change, saving each flat €X a winter without a single brick."*

### Scores (1–10)
| Collapse | Adoption loop | Proven tech | Measurable impact | Novelty | Demo wow | Local evidence | Jury appeal |
|---|---|---|---|---|---|---|---|
| 6 | 5 | 9 | 7 (overheating measurable; savings not by Nov 6) | 5 | 4 | 9 | 5 |

**VERDICT: MAYBE (leaning no).** Good engineering and possibly a great *real-world* project, but a weak *contest* project for this team's criteria. Keep it alive only if Danfoss LT confirms Leanheat isn't sold here **and** a bendrija or utility gives substation data access.

---

## 3. ChimneyWatch: rooftop camera AI ranks the smokiest chimneys

### Facts the idea rests on
- Residential combustion is 70–80% of LT PM2.5 emissions (EGUsphere preprint citing EEB). [S] The figure comes from a single preprint that relays another source, so cite it cautiously.
- All LT stations record cold-season PM exceedances; burning waste is banned. [S]
- Boiler-replacement subsidies exist. [S]
- ASTM D7520 / EPA ALT-082 camera opacity. [S]
- Kraków and Katowice drones. [S]
- **Round 2 already rejected the student "smoke fingerprint" idea on ethics** (scout-global rows 7–8). [S] ChimneyWatch is a camera-based cousin of that same idea.

### (a) Skeptical SfT jury member
- **Exciting?** The image is striking: a time-lapse of 300 chimneys with the "worst 10" glowing red.
- **But the first question** will be: *"So you film your neighbours' houses and report them to the municipality?"* The Baltics are sensitive to surveillance [K]. Samsung, as a brand, will not want a winning project that reads as "teens build a snitch camera". Even framed as "friendly advice", the headline writes itself.
- **Credible?** Low once a judge asks "how does it work at 19:00 in December?"
- **TOP 5?** Unlikely. **Baltic final?** No.

### (b) End user: municipal environment officer
**First 30 seconds, realistically:** "We can't act on a camera ranking. For a fine or even an official letter we need an inspector's protocol, and with an address this is personal data. Did the data protection inspectorate approve continuous filming of private homes? We have air-quality stations and complaints; our problem is staff, not information. The subsidy call is oversubscribed anyway [U]. And please, don't put us in the newspaper as the city that spies on chimneys."

- **What they already use [K]:** AAA (Environmental Protection Agency) stations; some municipalities have low-cost sensors (Airly-type, **[U] for LT**); complaint-driven AAD inspections; information campaigns.
- **Would they pay?** Unlikely. The value is an enforcement list they can't legally use.
- **Legal [K]:** under GDPR, a chimney linked to an address is data about an identifiable household's behaviour. Continuous systematic monitoring of private property needs a legal basis and probably a DPIA. A school or a student team has no such basis. A municipality might, but that's a long process, not a 6-week pilot.

### (c) Domain engineer: this is where the idea dies
- **D7520 is not a night or overcast method [K].** It needs:
  - daylight
  - a plume viewed against a contrasting background (ideally clear sky)
  - a sun position within a specified angle behind the camera
  - a calibrated digital camera, with readings valid only under those conditions

  LT heating season:
  - December daylight is ~7 h (Vilnius: sunrise ~08:40, sunset ~15:55 [K]).
  - Skies are overcast most days from November to January [K]. A grey plume against a grey sky gives no usable contrast.
  - **Residential burning peaks in the evening (17:00–22:00) and at weekends [K], in the dark.**
- **Thermal at night doesn't measure opacity.** A thermal camera sees a warm plume and chimney, and every working heater has those. It **can't tell** a clean, hot, dry-wood fire from a smouldering one or from plastic burning. The core metric disappears at night.
- **Steam plumes in cold weather [K]:** at −10°C a **condensing gas boiler's exhaust** makes a thick white plume, and so do wet-wood fires. An opacity model in RGB will rank the *cleanest* heaters (condensing gas) among the "worst". Method 9 readers are trained to read *after* the condensed water vapour dissipates; automating that separation is an unsolved research problem, not a proven building block.
- **Opacity ≠ PM2.5 for residential wood burning [K].** Most PM from stoves comes from cold starts and smouldering, often with thin, bluish, low-opacity smoke. Dark, opaque smoke points to waste or plastic burning, which is useful but a narrower claim.
- **Geometry:**
  - From a school roof (~15–20 m), private-house chimneys 200–800 m away are a few pixels high unless you use a narrow field of view or a PTZ camera.
  - Plumes drift and overlap in perspective, so attributing a plume to a specific chimney among rows of houses is error-prone.
  - "One camera, 300 chimneys" is optimistic. **30–80 attributable chimneys** is more realistic [U, geometry estimate].
- **Fatal technical flaw: yes.** The proven method (D7520) does not hold in the conditions under which the problem occurs (dark, overcast, cold, condensing plumes). That breaks the team's hard criterion 3: "proven building blocks, not hopefully-the-science-works."

### (d) The 16-year-old team, 6 weeks
- **Build:** a Raspberry Pi HQ camera or old phone with a zoom lens, a plume-segmentation model, a chimney registry on a map, and optionally an MLX90640 and 3–5 PM sensors.
- **Hardest part:** getting any usable plume footage. In October, private-house heating is intermittent and evenings go dark from ~17:30 after the DST change (Oct 25) [K]. Labelling plumes versus steam versus sky by hand.
- **Real pilot data by Nov 6:** a handful of daytime weekend clips. The ranking would come from too few observations to be fair to any household, and publishing it would be ethically risky.
- **Stage demo:** a smoke machine, with the opacity readout rising. That is visually fun, but a judge with a phone torch can ask "now do it in the dark".
- **Proud?** They'd enjoy building it, and then spend the Q&A defending surveillance. Not a good place for 16-year-olds.

### Fatal flaws
1. The core measurement method doesn't work in LT heating-season conditions (night, overcast, condensing plumes).
2. The ethics and GDPR problem of filming private homes continuously. The team already killed a close relative of this idea in round 2.
3. The end user can't legally act on the output.

### Fixable weaknesses and fixes
The only honest rescue changes the idea completely: **drop house-level cameras.** Use a **PM2.5 sensor mesh + wind data + AI source-direction inversion** to find the **street or block** where smoke comes from, and target subsidy outreach by street (no individual targeting, so no privacy problem). But low-cost PM meshes are a student classic, already rejected by scout-global ("sensor and then what?"; Airly-type saturation). So the rescue fails the saturation test.

### Sharpened version (if forced)
**"SmokeCompass":** 6 PM2.5 nodes on school and public buildings, with wind direction. An AI back-trajectory model narrows each smoke episode to a ~200 m sector, and the municipality sends a "clean burning + boiler subsidy" leaflet to that sector. The novelty and demo are weak, and it is **not recommended**.

**One-sentence pitch (for the record):** *"Residential stoves make 70–80% of Lithuania's fine-particle pollution. Our sensors trace each winter smoke episode back to the street it came from, so the city can send its boiler-replacement subsidy where it cuts the most smoke."*

### Scores (1–10), original ChimneyWatch
| Collapse | Adoption loop | Proven tech | Measurable impact | Novelty | Demo wow | Local evidence | Jury appeal |
|---|---|---|---|---|---|---|---|
| 8 | 3 | 3 (proven elsewhere, not in these conditions) | 5 | 8 | 7 | 8 | 4 |

**VERDICT: KILL.**

---

## 4. Variant glance: HeatLeak / 50-50 Watts (school classroom sensors)

- **What it is [S]:** temperature, CO₂ and humidity sensors (plus a window reed switch) per classroom. AI flags "heating + open window", weekend and holiday heating, and overheating. It includes a 50/50 savings-sharing deal (Hamburg fifty/fifty and Euronet 50/50 [S as 🟡/unverified]) and a Šiauliai GovTech4All 2024 challenge on school energy monitoring [S, marked V in scout-policy].
- **Jury:** relatable, with a school they can show. But **classroom CO₂ and energy dashboards are one of the most common school STEM projects** [K]. Judges will have seen versions of it. Saturation risk is high.
- **End user (municipal property manager / school caretaker):** "Nice. We've got a BMS in the renovated schools already; in old ones, there are no room valves, so what do I do with 'Room 204 is too warm'?" (Scout-global itself flags "no room-level valves in old schools".)
- **Engineer:**
  - Open-window detection from a temperature/CO₂ drop is trivial and a commodity feature (tado°, Netatmo) [K].
  - The "empty room heated" insight often can't be acted on without room valves.
  - Weekend setback is a controller schedule, no AI needed.
  - **Collapse test fails at the AI layer:** a caretaker plus a timer and a walk-round gets most of it.
- **Team:** the easiest pilot of all four, and data is guaranteed. The demo (a fan blowing cold air, then an alert) is cute but small.
- **The 50/50 money loop is the only genuinely strong part.** It is an adoption mechanism, not a technology, and it can be bolted onto any energy idea.

**Scores:**
| Collapse | Adoption | Proven | Measurable | Novelty | Demo wow | Local evidence | Jury appeal |
|---|---|---|---|---|---|---|---|
| 4 | 7 | 9 | 8 | 3 | 5 | 6 | 5 |

**VERDICT: MAYBE-low. Fallback only.**

**If HeatTwin survives,** the best combination is **HeatTwin deployed in the team's own school building under a 50/50 deal:**
- the municipality is the single owner and payer, which removes the split-incentive and flat-access problems
- sensors in every room are legitimate
- the maintainer answers to the municipality
- the AI's forecast preheating and setback are real

That is still a modest contest entry.

---

## 5. Cross-comparison and final bet

| | HopperGuard | HeatTwin | ChimneyWatch | HeatLeak |
|---|---|---|---|---|
| Collapse | **9** | 6 | 8 | 4 |
| Adoption loop | 6 | 5 | 3 | 7 |
| Proven tech | 7 | **9** | 3 | 9 |
| Measurable impact | 6 | 7 | 5 | 8 |
| Novelty | 6 | 5 | 8 | 3 |
| Demo wow | **8** | 4 | 7 | 5 |
| Local evidence | 8 | **9** | 8 | 6 |
| Jury appeal | **8** | 5 | 4 | 5 |
| **Sum /80** | **58** | 50 | 46 | 47 |
| Verdict | **GO (cond.)** | MAYBE | KILL | MAYBE-low |

**Bet on HopperGuard (sharpened, two-stage, thermal-first).** Why:
1. It is the only idea where the **tech is unarguably necessary**.
2. The problem is **in the LT news every few months**.
3. The core is **proven in the field abroad**.
4. It has a **policy clock** (63% by 2027).
5. The team gets a **loud, physical demo** that 16-year-olds will be proud of.

Its weaknesses (rare events that are hard to measure, the RGB-map overclaim, truck access) can all be fixed by **framing and one partner**, not by new science.

### Must-do in the next 2 weeks (before the Oct 16 form)
1. **Email or call 3 operators or RATCs** (Ecoservice, a municipal company such as Kauno švara [U], VAATC or another regional centre). Ask for (a) the number of truck fires or hot loads in 2023–25, (b) 1 day of hopper-camera footage or a static-camera slot at a collection point, (c) a letter of interest.
2. **Data request to PAGD:** fires in garbage trucks and waste facilities by cause, 2020–25.
3. **Pin down Goodyear specifics:** camera placement, number of trucks, alarms and fires caught. Contact the City of Goodyear's public works office by email if needed.
4. **Ask one insurer** whether a detection retrofit would affect the premium for a refuse truck. One sentence from an insurer strengthens the adoption loop enormously.
5. **Bench test protocol:** heat source × burial depth × material, giving time-to-alarm. Publish the curve including where it fails.
