# Round 5 generator: Lithuanian nature and outdoor life

**Lens:** where sustainability meets being active: forests, lakes, mushrooms, ticks, ice, sodybos, the Baltic.
**Date:** 2026-09-25. **Search budget:** 5 WebSearch calls, all used (sources at the end). Claims are tagged **[verified: source]** or **[unverified]**. "[memory]" means the claim comes from general knowledge and was not checked in this session.

---

## 0. What the 5 searches changed

| Finding | Consequence |
|---|---|
| Police say **more than 100 reports of lost mushroom pickers** this year, and 16 people got lost in Kaunas county forests **in August alone**. Searches use police, dog handlers, drones and firefighters, and the lost pickers are typically born in the 1950s. [verified: [klaipeda.diena](https://m.klaipeda.diena.lt/naujienos/klaipeda/nusikaltimai-ir-nelaimes/tikras-galvos-skausmas-grybautojai-miskuose-iesko-grybu-o-policija-grybautoju-1040204), [kauno.diena](https://m.kauno.diena.lt/naujienos/kaunas/nusikaltimai-ir-nelaimes/skambina-pavojaus-varpais-vien-rugpjuti-kauno-apskrities-miskuose-pasiklydo-16-zmoniu-1041404), [15min](https://www.15min.lt/naujiena/aktualu/nusikaltimaiirnelaimes/sezoninis-kriminalas-vyrai-ieskojo-grybu-vyrus-surado-dronai-59-2771040), [rinkosaikste](https://rinkosaikste.lt/pasiklydusiai-grybautojai-i-pagalba-skubejo-policininkai-kinologas-ir-ugniagesiai-naujas/)] (the year of the ">100" figure is not stated in the snippet; the article is recent) | **New #1.** A real, recurring, very Lithuanian problem, and the season is **now**, so a pilot can happen before Nov 6. |
| **Mushroom forecast apps already exist and cover Lithuania**: Boletus (boletusmap.eu, 7 countries including LT, a soil/tree layer plus daily moisture and temperature), ShroomCast, Waldschatzfinder (DE), and mushboom (PL). [verified: [boletusmap.eu](https://boletusmap.eu/), [shroomcast](https://shroomcast.net/), [github mushboom](https://github.com/bialasky/mushboom)] | A plain "where will mushrooms grow" forecast is **not new**. Dropped as a lead and rebuilt as a safety device (#1). |
| TBE: **807 cases in 2024 with 11 deaths** in LT. Lithuania has the highest incidence in Europe, and the NVSC headline says Lithuanians "get vaccinated sluggishly". Since 9 Dec 2025 vaccination is **free for people aged 50–60**. [verified: [NVSC](https://nvsc.lrv.lt/lt/uzkreciamuju-ligu-valdymas/erkinis-encefalitas-lietuva-endemine-teritorija-taciau-lietuviai-skiepijasi-vangiai/), [ulac.lt](https://ulac.lt/nemokami-skiepai-nuo-encefalito-2026-m-kas-juos-gaus/)] Incidence in the **unvaccinated** population was **30.5/100k/yr (2019–23)**, and vaccine effectiveness is ≥97.4% in every Baltic country. [verified: [PMC12452677](https://pmc.ncbi.nlm.nih.gov/articles/PMC12452677/)] National vaccination coverage in % was **not found** [gap]. | Round 3 killed the tick idea because "the fix is vaccination". But uptake is the actual problem, and Lyme disease has no vaccine. The tick idea only survives if it has a **physical sensing part** (TickBot) and pushes people toward vaccination. |
| Ice: PAGD's rule is ≥7 cm of ice for one person and ≥12 cm for a group or fishers. Fishing rules require fishers to carry ice picks. Every winter the news repeats the same story: an ice fisher drowns early in the season on thin ice, often near a stream inflow. [verified: [AM](https://am.lrv.lt/lt/naujienos/zvejyba-ant-ledo-ka-reikia-zinoti-zvejams/), [LRT](https://www.lrt.lt/naujienos/lietuvoje/2/1306472/gelbetojai-ispeja-poledinei-zuklei-dar-per-anksti-del-plono-ledo-jau-nuskendo-vienas-zvejys), [tv3](https://www.tv3.lt/naujiena/lietuva/traku-rajone-nuskendo-ant-ledo-iluzes-zvejys-n1321242)] A national count of **ice-specific** deaths per season was **not found** [gap]. | The ice victims are **ice fishers**, and they drill holes anyway. That points to a crowd-sensing design (#3), not buoys. |

---

## 1. Idea pool (35 ideas)

Scores are 0–2 on the round-5 filters: **W**ANT · W**O**W · **N**OT-SEEN · **B**uildable · **AI**/IoT does real work · bi**G** enough · **LT** hook. Σ is out of 14. Theme: **S** = Sport & tech, **G** = Sustainability.

| # | Name | One-line pitch | Real problem and user | Theme | W | O | N | B | AI | G | LT | Σ |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **BackTrack (Grybų švyturys)** | A €20 clip for mushroom pickers that remembers your secret spots, leads you back to the car without phone signal, and calls for help by itself when your track says you're lost | Over 100 lost-picker call-outs a year, mostly older people; families worry every weekend from Aug to Oct | S (+safety) | 2 | 2 | 2 | 2 | 1 | 2 | 2 | **13** |
| 2 | **Erkių radaras + TickBot** | A small rover drags a white flag through grass, a camera and AI count the ticks it picks up, and those counts plus bite reports and microclimate drive a daily tick-risk map and a "check yourself tonight" nudge | Highest TBE rate in Europe, slow vaccine uptake, and Lyme has no vaccine; users are dog walkers, parents, pickers, campsites | S/G | 1 | 2 | 2 | 1 | 2 | 2 | 2 | **12** |
| 3 | **Poledinis: a tip-up that measures the ice** | An ice fisher's bite alarm with a thermistor string built in: every hole a fisher already drills becomes an ice-thickness sensor on a shared map | The people who drown on ice are mostly fishers on thin early-season ice | S | 2 | 2 | 2 | 1 | 1 | 2 | 2 | **12** |
| 4 | **Ruonis: cold-water swim guardian** | A pod on your swim cap measures water and skin temperature and your stroke rate; AI spots the early fade of cold incapacitation and buzzes "get out now", and raises the alarm if you stop moving | Autumn and winter open-water swimming is growing, and cold shock and swim failure kill even good swimmers | S | 2 | 2 | 2 | 2 | 1 | 1 | 1 | **11** |
| 5 | **Obuolių radaras** | Photograph a sodyba apple tree; AI estimates the kg and the picking window and matches it with teen bike crews, juice presses and food banks | Tonnes of garden apples rot every autumn while presses and food banks need fruit | G (+active) | 2 | 1 | 2 | 2 | 1 | 2 | 2 | **12** |
| 6 | Ice-auger logger | A clip-on sensor on the ice drill detects the break-through moment, so every hole drilled logs a GPS-tagged thickness automatically | Same users as #3; a variant of it | S | 2 | 1 | 2 | 2 | 1 | 2 | 2 | 12 |
| 7 | SmartICE-LT buoys (the original seed) | Solar thermistor buoys frozen into popular lakes feed a public ice map | Skaters and fishers; municipalities | S | 1 | 2 | 1 | 1 | 1 | 2 | 2 | 10 |
| 8 | Smart ice picks | The compulsory ice picks sense immersion and send a LoRa SOS with GPS | Lone ice fishers | S | 1 | 2 | 2 | 2 | 0 | 1 | 2 | 10 |
| 9 | Tekenradar-LT (app only) | Citizens report bites, and a weather model forecasts tick activity | Everyone outdoors; a wrapper on its own | S | 1 | 0 | 1 | 2 | 1 | 2 | 2 | 9 |
| 10 | Tick-on-skin scanner | A phone camera sweeps your legs after a walk, and AI flags poppy-seed-sized nymphs | Parents after forest trips; privacy with images of kids | S | 1 | 2 | 2 | 1 | 2 | 1 | 1 | 10 |
| 11 | Dog-walker tick radar | Daily tick risk plus a babesiosis-symptom checklist for dog owners, fed by vets' case reports | Dog owners walk every day; babesiosis in dogs is common in LT [unverified] | S | 2 | 1 | 2 | 2 | 1 | 1 | 1 | 10 |
| 12 | Mushroom flush forecast with soil stakes | LoRa soil moisture and temperature stakes plus reports predict mushroom flushes | Pickers; **already exists (Boletus covers LT)** | S | 2 | 1 | 0 | 2 | 2 | 2 | 2 | 11 |
| 13 | AI mushroom ID | Photo in, "edible or not" out | Saturated and dangerous (liability) | S | 2 | 1 | 0 | 2 | 0 | 2 | 2 | 9 |
| 14 | Lesyklėlė: AI bird feeder on an old Galaxy | A drawer phone watches a winter feeder, counts species and sends data to ornithologists | Winter feeding is a habit and people check the feeder daily; Bird Buddy exists commercially | G | 2 | 1 | 1 | 2 | 2 | 1 | 1 | 10 |
| 15 | Smart life-ring station | The ring buoy at an unsupervised lake raises an emergency call when it's pulled, and flags theft | Rescue services; not personal repeated use | S | 0 | 2 | 2 | 2 | 0 | 1 | 2 | 9 |
| 16 | "Maudytis?" bloom buoy | A beach buoy measures temperature, turbidity and phycocyanin to warn of cyanobacteria | Swimmers at lakes and the lagoon; summer-only | G | 1 | 1 | 1 | 1 | 1 | 2 | 2 | 9 |
| 17 | Under-ice oxygen sentinel | A dissolved-oxygen logger warns of winter fish kills so the angling club can aerate | Clubs that lease lakes; DO sensors cost €100+ [unverified] | G | 1 | 1 | 2 | 1 | 1 | 1 | 2 | 9 |
| 18 | Slug-watch night camera | An IR camera counts Spanish slugs at night and finds where they hide and lay eggs, so beer traps and collecting happen in the right place at the right time | Every sodyba gardener; autumn egg-laying matters | G | 2 | 1 | 2 | 1 | 2 | 1 | 1 | 10 |
| 19 | SlugBot | A robot that finds and collects slugs at night | Too hard for 6 weeks | G | 1 | 2 | 2 | 0 | 2 | 1 | 1 | 9 |
| 20 | Vilkų sargas | An AI camera at the pasture edge detects a wolf and triggers lights and sound, and logs incidents for compensation claims | Sheep farmers; the wolf debate is hot in LT [unverified] | G | 1 | 2 | 1 | 1 | 2 | 1 | 2 | 10 |
| 21 | Gintaro audra (amber storm) | A model predicts from wind and waves when amber washes up; a UV-lamp phone camera spots it, and hunters log litter picked on the same walk | Amber hunters in Palanga, Klaipėda, Nida; the green link is thin | G/S | 2 | 2 | 2 | 1 | 1 | 1 | 2 | 11 |
| 22 | Campfire smoulder sensor | Official forest fire sites alert the ranger if embers are left glowing | VMU rangers; nobody uses it repeatedly | G | 0 | 1 | 2 | 2 | 1 | 1 | 1 | 8 |
| 23 | Kayak blockage map | Rental kayaks' GPS slow-downs reveal fallen trees and portages on LT kayaking routes | Kayak rentals and paddlers; season over | S | 1 | 1 | 2 | 2 | 1 | 1 | 2 | 10 |
| 24 | Miško receptas | A Galaxy Watch measures your HRV stress drop in the forest versus the city: a "green prescription" | Stressed teens and adults; wellness apps are common | S | 1 | 1 | 1 | 2 | 1 | 1 | 1 | 8 |
| 25 | Trail counters for parks | Counting visitors on trails | Park admins; seen, dull | S | 0 | 0 | 1 | 2 | 1 | 1 | 1 | 6 |
| 26 | Rip-current camera, Palanga | Beach-camera AI marks rip channels | Lifeguards; summer-only | S | 0 | 2 | 1 | 1 | 2 | 1 | 1 | 8 |
| 27 | Septic-tank level sensor | A lakeside sodyba septic tank reports its level and pump-outs, to protect the lake | Owners; low appeal | G | 1 | 0 | 2 | 2 | 0 | 1 | 1 | 7 |
| 28 | Fish-length photo catch log | A photo checks the legal size and logs the catch | Anglers; apps exist | G | 1 | 1 | 0 | 2 | 1 | 1 | 1 | 7 |
| 29 | Natural-ice skate map (Ice-safe 2.0 without hardware) | Sentinel-1 ice-on dates plus Stefan's-law thickness plus crowd reports for every lake | Skaters and fishers; needs ground truth (#3 provides it) | S | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 11 |
| 30 | Stork-nest AI camera | Tracks occupancy and breeding in the "land of storks" | Birders; storks are gone until spring, so no pilot | G | 1 | 1 | 1 | 2 | 1 | 1 | 2 | 9 |
| 31 | Bog berry safety | Cranberry pickers in bogs; opening dates | Tiny, low-tech | G | 0 | 0 | 2 | 1 | 0 | 0 | 1 | 4 |
| 32 | Forest mesh SOS posts | Meshtastic posts in national parks | Infrastructure nobody owns | S | 0 | 1 | 1 | 2 | 0 | 1 | 2 | 7 |
| 33 | XC-ski snow quality | Skiers' phones rate the glide and snow on trails | Small user base, uncertain winters | S | 1 | 1 | 2 | 1 | 1 | 1 | 1 | 8 |
| 34 | Hive winter scale | Hive weight and temperature through winter warn of starvation | Hobby beekeepers; Broodminder/Arnia exist [memory] | G | 2 | 1 | 1 | 2 | 1 | 1 | 1 | 9 |
| 35 | School tick-census kit | Standard 100 m² flag drags by classes each spring and autumn feed #2's map | Schools and biology teachers; part of #2 | G | 1 | 1 | 2 | 2 | 1 | 2 | 2 | 11 |

**Top 5 chosen** (not strictly by Σ; one strong option per theme and season): #1 BackTrack, #2 Erkių radaras + TickBot, #3 Poledinis, #5 Obuolių radaras, #4 Ruonis. **Honourable mentions:** #21 Gintaro audra (the most fun, but the green link is thin) and #29 (becomes the "scale" slide of #3).

---

## 2. Top 5 profiles

### #1 BackTrack (Grybų švyturys): the mushroom picker's way home. Σ 13

**What it physically is.** A matchbox-sized clip for a jacket or basket handle: ESP32-S3, GNSS, a compass/IMU, a LoRa radio, a vibration motor, **three big buttons** and a ring of 8 LEDs. No screen and no smartphone skills needed. A second unit stays in the car (or at the sodyba) as the "home" node and LoRa gateway. The family gets a web or phone view.
- **Button 1, "Vesk atgal" (take me back):** the LED ring points along *your own breadcrumb trail* back to the car and pulses faster as you get closer. It works with no mobile signal, and it's more reliable than "straight line to the car" because it avoids the bog you walked around.
- **Button 2, "Čia grybai" (mushrooms here):** marks a spot. That is the *reason grandpa carries it every trip*: at home he gets a private map of his spots, by year and by species (a "grybų dienoraštis"). Safety comes for free.
- **Button 3, SOS:** sends the position over LoRa to the car node (a few km in forest [unverified: real range depends on terrain]) or over phone data when there is any.

**The demo.** Live on stage: a volunteer is "lost" in a dark hall (or a pre-recorded walk in a real forest). Their track draws on the screen, and the loops and back-tracking turn it amber. The device buzzes by itself: "Atrodo pasiklydote, vesti atgal?" ("Looks like you're lost, lead you back?"). The LED ring then walks them to the "car". Then show the real pilot map: 10 grandparents, 6 weekends, 300 km of tracks, zero calls to 112.

**What the AI actually does.**
1. **"Am I lost?" detection on the device.** The model learns what a normal foraging track looks like: slow meandering around a home area, returning over time. It flags a lost-person pattern: rising tortuosity, repeated loops, distance from the car still growing after a long time, pace dropping, dusk approaching. It is trained on the pilot's own normal tracks. Lost tracks are simulated by walking and are labelled from published lost-person-behaviour patterns (Koester's ISRID data on lost hikers, including "gatherers" [memory, unverified]).
2. **A probability-of-area map for rescuers.** When SOS fails (flat battery or no signal), the last known point plus terrain (forest roads, bogs, rivers from OpenStreetMap/GIS) produces a search-probability heatmap like those that professional search and rescue uses. Police already fly drones over large forests [verified: 15min], so a ranked search area helps them.
3. Optional: a "turn back now" nudge that combines distance, walking speed and sunset time.

**Who uses it repeatedly, and scale.** Pickers go every weekend from August to October, and berry pickers in summer. Grandchildren give it to grandparents, which is the natural gift. Scale routes: municipalities or the police lending units at forest car parks, seniors' organisations, hunters' clubs, and the same device for orienteering or hiking clubs and for dementia-wandering families. The data (anonymised) shows where people get lost: which forests, which features.

**Proven model abroad.** Personal locator beacons and satellite messengers (Garmin inReach) exist but cost hundreds of € plus subscriptions and are too complex for a 70-year-old [memory]. Koester's lost-person behaviour and probability-of-area methods are standard SAR practice [memory, unverified]. Meshtastic LoRa off-grid messaging is proven hobby tech [memory]. Nobody has packaged a senior-proof mushroom picker's beacon with a spot diary [not checked in detail; the search showed none].

**LT hook.** Mushroom picking is a national ritual. Over 100 lost-picker call-outs a year, 16 in Kaunas county in August alone, and pickers born in the 1950s found by drones near a bog [verified: sources above].

**Pilot by Nov 6?** **Yes, the best timing in this list.** Peak season is right now. Build 10 units in 2–3 weeks. Recruit grandparents through the team's own families and one seniors' club. Collect real tracks in October. Measure: trips, spots marked, "take me back" uses, false lost alerts, and battery life. Also ask the local police commissariat how many picker searches it ran.

**Biggest risk.** A jury may ask "isn't this just GPS?" The answer has to be the senior-proof hardware, the spot diary that makes people carry it, and the proactive lost detection. Second risk: the theme. Pitch it under Sport & tech as "the most popular outdoor activity in Lithuania, made safe for everyone". Round 3 noted that drowning victims are not students; here the users are also not students, but the team's own grandparents are, which is a relatable story.

---

### #2 Erkių radaras + TickBot: measure the ticks, don't just guess them. Σ 12

**What it physically is.** Three layers:
1. **TickBot:** a small RC or autonomous rover (a toy-car chassis) that drags a white flannel flag, the standard 100 m² "flagging" method used by tick ecologists. A camera over the flag (the flag passes under it, or the rover stops every 10 m) and a YOLO-type model **counts ticks and separates nymphs from adults**. The same box logs leaf-litter temperature and humidity.
2. **Microclimate stakes** in the school's local forest: temperature and humidity near the ground, giving a questing-activity index (ticks quest when it is warm and humid enough; "saturation deficit" models [memory, unverified]).
3. **Erkių radaras app:** bite reports in the style of Tekenradar, a daily risk level per area, and a Galaxy Watch geofence nudge: "you were in the forest for 2 h, check for ticks tonight". Removing ticks early lowers Lyme risk [memory, widely stated, unverified here]. For 50–60-year-olds it adds "your TBE vaccine is free since Dec 2025".

**The demo.** TickBot drives across a carpet of fake grass with dozens of sesame seeds and rubber "nymphs" (or preserved real ticks in a sealed tray). The live camera counts them: "23 nymphs per 100 m² = HIGH". The map colours the school's trail red. Then show real October drag data from the local park.

**What the AI actually does.** Real computer vision: counting tiny dark objects on a moving textured cloth and telling ticks from seeds and debris. Plus a forecast model that combines drag counts, bite reports and weather into a daily risk per area, and a model that checks how bite reports line up with the actual drag density.

**Who uses it repeatedly, and scale.** Dog walkers and parents check the daily risk like a weather forecast. Campsites, schools with forest classes and municipal parks departments get objective tick density for mowing and signage. The school tick-census kit (#35) can spread through biology classes nationally. The data feeds NVSC's vaccination campaigns.

**Proven model abroad.** Tekenradar (NL) is a citizen-science tick-bite and tick-activity forecast platform run by Dutch research institutes; it has run for years with many thousands of reports [memory, details unverified]. Flag dragging is the standard ecological method [memory]. There was a research "TickBot" robot in the US that dragged permethrin cloth [memory, unverified].

**LT hook.** Highest TBE incidence in Europe: 807 cases and 11 deaths in 2024, 30.5/100k among the unvaccinated, and slow vaccine uptake [verified: NVSC, PMC12452677].

**Pilot by Nov 6?** **Partly.** Ticks keep questing in mild October weather [unverified: exact temperature thresholds], so the team can do real drags in the first half of October (with gloves and permethrin-treated clothing) and a survey of bites in their school. By November activity drops, so drag data will be thin.

**Biggest risk.** Round 3's objection that "the fix is vaccination". The counter: vaccine uptake is the problem, and Lyme has no vaccine. Second risk: handling ticks is a health issue, so the team needs a biology teacher's supervision. Third: the WANT depends on people opening a map, which is weaker than a device they carry.

---

### #3 Poledinis: the ice fisher's bite alarm that measures the ice. Σ 12

**What it physically is.** An evolution of the ice seed. Instead of buoys that nobody maintains, a **tip-up bite alarm** (fishers already set several over holes) whose stem is a **thermistor string**: DS18B20 sensors every 2 cm, the SmartICE principle. When it sits in the hole, the temperature profile shows the ice–water boundary and so the thickness, and whether there is a slush layer. A line-tension or flag sensor sends **bite alerts to the phone**; that is the reason fishers buy it. Every hole uploads GPS, thickness and water temperature to a shared map. Variant #6 is a clip-on for the ice auger that detects break-through.

**The demo.** A clear tub of ice grown in a chest freezer, with dyed layers of clear ice and snow-ice. Drill a hole on stage, drop in the tip-up, and the phone shows "9 cm, snow-ice on top, slush layer: fine for one person, not for a group". Pull the line: "Bite! Hole 3". The national map lights up with simulated holes.

**What the AI actually does.**
1. Reads the ice–water boundary and slush layers from noisy temperature profiles.
2. **Interpolates from the scattered holes to the whole lake** using Stefan's-law growth (thickness ∝ √freezing degree-days), calibrated per lake from real holes. Published calibrated models reach an RMSE of about 2.3 cm [verified in round 2: PLOS One / Water 2022, see deep-dives/03-ice-safe.md]. It flags anomalies: a stream inflow or thaw forecast next to a thin reading turns the zone red. The drowning near a stream inflow is exactly this pattern [verified: search snippet, the Grendavė case].
3. Later: Sentinel-1 ice-on detection for lakes with no holes (#29).

**Who uses it repeatedly, and scale.** Ice fishers go out every winter weekend. The more fishers, the better the map (network effects). PAGD could use it for warnings, and the national fishing association and fishing-gear shops could distribute it. Skaters benefit from the same map.

**Proven model abroad.** SmartICE (Canada): thermistor-chain SmartBUOYs frozen into sea ice, plus a sled-towed sensor, giving Inuit communities travel-safety maps [memory; deep-dives/03 cites smartice.org]. Sweden's Skridskonätet crowd-reports ice for tour skaters [memory].

**LT hook.** PAGD's 7/12 cm rule, compulsory ice picks for ice fishers, and an early-season fisher drowning in the news every winter [verified: AM, LRT, tv3].

**Pilot by Nov 6?** **No field pilot.** Lithuanian lakes normally freeze in December or later [unverified]. What can be done: a freezer ice-growth test that validates the thermistor thickness against a ruler and tests the model; interviews with 10–20 fishers at a gear shop or a fishing-club meeting; and a back-test of Stefan's law on past winters using weather data and news reports. A real pilot would come in Dec–Feb, between the Baltic final and next season.

**Biggest risk.** Liability ("your map said green"). Mitigate by showing only "measured here, at this time" and by never showing green alone. And the timeline: the demo is lab-only, and the jury knows ice doesn't exist in November. Round 3 red team killed ice for exactly this reason. It is stronger than the buoys, but the season problem remains.

---

### #5 Obuolių radaras: garden fruit rescue powered by teen bike crews. Σ 12

**What it physically is.** An app plus a cheap kit. A sodyba owner or grandparent photographs an apple tree (or the team does it on visits). **AI counts the apples in the photo and estimates the kg and the picking window**, then publishes a pin: "≈120 kg Antonovka, pick within 10 days, free". Collectors claim it: juice presses, food banks, animal farms, school canteens, families. A route planner builds weekend "harvest rides" for teen crews on bikes with trailers. A €5 fruit-drop counter under a tree is optional.

**The demo.** Hold a phone up to a real apple branch (or a photo of a tree) on stage: "143 apples ≈ 21 kg". Show the live map of the pilot district, and a jar of juice pressed from rescued fruit with its kg-saved counter.

**What the AI actually does.** Apple detection and counting under occlusion, then a correction from visible to total fruit (calibrated by picking and weighing pilot trees), then a kg estimate. It matches supply to collectors' minimums (a press needs at least X kg) and plans the routes.

**Who uses it repeatedly, and scale.** Every autumn, the same trees and the same people; it's a seasonal habit like the deposit system. Municipalities, food banks and school eco-clubs, then Latvia and Estonia (same sodyba culture). It also covers plums, pears and berries.

**Proven model abroad.** Mundraub (DE) and Falling Fruit (global) public fruit maps; UK community fruit-harvesting projects [memory, unverified]. Apple counting from images is well studied, for example with the MinneApple dataset [memory].

**LT hook.** Sodybos and grandparents' orchards, and the autumn "we don't know where to put the apples" [unverified as a statistic; common experience]. Garden fruit waste is **not** quantified [gap].

**Pilot by Nov 6?** **Yes.** Apple harvest runs from September into October. Weigh 20 trees and compare with the AI estimate, and run 3–4 harvest rides.

**Biggest risk.** WOW and "AI doing real work" are only medium, and it risks looking like "a food-waste app" (seen). Tonnage impact is small unless partners join.

---

### #4 Ruonis: the cold-water swimmer's guardian. Σ 11

**What it physically is.** A waterproof pod (ESP32, IMU, water-temperature and skin-temperature probes, a vibration motor and a bright LED) clipped to the goggle strap or to the tow float that open-water swimmers already use. Buoy version: the float carries LoRa and a buzzer.

**The demo.** A volunteer puts a hand and forearm into an ice bath on stage. The countdown shows a personalised safe time and buzzes. Then a video of a real swim: the stroke rate fades, and the pod buzzes "OUT" before the swimmer notices.

**What the AI actually does.** It learns each swimmer's normal stroke rhythm and detects the **early fade** (slower strokes, shorter glide, erratic head position) that comes before cold swim failure. It combines that with water temperature, time in the water and the swimmer's own acclimatisation history to predict a safe remaining time. If the swimmer stops moving, it sends an alarm.

**Who uses it repeatedly, and scale.** Club and solo cold-water swimmers use it weekly from October to March. Triathlon clubs and open-water events can use it too, and the buoy version suits beaches and lakes.

**Proven model abroad.** Research on cold shock and swim failure (Tipton's "float first" work; Giesbrecht's 1-10-1 rule) [memory, unverified]. Consumer swim watches track strokes, but none watches for swim failure in cold water [not checked].

**LT hook.** Lithuania's drowning rate is among the EU's highest [verified in round 3: LRT/Eurostat]. The winter-swimming ("ruoniai") club scene [unverified]. Weaker hook than #1–#3.

**Pilot by Nov 6?** **Yes.** Water is cooling through October and November, so the team can recruit one winter-swimming club and collect stroke data.

**Biggest risk.** A niche user base (Big = 1). The prediction is a safety claim, so a physiologist or sports-medicine partner is needed. Real LT drowning victims (drunk middle-aged men) are not the users.

---

## 3. Short summary

- **Best new find: BackTrack (Σ 13).** Police get 100+ lost-mushroom-picker call-outs a year, with drones and dog teams deployed [verified]. A senior-proof LoRa clip combines a spot diary (why people carry it), "take me back" without signal, and on-device "you look lost" detection. **It can be piloted right now, in peak season.** This is the idea from this lens that best passes WANT + WOW + NOT-SEEN + a pilot before Nov 6.
- **Seed 1, ice: improved but still season-blocked.** The better design is **Poledinis**, a fisher's bite-alarm tip-up that measures the ice at every hole (crowd-sensing among the actual victims), not buoys. There is no ice before Nov 6, so the demo is lab-only.
- **Seed 2, ticks: survives only with hardware.** A map-only app is a wrapper, but **TickBot** (a flag-dragging rover with AI tick counting) plus a microclimate model plus nudges is novel and demo-able. LT facts: 807 TBE cases and 11 deaths in 2024, 30.5/100k among the unvaccinated, and slow uptake [verified]. Field drags are possible in early October only.
- **Killed by search:** a mushroom *forecast* app. Boletus already covers Lithuania.
- **Sustainability option:** Obuolių radaras (AI apple counting plus teen harvest rides; pilot now), but it's medium on WOW.
- **Gaps:** national TBE vaccination coverage %, the number of ice-specific deaths per season, garden-fruit waste volume, Tekenradar and SmartICE details (from memory).

## Sources (5 searches)
- Lost mushroom pickers: [klaipeda.diena](https://m.klaipeda.diena.lt/naujienos/klaipeda/nusikaltimai-ir-nelaimes/tikras-galvos-skausmas-grybautojai-miskuose-iesko-grybu-o-policija-grybautoju-1040204) · [kauno.diena](https://m.kauno.diena.lt/naujienos/kaunas/nusikaltimai-ir-nelaimes/skambina-pavojaus-varpais-vien-rugpjuti-kauno-apskrities-miskuose-pasiklydo-16-zmoniu-1041404) · [15min](https://www.15min.lt/naujiena/aktualu/nusikaltimaiirnelaimes/sezoninis-kriminalas-vyrai-ieskojo-grybu-vyrus-surado-dronai-59-2771040) · [rinkosaikste](https://rinkosaikste.lt/pasiklydusiai-grybautojai-i-pagalba-skubejo-policininkai-kinologas-ir-ugniagesiai-naujas/) · [tv3](https://www.tv3.lt/naujiena/lietuva/gelbejimo-operacija-is-arti-skelbia-vaizdus-surasti-pasiklyde-grybautojai-n1554166)
- TBE: [NVSC](https://nvsc.lrv.lt/lt/uzkreciamuju-ligu-valdymas/erkinis-encefalitas-lietuva-endemine-teritorija-taciau-lietuviai-skiepijasi-vangiai/) · [ulac.lt](https://ulac.lt/nemokami-skiepai-nuo-encefalito-2026-m-kas-juos-gaus/) · [PMC12452677](https://pmc.ncbi.nlm.nih.gov/articles/PMC12452677/) · [IJID 2025](https://www.sciencedirect.com/science/article/pii/S1201971225002747)
- Ice: [AM](https://am.lrv.lt/lt/naujienos/zvejyba-ant-ledo-ka-reikia-zinoti-zvejams/) · [LRT](https://www.lrt.lt/naujienos/lietuvoje/2/1306472/gelbetojai-ispeja-poledinei-zuklei-dar-per-anksti-del-plono-ledo-jau-nuskendo-vienas-zvejys) · [tv3](https://www.tv3.lt/naujiena/lietuva/traku-rajone-nuskendo-ant-ledo-iluzes-zvejys-n1321242) · [alkas](https://alkas.lt/2023/12/05/ugniagesiai-ledas-dar-plonas-ir-nesaugus/)
- Mushroom forecast prior art: [Boletus](https://boletusmap.eu/) · [ShroomCast](https://shroomcast.net/) · [mushboom](https://github.com/bialasky/mushboom) · [Waldschatzfinder](https://www.waldschatzfinder.de/)
