# Round 5 generator: "mine the internet for real pain"

**Lens.** People have complained online about the same things for decades: on Reddit (r/homeimprovement, r/running, r/Frugal, r/gardening, r/lithuania), on Lithuanian forums and comment sections (supermama.lt, pliuss.lt, delfi and tv3 comments), and in local news that repeats every season ("grybautojai pasiklydo", "žvejai įlūžo", "gyvatukas vėl brangus"). Hackaday and GitHub projects that go viral, and Kickstarter hardware that gets funded, also show demand. I looked for **recurring** pains linked to sustainability or active life, where a cheap device plus AI would really help, preferably with a Lithuanian twist.

**Method and evidence.** The ideas come from my own knowledge of these communities. I used all 8 web searches to check the biggest pains and the prior art for the top picks. Tags:
- **[verified: source]**: confirmed by a search this session.
- **[unverified]**: from memory. Treat as a lead, not a fact.
- In the table, the "who complains, where" column is from memory ([unverified]) unless it has its own tag.

**Scoring.** The 7 round-5 filters, 0–2 each: **Wa** WANT · **Wo** WOW · **NS** NOT-SEEN · **B** buildable in 6 weeks · **AI** AI/IoT does real work · **Big** scales beyond one family · **LT** Lithuanian hook. Total out of 14.

---

## 1. Idea list (36)

| # | Idea | One-line pitch | The real pain (who complains, where) | Theme | Wa | Wo | NS | B | AI | Big | LT | **/14** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **Ledo sargas** (Ice Guard) | A €40 stake frozen into the lake measures ice thickness every 10 min and puts "9 cm, getting stronger" on a public map | Ice anglers and skaters guess ice thickness by drilling or from Facebook rumours. Anglers drown through thin ice every winter [verified: LRT, Ignalina case]. Warm winters make ice unreliable [verified: LRT "Šilta žiema keičia žvejų įpročius"] | Sustainability (climate adaptation) / winter sport | 2 | 2 | 2 | 1 | 2 | 2 | 2 | **13** |
| 2 | **Vandens akis** (Meter Eye) | A camera clipped onto the flat's hot and cold water meters. AI reads them and splits the flow into shower, toilet, leak and "hot water poured away while waiting" | Dads fighting over hot water (the team's own). Running-toilet leaks, a constant r/homeimprovement thread. The circulation ("gyvatukas") fee differs by building and is poorly understood [verified: Ukmergė municipality, Kauno energija]. The GitHub project that reads meters with AI is hugely popular [verified: jomjol/AI-on-the-edge-device] | Sustainability (water, heat) | 2 | 2 | 1 | 2 | 2 | 2 | 2 | **13** |
| 3 | **Aikštelės pulsas** (Court Pulse) | A solar vibration sensor behind the backboard of public courts: a live "game on now" map, per-court leaderboards, and usage data for the municipality | Pickup players walk to an empty court, or one that's full. Municipalities renovate courts blind. Smart hoops exist only as expensive private products [verified: Noah, huupe] | Sport | 2 | 2 | 2 | 2 | 1 | 2 | 2 | **13** |
| 4 | **Grybautojo švyturys** (Picker's Beacon) | A pebble-sized fob for grandparents: one press marks the car, then an LED arrow always points back. SOS over LoRa, "you're walking in circles" warning | Police received 100+ reports of lost mushroom pickers in one season; drones and dog handlers were used [verified: diena.lt, 15min.lt, tv3.lt]. Worried adult children, supermama-style threads "mama vėl išėjo grybauti viena" [unverified] | Active life (seniors outdoors) / nature | 2 | 1 | 2 | 2 | 1 | 2 | 2 | **12** |
| 5 | **Erkių radaras** (Tick Radar) | A white "tick-drag" cloth plus a camera AI that counts ticks, and microclimate stakes, give a daily tick-risk map for trails, parks and school stadiums | Lithuania has the EU's highest tick-borne encephalitis (TBE) rate [verified: ECDC/PubMed]. Parents, dog owners, runners and orienteers ask "are ticks bad in Vingis now?" [unverified] | Active life / nature | 1 | 1 | 2 | 2 | 2 | 2 | 2 | **12** |
| 6 | **Saulės routeris** (Solar diverter) | Sends surplus rooftop-PV power into the electric water heater instead of "storing" it in the grid for a fee; the AI plans around the sun and price forecast | LT prosumers pay to take stored energy back from the grid [verified: ESO/Ignitis FAQ]. There were ~174k prosumers by Feb 2026 [verified: lt.wikipedia via search]. The French DIY "routeur solaire" scene is huge [unverified] | Sustainability (energy) | 2 | 1 | 2 | 1 | 2 | 2 | 2 | **12** |
| 7 | **Namo šilumos žemėlapis** (Block heat map) | €8 temperature tags in many flats of one Soviet block make a live riser-by-riser map. The AI finds imbalance, and the building committee (bendrija) fixes valves instead of arguing | In unrenovated blocks top floors freeze while middle floors keep windows open in January. There are endless delfi comment wars and bendrija meeting fights [unverified] | Sustainability (heat) | 1 | 1 | 2 | 2 | 2 | 2 | 2 | **12** |
| 8 | **Ežero vasara** (Lake summer mode) | The same buoy as #1, in summer: water temperature plus a DIY phycocyanin fluorescence sensor answers "can I swim / let the dog in?" | Blue-green algae in lakes and the Curonian Lagoon. Official beach samples are sparse [unverified]. Dog owners fear toxic blooms (r/dogs) | Sustainability (water) | 2 | 2 | 2 | 1 | 2 | 2 | 2 | 13 → *merged into #1* |
| 9 | **Pelėsio sargas** (Mould guard) | A dew-point sensor in the coldest corner learns the flat and says "air now for 6 min" before mould starts | Mould in Soviet flats after new plastic windows, a classic supermama/pliuss topic [unverified] | Sustainability (heat, health) | 2 | 1 | 1 | 2 | 1 | 2 | 2 | **11** |
| 10 | **Karšto vandens laukimas** (Hot-water wait meter) | A clip-on at the tap logs the seconds and litres until the water is hot and its temperature. Building-wide evidence for recalculating bills | "The hot water runs lukewarm for 2 min." Residents pay for circulation that doesn't deliver [unverified complaint pattern] | Sustainability | 1 | 1 | 2 | 2 | 1 | 2 | 2 | 11 → *module of #2* |
| 11 | **Grybų prognozė** (Mushroom forecast) | Soil moisture and temperature stakes in forests plus picker reports: "boletus flush likely in Labanoras in 4 days" | "Ar jau dygsta?" every August–October in huge Facebook picker groups [unverified size]. People drive hundreds of km for nothing | Nature / active life | 2 | 1 | 2 | 2 | 2 | 1 | 2 | 12 → *the carrot for #4* |
| 12 | **Šliužų radaras** (Slug radar) | A night IR camera counts invasive Spanish slugs, maps their spread by village and times the beer traps | Every LT gardener's summer complaint about "ispaniniai šliužai" in gardening groups [unverified] | Nature (invasive species) | 1 | 1 | 2 | 2 | 2 | 1 | 1 | 10 |
| 13 | **Avilio sargas** (Hive guard) | A hive scale plus microphone detects winter starvation and swarming; hobby beekeepers get an alert | r/Beekeeping staple. Beehive monitors are popular Hackaday builds [unverified] | Nature (pollinators) | 2 | 1 | 1 | 2 | 2 | 1 | 1 | 10 |
| 14 | **Pėsčiojo radaras** (Walker radar) | A rear radar reflector-light for people walking on unlit village roads: flashes harder and buzzes when a car approaches | The Lithuanian reflector (atšvaitas) rule. Grandparents walk dark roads with no sidewalks. Bike radars exist, pedestrian ones don't [unverified] | Active life / safety | 1 | 1 | 1 | 2 | 1 | 2 | 2 | 10 |
| 15 | **Kirtimų ausis** (Chainsaw ear) | Old phones hung in protected forests detect chainsaw sounds and alert rangers (Rainforest Connection model) | The clear-cutting debate in Lithuanian forest-activist groups [unverified] | Nature | 0 | 2 | 1 | 2 | 2 | 1 | 1 | 9 |
| 16 | **Balkono saulė** (Balcony solar) | A plug-in balcony PV kit plus monitor for block residents who can't get a roof | The German Balkonkraftwerk boom. Flat dwellers are left out [legality in LT unverified] | Energy | 1 | 1 | 2 | 1 | 1 | 2 | 1 | 9 |
| 17 | **Pirties laikmatis** (Sauna brain) | Predicts when the wood sauna reaches temperature and stops people overburning wood | The sodyba pirtis ritual: "we burned a whole basket and it's still 60°C" [unverified] | Energy / wood smoke | 1 | 1 | 2 | 2 | 1 | 0 | 2 | 9 |
| 18 | **Kiemo čiuožykla** (Yard rink) | Temperature-guided flooding tells a block yard or school when and how much to flood to build a natural ice rink | r/BackyardRinks is a real niche. Kids lack free skating [unverified] | Sport | 1 | 1 | 2 | 2 | 1 | 1 | 1 | 9 |
| 19 | **Pigi valanda** (Cheap hour) | A smart plug runs the boiler or washing machine in the cheapest Nord Pool hours | LT exchange-price electricity plans, discussed on r/lithuania [unverified] | Energy | 2 | 0 | 1 | 1 | 1 | 2 | 1 | 8 → *part of #6* |
| 20 | **Prietaiso stetoskopas** (Appliance stethoscope) | A clip-on mic plus AI hears a washing-machine bearing failing early, so you repair instead of replace | r/appliancerepair and repair-café culture [unverified] | Stuff / circularity | 1 | 1 | 2 | 1 | 2 | 1 | 0 | 8 |
| 21 | **Žievėgraužio gaudyklė** (Beetle trap cam) | A camera in pheromone traps counts bark beetles in spruce forests | Foresters. Bark-beetle outbreaks after hot summers [unverified] | Nature | 0 | 1 | 1 | 2 | 2 | 1 | 1 | 8 |
| 22 | **Solo rebound** | A cheap ball-return chute plus a shot log for the sodyba or driveway hoop | r/basketball: "rebounding for yourself kills practice" [unverified] | Sport | 2 | 1 | 1 | 1 | 1 | 0 | 2 | 8 |
| 23 | **Šaldytuvo senis** (Old-fridge exposer) | A plug meter tells grandma her 1990s fridge costs €X a year and gives the payback of replacing it | r/Frugal "what's eating my electricity" [unverified] | Energy | 1 | 0 | 1 | 2 | 1 | 1 | 1 | 7 |
| 24 | **Obuolių upė** (Apple river) | A map of sodyba fruit surplus plus a mobile juicer's route planner | Every autumn "atiduodu obuolius nemokamai" posts [unverified]. Mundraub (DE) exists | Food | 1 | 0 | 1 | 2 | 0 | 1 | 2 | 7 |
| 25 | **Malkų drėgmė** (Firewood check) | A moisture probe plus a seller rating stops people buying wet "dry" firewood | Forum complaints about firewood sellers. Wet wood makes smoke [unverified] | Energy / air | 1 | 0 | 1 | 2 | 1 | 1 | 1 | 7 |
| 26 | **Šulinio sargas** (Well guard) | Water level and nitrate trend in sodyba wells | Rural wells with nitrates [unverified] | Water | 1 | 0 | 2 | 1 | 1 | 1 | 1 | 7 |
| 27 | **Barščio medžioklė** (Hogweed hunt) | A dashcam AI maps Sosnowsky's hogweed along roads | Municipal invasive-species fights [unverified] | Nature | 0 | 1 | 1 | 1 | 2 | 1 | 1 | 7 |
| 28 | **Plaukiko palydovas** (Swim buddy) | A float/wearable for open-water swimmers that alerts the shore when the swimmer stops moving | LT drownings at lakes [unverified rate] | Sport / safety | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 7 |
| 29 | **Sodybos šalnos** (Frost SMS) | Microclimate frost alert to grandma's button phone: "cover the strawberries tonight" | May frosts, r/gardening | Food | 1 | 0 | 0 | 2 | 1 | 1 | 1 | 6 |
| 30 | **Ruonių termometras** (Winter-swim temp) | Live water temperature for winter-swimming clubs | Winter swimming clubs [unverified] | Sport | 1 | 0 | 1 | 2 | 0 | 1 | 1 | 6 → *in #1* |
| 31 | **Lauko treniruokliai** (Outdoor gyms) | A usage sensor plus QR coaching on municipal outdoor gym equipment | Outdoor gyms installed, then left unused [unverified] | Sport | 0 | 0 | 1 | 2 | 1 | 1 | 1 | 6 → *in #3* |
| 32 | **Duobių žemėlapis** (Pothole map) | Bike accelerometers map spring potholes | Spring "duobės" complaints | Active life | 0 | 0 | 0 | 2 | 1 | 1 | 1 | 5 |
| 33 | **Rūsio potvynis** (Basement flood) | A water alarm for shared basements in blocks | Flooded storage cellars [unverified] | Water | 1 | 0 | 1 | 2 | 0 | 1 | 0 | 5 |
| 34 | **Dviračio sargas** (Bike guard) | A hidden tracker plus movement alarm | Bike theft threads | Active mobility | 1 | 0 | 0 | 2 | 0 | 1 | 0 | 4 |
| 35 | **Inventoriaus mainai** (Gear swap) | A school locker for outgrown skates and skis | Kids outgrow gear yearly (too close to RecessBox) | Sport / stuff | 1 | 0 | 1 | 1 | 0 | 1 | 0 | 4 |
| 36 | **Gintaro prognozė** (Amber forecast) | Wind and wave data predict amber washing up on the Baltic coast | Amber hunters after storms (a fun LT niche, weak theme fit) | Nature | 1 | 1 | 2 | 2 | 1 | 0 | 2 | 9 (off-theme) |

**Pattern.** The high scorers fall into two families:
- **Seasonal Lithuanian nature rituals that go wrong**: thin ice, lost pickers, ticks.
- **Soviet-block money pains nobody can see**: hot water, the circulation fee, heat imbalance.

Both have a built-in "every year the news says…" hook, and both give the device a reason to be used again and again, not once.

---

## 2. Top 5 profiles

### #1 Ledo sargas: live ice thickness for every lake (13/14)

**What it physically is.**
- A 1.2 m PVC stake holding a chain of ~40 DS18B20 digital temperature sensors spaced 2–3 cm apart, plus an ESP32, a LoRa or LTE-M modem, a battery and a small solar cap.
- It is anchored at a popular angling or skating spot before freeze-up (hung from a pier or a buoy), so the ice grows around it.
- The temperature profile shows air (cold, noisy), snow (insulating gradient), ice (a linear gradient) and water (flat, near 0 °C). The ice–water boundary is where the gradient flattens.
- This is the same principle as Canada's SmartICE buoys, which use thermistor strings to measure ice and snow thickness [verified: smartice.org].

**Who wants it, and why they'd use it again and again.**
- Ice anglers (poledinė žūklė is a mass hobby), skaters, winter walkers and the "ruoniai" winter swimmers.
- They check the map before every trip, all winter, like a weather app.
- The official rule of thumb is ≥7 cm for one person and ≥12 cm for a group [verified: Alkas.lt citing the Environmental Protection Dept.], so the display is simply "7 / 12 cm reached here?".
- People drown through thin ice each winter. In one recent case an Ignalina angler and his dog died [verified: LRT].

**Wow demo.**
- A clear tank of water freezing in a chest freezer. Time-lapse the growing ice next to the live profile graph.
- On stage, bring a pre-frozen bucket with the stake. The map dot reads "8 cm, stiprėja" (getting stronger).
- Pour warm water under the ice or blast the top with a heat gun: the forecast flips to "red by Thursday: thaw".
- The "we measured ice with 40 thermometers" moment is what a 16-year-old would be proud to explain.

**What the AI/IoT actually does.**
1. **Infers thickness** from a noisy profile, including snow on top and slush layers. It classifies each sensor as air, snow, ice or water with a small model trained on freezer runs.
2. **Forecasts 3–5 days ahead**: the growth or decay of the ice from the weather forecast (freezing degree-days, Stefan's law) with a per-lake learned correction.
3. **Crowd calibration**: anglers who drill a hole enter the measured cm, and the model learns how far the stake's value extends across the lake (bays, inflows and reeds freeze differently).

It is a real sensor-fusion and forecasting problem, not an LLM wrapper.

**What exists, honestly.**
- SmartICE is proven in 40+ Canadian Arctic communities [verified: smartice.org].
- Scientific ice-mass-balance buoys cost thousands [unverified price].
- The Nordics have crowdsourced ice-report apps [unverified].
- In Lithuania, as far as I know, people rely on Facebook groups and drilling [unverified].

Ours is a cheap version for lakes, for recreation, plus a year-round **summer mode** (idea #8: water temperature and a DIY blue-green-algae fluorescence sensor), so one buoy earns its place 12 months a year.

**How it scales.** One stake per popular lake: municipalities, the fire and rescue department (PAGD), angling clubs and the Environmental Protection Dept. all have an interest. It also produces a lake-ice climate dataset for Lithuania's many lakes, a sustainability story about warming winters [verified: LRT on warm winters changing angling habits]. The same approach works in Latvia and Estonia.

**LT hook.** Thousands of lakes [exact count unverified], a national winter angling habit, and news every December about anglers going through the ice.

**Biggest risk.**
- **Timing.** There is no natural ice before Nov 6, so the pilot is a freezer lab plus a real deployment in December for the Baltic final.
- **Liability.** Never display "safe", only "measured here, now" next to the official thresholds.
- **Vandalism and theft** of the stake.

---

### #2 Vandens akis: the water meter that tells the truth (13/14)

**What it physically is.**
- An ESP32-CAM in a 3D-printed hood that clamps over the flat's existing hot and cold water meters. No plumbing, nothing to seal, which fixes ShowerCoach's leak and installation problem.
- A €2 temperature probe clipped onto the hot pipe.
- An old Galaxy phone on the bathroom wall as the live display, if wanted.

**Who wants it, and why they'd use it repeatedly.**
- The team's own dad ("wasted hot water"), and every family with the "get out of the shower" fight. This is the one want-it reaction from round 4, kept, but for the whole flat.
- It runs continuously: leak alarms, a monthly bill forecast, and automatic readings when the family declares its meter readings [the LT self-declaration practice is unverified per utility].

**Wow demo.**
- A real meter on a small pump rig with a clear pipe.
- Flush a toy cistern: "WC flush, 6 L".
- Let a valve drip: "hidden leak: X L/day ≈ €Y/year".
- Open the hot tap while the "hot" water is still cold: "you poured 4 L down the drain waiting. Your building's circulation is failing."

**What the AI/IoT actually does.**
1. Reads the digits and the fast red 0.1 L dial with TFLite. The jomjol open-source models already do this [verified: GitHub jomjol/AI-on-the-edge-device], so we reuse them.
2. **Our new part: event disaggregation.** It splits the high-resolution flow series into shower, bath, toilet, dishwasher and leak events (the Flume idea, unverified details), plus a night-baseline leak detector.
3. **Hot-water wait detection.** Hot meter turning + pipe still cold = litres of "cold hot water". Aggregated across flats, it shows the building's circulation health.

**What exists, honestly.**
- jomjol is a popular hobby project [verified].
- Flume (US) and LeakBot (UK) sell leak and usage devices [unverified details].
- Utilities are rolling out remote-read meters in places [unverified for LT].

Ours differs in three ways:
- it is non-invasive and retrofits Soviet-block meters;
- it measures hot-water waste and circulation quality, which no consumer product targets;
- it rolls up to the building for the bendrija.

**How it scales.** Every flat in the old block stock has the same meter types. Building committees and administrators get the dashboards, heat and water utilities could run pilots, and energy-poverty programmes could loan devices.

**LT hook.** The "gyvatukas" fee: residents pay for the heat that circulates hot water and warms the bathroom towel rail, and the amount varies by building and month [verified: Kauno energija, Šilutės šilumos tinklai, Ukmergė municipality]. VAT on central heating and hot water was proposed to rise from 9% to 21% in the 2026 tax reform [verified: search summary of LRT/finmin; check the final outcome].

**Biggest risk.**
- Cramped, dark meter niches and Wi-Fi in bathrooms.
- Accuracy of event splitting with only 0.1 L resolution.
- Privacy (shower times reveal who is home), so process locally.
- **NOT-SEEN is only 1/2**: meter-reading is known in maker circles, so the pitch must lead with disaggregation and the hot-water-wait insight.

---

### #3 Aikštelės pulsas: a live pulse for every outdoor basketball court (13/14)

**What it physically is.** A weatherproof box zip-tied behind the backboard: an ESP32, an IMU (accelerometer), an optional piezo on the rim, a mic, and a small solar panel with a battery. No camera. It sends data over LoRa, LTE-M or nearby Wi-Fi.

**Who wants it, and why they'd use it repeatedly.** Teen and adult pickup players ask "is anyone at the court?" every evening. They get:
- a live map ("Šilainių aikštelė: game on, ~6 players, 40 min");
- a "best time to find a game" calendar per court;
- **court-vs-court leaderboards** (district rivalries), which is the part teens will actually check.

**Wow demo.** A hoop on stage. A juror shoots. The phone map dot pulses, and the event is classified live: "bank shot", "rim-out", "air ball". Then show a week of pilot data as a heat-map of when the town's courts are alive.

**What the AI/IoT actually does.**
1. On-device TinyML tells backboard hits, rim hits and makes (rim piezo plus net-swish acoustics) apart from wind, rain and kids hanging on the rim.
2. It estimates the number of players from shot rate and rhythm.
3. It aggregates courts into usage analytics: which courts need new rims, lights or resurfacing. The **municipality** has no data today and renovates blind [unverified].

**What exists, honestly.**
- Noah and huupe are expensive private smart-hoop systems [verified].
- Courts of the World is a static court map [verified].
- BallerCam is camera-based and aimed at teams [verified].

I found no live, camera-free network measuring activity on public courts [search found none; absence unverified]. Ours is cheap, anonymous and public.

**How it scales.** Every block-yard court in Lithuania, and the same sensor fits football goals and outdoor gyms (idea #31). The municipality buys it as a "sport infrastructure usage" tool. It fits "make sport accessible" exactly.

**LT hook.** Basketball is the national religion. Courts in block yards are everywhere [count unverified]. Pitch line: "we know every Žalgiris stat but not whether our own court is used".

**Biggest risk.**
- Reliably detecting makes without a camera; start with "shots/activity" and add makes later.
- Vandalism.
- The pilot runs Oct–Nov, when outdoor play drops, so run 2–3 outdoor courts plus the school hall.

---

### #4 Grybautojo švyturys: a way home for mushroom-picking grandparents (12/14)

**What it physically is.**
- A pebble-sized fob with GPS, a compass, an accelerometer, an nRF/ESP32, LoRa, one big button, a ring of 8 LEDs and a vibration motor.
- One press at the car stores "home". After that the lit LED always points back to the car, and the ring's colour shows the distance.
- A long press sends an SOS.
- A matching **car unit** (a LoRa gateway plus buzzer and light) stays in the car. It relays the SOS and track to family by SMS and beeps and flashes to guide the picker for the last few hundred metres.
- No smartphone, menus or screen: designed for 65+ with button phones.

**Who wants it, and why they'd use it repeatedly.**
- Adult children buy it for their parents. Pickers carry it on every forest trip, all season, for years.
- The carrot for daily use: it privately logs "my spots" (where you stopped and picked), and anonymised, fuzzed data feeds a **mushroom-flush forecast** (idea #11), the question every Lithuanian asks each autumn.

**Wow demo.**
- A juror presses "car" at the stage door, walks a loop around the hall, and the arrow keeps pointing back.
- Then a simulated "lost" alert: the family phone gets an SMS with the track and a map.
- Show a real pilot track where the device warned "you're walking in circles, sunset in 50 min, 40 min to the car".

**What the AI/IoT actually does.**
1. Detects circling and disorientation from the track.
2. Computes a turn-back time from walking speed, distance, sunset and battery.
3. Detects falls and long inactivity with the accelerometer.
4. Aggregates the spots for a forecast model built with public weather data.

This is modest but real work (AI 1/2).

**What exists, honestly.**
- Phone apps (a Google Maps pin, Mapy.cz) work only if grandma uses a smartphone and it has battery.
- Bushnell's BackTrack was a GPS "return to point" gadget [unverified whether still sold].
- Garmin inReach satellite communicators exist but are expensive.

Ours is the only one designed for elderly pickers, with the car as the rescue beacon, cheap enough for police or municipalities to lend out.

**How it scales.**
- Rural district offices (seniūnijos), police prevention campaigns and the state forest enterprise lend them at forest parking lots.
- The same culture exists in Latvia, Poland, Finland and Belarus.
- Search-and-rescue costs (drones, dog handlers, helicopters) are a public expense [verified that these are used: 15min, diena].

**LT hook.** Police received **100+ reports of lost mushroom pickers already this year** [verified: diena.lt via search]. The drone rescue of two men born in 1956 and 1959 near Mickūnai is a ready-made opening story [verified: diena.lt, 15min.lt].

**Big advantage.** **It can be piloted now**: the mushroom season runs through October, so 10 grandparents can test it before Nov 6.

**Biggest risk.** Theme fit. Frame it as "active life for seniors outdoors" (Sport & tech) or "safe access to nature". The AI is thin unless the forecast layer is real. GPS under dense canopy can be inaccurate.

---

### #5 Erkių radaras: the daily tick-risk map (12/14)

**What it physically is.**
- **(a) A drag kit:** a 1×1 m white flannel on a pole, the standard tick-sampling method [unverified as the national protocol]. After a 100 m drag, a phone or ESP32-CAM photo stand takes a picture and a detection model counts nymphs and adults.
- **(b) Microclimate stakes** in popular trails, parks and school stadium edges measure leaf-litter temperature and humidity.

**Who wants it, and why they'd use it repeatedly.** Parents, dog owners, runners, orienteers and PE teachers check "tick risk today" before every walk in season, and get a "check yourself now" reminder after. Scouts, school eco-clubs and running clubs do the weekly drags. That is a large community task, which makes it good for a pilot.

**Wow demo.** A (sealed) jar of real ticks on the table: people lean forward. Then the drag cloth goes under the camera and boxes appear on every tick. Then the city map with red trails.

**What the AI/IoT actually does.**
1. Small-object detection separates ticks from seeds and dirt on the cloth. It is trained by the team, not a wrapper.
2. An activity model learns from microclimate and drag counts: ticks quest when it is warm and humid [threshold unverified] and hide in dry heat.
3. It forecasts risk per trail and per day from the weather forecast.

**What exists, honestly.** Tick citizen science and risk maps exist elsewhere, for example the Dutch Tekenradar and German tick forecasts [unverified details]. I don't know of a Lithuanian one [unverified]. Ours automates the counting and adds hyperlocal sensors.

**How it scales.** Every municipality with forest parks. The public health centre (NVSC) and public health bureaus get data, schools get a PE-season tool, and the same method works across the Baltics.

**LT hook.** **Lithuania has the highest tick-borne encephalitis rate in the EU**, e.g. 21.9 per 100k in 2016 against Estonia's 6.1 [verified: ECDC annual report via search; also PubMed on 25.45/100k during COVID].

**Biggest risk.** Season: ticks fade by November, so the pilot must run in the next 4–5 weeks. WANT is weaker than the others ("I'll just use repellent"). The ticks-on-stage demo might gross out the jury (or win it).

---

### Honourable mentions (12/14, not profiled)
- **#6 Saulės routeris.** Strong money pain for ~174k prosumers who pay to take energy back from the grid [verified: ESO/Wikipedia], but it involves 230 V switching by teens and has a low-wow demo.
- **#7 Namo šilumos žemėlapis.** A great Soviet-block story, but it needs many neighbours to join and people want it less individually. It would combine well with #2 as a "building" layer.

---

## Summary: my top 5

1. **Ledo sargas (13/14).** A €40 thermistor stake freezes into the lake. The AI infers and forecasts ice thickness and puts it on a public map against the official 7/12 cm rules. Proven by SmartICE in Canada, unseen in Lithuania. Anglers drown every winter. A summer algae mode makes it year-round. Risk: no ice before Nov 6, so the pilot is a freezer lab plus a December deployment.
2. **Vandens akis (13/14).** A camera clips onto the flat's meters (no plumbing). The AI splits the water use into shower, toilet, leak and "cold hot water" waiting, and rolls it up to show a building's circulation (gyvatukas) failing. It keeps ShowerCoach's want-it reaction without its problems.
3. **Aikštelės pulsas (13/14).** A camera-free backboard sensor gives a live "game on" map, court leaderboards, and the first usage data municipalities have for their courts. Basketball culture plus sport accessibility.
4. **Grybautojo švyturys (12/14).** An arrow-home fob and car beacon for elderly mushroom pickers: 100+ lost-picker reports to police this year, and it can be piloted **right now** in the mushroom season. The forecast layer drives repeat use.
5. **Erkių radaras (12/14).** A tick-drag AI counter plus microclimate stakes make a daily tick-risk map in the EU's TBE hotspot. Very Lithuanian and unseen, with weaker personal want.

**The strongest pair for the team:** #1 (the biggest wow and newest to Lithuania) or #2 (the most personal want, closest to their own home). #4 is the safest to pilot before Nov 6.

## Sources (searches this session)
- Gyvatukas fee: [Kauno energija](https://www.kaunoenergija.lt/dazniausiai-uzduodami-klausimai/karsto-vandens-temperaturos-palaikymo-gyvatuko-mokestis) · [Ukmergė municipality](https://www.ukmerge.lt/naujienos/kodel-skiriasi-karsto-vandens-cirkuliacijos-gyvatuko-mokestis/?lang=lt) · [Šilutės šilumos tinklai](https://silutesst.lt/pages/kas-yra-gyvatuko-mokestis) · [Pasvalys](https://www.pasvalys.lt/naujienos/1/kaip-apskaiciuojamas-buto-mokestis-uz-cirkuliacine-siluma-gyvatuka:8669) · [LRT tax reform](https://www.lrt.lt/naujienos/verslas/4/2560151/svarbiausi-pakoreguotos-mokesciu-pertvarkos-pakeitimai-kas-siuloma)
- Ice: [SmartICE technology](https://smartice.org/our-smart-technology/) · [Alkas.lt ice thickness rules](https://alkas.lt/2025/02/16/poledine-zukle-pries-zvejyba-svarbu-atsakingai-ivertinti-ledo-stori-ir-laikytis-zvejybos-taisykliu/) · [LRT drowned angler](https://www.lrt.lt/naujienos/lietuvoje/2/1306472/gelbetojai-ispeja-poledinei-zuklei-dar-per-anksti-del-plono-ledo-jau-nuskendo-vienas-zvejys) · [LRT warm winters](https://www.lrt.lt/naujienos/gyvenimas/13/1137493/silta-ziema-keicia-zveju-iprocius-poledines-zukles-siemet-nebesitiki)
- TBE: [ECDC LT profile](https://www.ecdc.europa.eu/en/publications-data/country-profile-lithuania-tick-borne-encephalitis-tbe) · [ECDC AER 2016](https://www.ecdc.europa.eu/sites/portal/files/documents/AER_for_2016-TBE.pdf) · [PubMed 35160255](https://pubmed.ncbi.nlm.nih.gov/35160255/)
- Courts: [Noah](https://www.noahbasketball.com/products/noah-backboard) · [huupe](https://huupe.com/) · [Courts of the World](https://www.courtsoftheworld.com/map/) · [BallerCam](https://ballercam.com/pages/sports-basketball)
- Meter AI: [jomjol/AI-on-the-edge-device](https://github.com/jomjol/AI-on-the-edge-device)
- Mushroom pickers: [diena.lt (100+ reports)](https://m.klaipeda.diena.lt/naujienos/klaipeda/nusikaltimai-ir-nelaimes/tikras-galvos-skausmas-grybautojai-miskuose-iesko-grybu-o-policija-grybautoju-1040204) · [15min drones](https://www.15min.lt/naujiena/aktualu/nusikaltimaiirnelaimes/sezoninis-kriminalas-vyrai-ieskojo-grybu-vyrus-surado-dronai-59-2771040) · [vilniaus.diena.lt Mickūnai rescue](https://vilniaus.diena.lt/naujienos/vilnius/nusikaltimai-ir-nelaimes/miske-dvieju-grybavusiu-vyru-gelbejimo-operacija-rasti-perslape-ir-pavarge-1776230)
- Prosumers: [lt.wikipedia Saulės energetika](https://lt.wikipedia.org/wiki/Saul%C4%97s_energetika_Lietuvoje) · [Infoerdve ESO record](https://infoerdve.lt/eso-rekordas-53-tukst-nauju-gaminanciu-vartotoju-2025-m/) · [Ignitis FAQ](https://ignitis.lt/duk/saules-energija)
