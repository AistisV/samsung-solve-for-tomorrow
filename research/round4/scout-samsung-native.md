# Scout: Samsung-native ideas (round 4)

Angle: ideas where Samsung technology fits naturally (Galaxy phones, old Galaxy phones, SmartThings, Galaxy Watch sensors, Samsung's own sustainability story) **and** that pass the 9-point winning formula in `BRIEF.md`. Anything that only uses Samsung for name-dropping was dropped.

Search budget used: **20 / 20 WebSearch calls**. Every claim is tagged `[verified: source]`, meaning a search snippet or primary page stated it, or `[unverified]`.

---

## 0. Samsung tech a school team can actually use

| Tech | What it does | Can a school team use it? | Link |
|---|---|---|---|
| **Samsung Health Data SDK** (replaces the Samsung Health SDK for Android, deprecated 31 Jul 2025) | Reads a user's Samsung Health data: steps, exercise, heart rate, sleep and more. | **Yes, for a prototype.** Developer mode lets you *read* data with no partner request. Writing data or publishing the app needs Samsung partner approval (package name + SHA-256 registration). [verified: developer.samsung.com/health/data] | https://developer.samsung.com/health/data · https://developer.samsung.com/health/data/guide/developer-mode.html |
| **Samsung Health Sensor SDK** (Galaxy Watch4 and later) | Raw accelerometer at 25 Hz, PPG and ECG, plus processed heart rate, SpO2, skin temperature, EDA, body composition (BIA) and sweat loss. | **Yes, in the Health Platform's developer mode.** Distributing the app needs the Samsung Partner Program. Official codelabs exist (heart rate + SpO2, skin temperature, EDA). [verified: developer.samsung.com/health/sensor] | https://developer.samsung.com/health/sensor/overview.html · https://developer.samsung.com/codelab/health/blood-oxygen-heart-rate.html |
| **SmartThings API + SmartThings Energy** | Controls and reads devices through a cloud REST API, including power and energy readings from compatible smart plugs. Edge drivers (Lua) run on the hub. | **Yes.** A Personal Access Token is enough for a prototype, but tokens created after 30 Dec 2024 **expire after 24 h**, so a long pilot needs an OAuth SmartApp or daily token refresh. [verified: developer.smartthings.com] Samsung recommends the Edge Device Builder over custom drivers. [verified: same] | https://developer.smartthings.com/docs/getting-started/quickstart · https://developer.smartthings.com/docs/getting-started/authorization-and-permissions |
| **SmartThings AI Energy Mode** (Samsung's own proof point) | Samsung's study of ~187,000 washers in 126 countries (Jul 2024–Jun 2025) found **5.02 GWh saved, about 30%** of their consumption. [verified: Gizmochina / SammyGuru, Dec 2025] | Useful as a *citation* ("Samsung's own data shows AI + feedback saves energy"), not as an API. | https://www.gizmochina.com/2025/12/15/samsung-smartthings-ai-cuts-power-use-by-30-percent/ |
| **Galaxy Upcycling at Home** | Turns an old Galaxy phone (S9 / Note9 or newer, Android 8.1+) into a SmartThings sound sensor (baby crying, dog, knock) or light sensor. [verified: 9to5google, Samsung US newsroom] | **Partly.** It launched as a beta in the US, UK and Korea only [verified: same]. We found no sign of it in LT. **Our approach:** follow Samsung's concept but write our own Android app for old Galaxy phones, which is fully doable. iFixit criticised the programme for being too limited [verified: iFixit headline], so we can say we are "finishing Samsung's idea". | https://news.samsung.com/us/samsung-galaxy-upcycling-programrepurpose-galaxy-smartphones-smart-home-devices/ |
| **Galaxy Upcycling: EYELIKE** | Old Galaxy phone + lens + AI used as a retinal (fundus) camera. It served **19,000+ people in Vietnam**, with 90 devices supplied in 2019. [verified: Samsung Newsroom] | This is inspiration showing that Samsung *itself* markets old phones + AI as social good. It is not an API. | https://news.samsung.com/global/samsungs-eyelike-fundus-camera-repurposes-galaxy-smartphones-to-improve-access-to-eye-care |
| **Galaxy Watch Running Coach** (Watch8, 2025) | A 12-minute run assessment gives a 1–10 score using heart rate, VO2 max, pace and six running-form metrics (asymmetry, ground contact time, etc.). [verified: Samsung US newsroom, etnews] | This is a consumer feature, not an SDK. It is good for pitch framing. We would reimplement a simple version with the Sensor SDK. | https://news.samsung.com/us/samsung-health-galaxy-ai-offer-personalized-training-tools-for-your-race-this-fall/ |
| **On-device AI on Galaxy: ML Kit GenAI / Gemini Nano** | On-device summarise, rewrite and proofread, plus a Prompt API (alpha, Oct 2025) for custom multimodal prompts. It works offline. Galaxy S25 / S25+ / S25 Ultra are supported devices. [verified: developers.google.com/ml-kit/genai] | **Yes**, if the team has access to an S25-class phone. Note that it is Google's API running on Galaxy. We found no public "Galaxy AI" SDK in our searches [unverified]. For older phones, use TensorFlow Lite / MediaPipe models instead [unverified: standard practice]. | https://developers.google.com/ml-kit/genai |
| **Galaxy for the Planet** | Samsung says it met its 2025 goals: recycled materials, no single-use plastic in packaging, charger standby power **< 0.005 W**, Zero Waste to Landfill. It has new goals through 2030. [verified: Samsung Mobile Press] | This is pitch framing: "Samsung cut *its* chargers' standby to near zero; we help schools and homes find the rest." | https://news.samsung.com/global/samsung-expands-its-journey-galaxy-for-the-planet-with-new-goals-through-2030 |

**Practical note.** The Health SDKs and SmartThings are prototype-friendly, and a live stage demo in developer mode is fine. Wide distribution (a Play Store release) would need a Samsung partnership. That is a good line for the development plan: "Next step: Samsung Partner Program". Samsung SmartThings Find / SmartTag was considered but not researched. Its only natural use is lost-item tracking, which does not fit either theme.

---

## 1. Idea table (24 ideas, scored 0–2 on the 9 formula points; max 18)

Columns: **R** = relatable in 10 s · **T** = team authenticity · **P** = proven model · **W** = working prototype in 6 weeks · **AI** = AI/IoT naturally at the core · **Pi** = mini-pilot by 6 Nov · **Re** = audience + reach · **Im** = one impact number · **LT** = Lithuanian hook.

| # | Idea | Samsung tech | R | T | P | W | AI | Pi | Re | Im | LT | **Σ** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **Oro sargas (Air Guard)**: an old Galaxy phone + a €20 CO2 sensor on the classroom wall. AI predicts "you will hit 1,500 ppm in 8 min" and tells the class *when* and *how long* to open the windows (short burst, not all lesson), balancing fresh air against heat loss. | Old phone (Upcycling concept), SmartThings (window contact / plug), on-device ML | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | **18** |
| 2 | **Energijos detektyvai (Energy Detectives)**: SmartThings smart plugs + an energy dashboard for the school. AI learns the "empty school" baseline and flags night and weekend waste (projectors, PCs, vending machines). Savings are split 50/50 with the municipality. | SmartThings API + Energy, old phones as hallway displays | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 1 | **17** |
| 3 | **Širdies ritmo kūno kultūra (Heart-rate PE)**: Galaxy Watch HR per student in PE. The grade is based on minutes in *your* personal heart-rate zone, not on who runs fastest, so unfit kids can earn a top grade for effort. | Galaxy Watch + Health Sensor SDK, Health Data SDK | 2 | 2 | 2 | 2 | 1 | 2 | 2 | 2 | 2 | **17** |
| 4 | **Stalčiaus telefonai → gamtos sensoriai (Drawer phones → nature sensors)**: a school collects old phones, and each becomes a solar-powered schoolyard/park bird-sound station (BirdNET-style AI). Results feed a school biodiversity map. | Old Galaxy phones (Upcycling + RFCx model), on-device audio AI | 1 | 2 | 2 | 2 | 2 | 2 | 1 | 1 | 2 | **15** |
| 5 | **Vampyrų medžioklė (Vampire Hunt)**: students take home a SmartThings plug kit for a week. AI names each family's biggest standby "vampire" and estimates €/year. | SmartThings plugs + API, Gemini Nano report | 2 | 2 | 1 | 2 | 1 | 2 | 2 | 2 | 1 | **15** |
| 6 | Heart-rate PE lite: 5 watches rotated per class, plus an AI "effort report" to parents instead of a sprint-time grade (a cheaper variant of #3) | Galaxy Watch, Health Data SDK | 2 | 2 | 2 | 2 | 1 | 2 | 1 | 1 | 2 | 15 |
| 7 | Old-phone smoke watch: a phone camera in a private-house district plus a PM sensor. AI detects chimney smoke episodes (wet wood or burning waste) and sends an anonymous heat-map to the municipality. | Old phone camera + vision AI | 1 | 1 | 1 | 2 | 2 | 1 | 1 | 1 | 2 | 12 |
| 8 | School "second-life phone library": repair and wipe donated phones, lend them to kids without phones, and have AI grade battery and screen health | Samsung repair mode, battery diagnostics | 1 | 2 | 1 | 1 | 1 | 1 | 1 | 1 | 2 | 11 |
| 9 | Canteen waste camera: an old phone over the tray-return. AI estimates the plate waste per dish. | Old phone + vision | 2 | 2 | 2 | 2 | 2 | 2 | 1 | 2 | 1 | 16* |
| 10 | Running-form coach for school runners using the watch's 6 form metrics | Health Sensor SDK accel | 1 | 2 | 2 | 1 | 2 | 1 | 1 | 1 | 1 | 12 |
| 11 | Heat/dehydration alert for summer sports camps (watch sweat loss + skin temperature) | Sensor SDK | 1 | 1 | 1 | 1 | 2 | 0 | 1 | 1 | 0 | 8 |
| 12 | Grandparent fall-detection + inactivity alerts for rural elderly | Galaxy Watch fall detection, SmartThings | 2 | 1 | 2 | 2 | 1 | 1 | 1 | 1 | 1 | 12 (off-theme) |
| 13 | Solar-surplus scheduler: SmartThings runs the washer or boiler when the school or home solar is peaking | SmartThings Energy | 1 | 1 | 2 | 1 | 2 | 1 | 1 | 1 | 2 | 12 |
| 14 | Classroom lights-left-on detector: an old phone's light sensor + a motion sensor, with AI alerts after the last lesson | Old phone light sensor (the actual Upcycling feature) | 2 | 2 | 1 | 2 | 1 | 2 | 1 | 1 | 0 | 12 |
| 15 | Sleep-and-grades study: Galaxy Watch sleep data vs self-reported focus among 30 students, with an AI sleep nudge | Health Data SDK (sleep) | 2 | 2 | 1 | 2 | 1 | 2 | 1 | 1 | 1 | 13 (off-theme unless framed as sport/health) |
| 16 | Dog-walk / e-scooter vs car school-run tracker | Galaxy phone | 2 | 1 | 1 | 2 | 0 | 1 | 1 | 1 | 2 | 11 (close to rejected "points app") |
| 17 | Sound-level "quiet library/canteen" monitor (old-phone mic) | Upcycling sound sensor | 2 | 2 | 1 | 2 | 1 | 2 | 1 | 1 | 0 | 12 (not on-theme) |
| 18 | AI repair helper: point the phone camera at a broken device and get repair steps plus nearest repair café | Gemini Nano (multimodal Prompt API) | 1 | 1 | 1 | 1 | 2 | 1 | 1 | 1 | 1 | 10 |
| 19 | Textile-bin fill-level sensor from an old phone | Old phone camera | 1 | 1 | 1 | 2 | 1 | 1 | 1 | 1 | 2 | 11 |
| 20 | Home heating "window open while radiator on" alert via SmartThings contact sensor + temperature | SmartThings | 2 | 1 | 1 | 2 | 1 | 1 | 1 | 1 | 1 | 11 (fold into #1) |
| 21 | Adaptive PE for kids with disabilities: watch HR keeps effort safe and fair | Sensor SDK | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 2 | 10 |
| 22 | Ice-rink / pool water-heating energy monitor for sports facilities | SmartThings Energy | 0 | 0 | 1 | 1 | 1 | 0 | 1 | 1 | 1 | 6 |
| 23 | Old phone as a nest-box camera for school ornithology, with AI species ID | Old phone camera | 2 | 2 | 2 | 1 | 1 | 1 | 1 | 0 | 1 | 11 |
| 24 | Standby-power "phone-charger audit" (chargers left plugged in) | SmartThings plug | 1 | 1 | 0 | 2 | 0 | 2 | 1 | 1 | 0 | 8 (too trivial) |

\* #9 scores high, but canteen food waste is the **Minova-2022 memory** (`past-winners.md` pattern 6) and is covered by other scouts, so it is out of scope for this Samsung angle.

Dropped as tech wrappers: "Galaxy AI chatbot for recycling questions", "SmartThings points for turning lights off" (a gamified points app, which the team rejected), and "watch step challenge" (rejected).

---

## 2. Top profiles

### #1 Oro sargas (Air Guard): upcycled Galaxy phones that tell your class when to open the window (Σ 18)

**Pitch.** "Every student knows that 6th-lesson sleepiness. We measured it: it's CO2. Oro sargas is an old Galaxy phone on the classroom wall that tells you exactly when and how long to open the window, so you get fresh air without wasting heat."

**Relatable problem + LT evidence**
- Lithuanian studies found classroom CO2 averaging about 1,400 ppm, with lessons reaching **3,000–4,000 ppm**. The highest reading in one Vilnius school was **5,152 ppm against a 1,500 ppm norm**. Schools rely on natural ventilation, and none of the schools studied had a dedicated ventilation system. [verified: emokykla.lt "Tyrimas: Lietuvoje vaikai mokyklose kenčia nuo deguonies trūkumo"; sildymas-vedinimas.lt]
- KTU researchers warn that renovated (insulated) schools need ventilation too, because insulation without ventilation traps air. [verified: headline, vaistines.lt / n9.lt]
- A Berkeley Lab-led study found that in classrooms **above 1,000 ppm, children miss 10–20% more lessons**. [verified: as quoted in the emokykla.lt snippet]
- There is also a sustainability angle. In winter, windows left open all lesson waste heating. The usual guidance is short "burst" ventilation. [unverified: common heating advice; verify with a Lithuanian source]

**Proven model abroad**
- CO2 "traffic lights" (e.g. Germany's CO2-Ampel, COVID-era schools). A controlled study used green < 1,000, yellow 1,000–2,000 and red ≥ 2,000 ppm. Visual alarms cut CO2 by **19.5%**, and ventilation protocols cut the time above 1,000 ppm **from > 90% to < 10%**. Researchers stress that sensors alone fail without behaviour change. [verified: ScienceDirect "IoT-driven acoustic and visual CO2 feedback system" 2025; NCCEH evidence review] https://www.sciencedirect.com/science/article/abs/pii/S0048969725011842 · https://ncceh.ca/resources/evidence-reviews/pandemic-experiences-manual-ventilation-and-carbon-dioxide-co2-sensing
- Samsung's own Galaxy Upcycling turns old phones into home sensors (US/UK/KR beta) [verified]. We bring the idea to schools in LT.

**What the prototype is (the 2-minute stage demo)**
- An old Galaxy phone in a 3D-printed wall frame, with a Bluetooth or USB CO2 sensor (e.g. SCD40 on an ESP32) and optionally a SmartThings window contact sensor.
- On stage: a team member breathes into a jar or bag over the sensor. The screen goes yellow, then red, and the phone says "Open 2 windows for 4 min. Fresh air in 3 min, heat loss ~X kWh." When the jar is lifted the level drops, and the AI shows the countdown. A second screen shows a live dashboard of the pilot classrooms over the last 3 weeks.

**How AI/IoT is used and why it helps**
- **Prediction, not a threshold.** A small regression model uses the CO2 slope, number of students (from the timetable) and room volume to predict the minutes until 1,500 ppm, so the alert comes *before* the fog.
- **Optimal airing time.** It learns from each room's past decay curves how long a burst is needed, depending on outdoor temperature (weather API). This is the energy-saving part.
- **Weekly teacher summary.** It uses on-device Gemini Nano on an S25-class phone, or a cloud LLM: "Room 214 was in the red 38% of lesson time; best improvement: open during breaks."
- IoT: phone + sensor + optional SmartThings contact sensor → cloud dashboard for the school administration.

**Mini-pilot by 6 Nov (6 weeks)**
- Week 1–2: build 3 units from teachers' and families' drawer phones.
- Week 3: 1 week baseline with the display hidden, in 3 classrooms.
- Week 4–5: display on, measuring the before/after % of lesson time above 1,000 and 1,500 ppm.
- Add a 200-student survey ("do you feel sleepy in lesson X?") and a letter from the school director. This is heating season, so the timing is perfect.

**Target audience and reach**
Lithuanian schools, owned by municipalities. There are two routes to reach them:
- the municipal education department, since the kit is €30–40 per classroom plus a donated phone [unverified: component-price estimate];
- the school's own old-phone collection drive, which gives every student a role.

It could scale through the NVŠ/technology teachers' network or a municipal "green schools" programme.

**The one impact number**
"% of lesson time above 1,500 ppm: from X% to Y% in our school". Target −50% relative, based on the 19.5% / >90%→<10% evidence. The secondary number is phones rescued from drawers. 53% of Lithuanians keep old phones in a drawer and only 9% recycle them [verified: LRT via local-data.md].

**Top 3 jury objections**
1. *"CO2 monitors already exist; buy one for €50."* Yes, and our research shows that monitors alone don't change behaviour. The value is prediction, the burst-length advice that saves heat, and reusing phones that sit in drawers. We are adapting a proven model rather than inventing one.
2. *"Opening windows in a Lithuanian winter wastes energy."* That is exactly why the AI times short bursts. We show kWh estimates alongside ppm. The same fresh air with less heat loss is the sustainability angle.
3. *"Is this sustainability or health?"* Both. It is "living more sustainably" in buildings, and it upcycles e-waste. Samsung runs this same upcycling idea, and we bring it to Lithuanian classrooms.

---

### #2 Energijos detektyvai (Energy Detectives): students find their school's hidden energy waste with SmartThings (Σ 17)

**Pitch.** "Our school uses electricity at 3 a.m. when nobody's there. We built a SmartThings-based detective kit that shows where, and a 50/50 deal so the school keeps half of what it saves."

**Relatable problem + LT evidence**
- Standby power is **3–10% of residential electricity** in estimates across countries (8% UK 2004, 7% France, 7% Spain). [verified: Wikipedia "Standby power" / One Watt Initiative; Euronews]
- Kaunas has put solar plants on **72 school and kindergarten roofs**, with 13 more planned. [verified: kaunas.lt, Jul 2025] Municipalities care about school energy, but schools don't see their own data. [unverified: needs confirmation from our school's facilities manager]
- Kaunas district cut lighting electricity by more than half by switching fixtures. [verified: kasvyksta.lt snippet]
- Ignitis runs an energy-efficiency education programme in schools, which could be a potential partner. [verified: ignitis.lt snippet]

**Proven model abroad**
- **Energy Sparks (UK)**: 1,000+ schools and 500,000+ pupils. Among schools that cut use, the average change was **−19% gas and −9% electricity**. An average secondary saves ≥ £12,000 and 48 t CO2 a year. [verified: Transition Bath / energysparks.uk]
- **Euronet 50/50**: 500+ schools. Schools keep 50% of the savings and the municipality keeps 50%. Savings were at least 8%. In one region, 67% of schools saved, averaging 11.6%. [verified: interregeurope.eu, euronet50-50max.eu] We found no evidence of Lithuanian participation [unverified gap], which makes this a "first in Lithuania" angle.
- **Samsung's own AI Energy Mode** saved about 30% on 187k washers. [verified]

**Prototype and demo**
10 SmartThings-compatible Wi-Fi energy plugs on the biggest suspects (staff-room fridge, vending machine, printer, projectors, PC lab strip), SmartThings API → a web dashboard, and an old Galaxy phone in the hallway as a public "energy mirror".

On stage:
- plug a kettle or lamp into a SmartThings plug, and the dashboard spikes live;
- the AI anomaly panel shows a real pilot finding, for example "Printer room: 140 W all weekend = €X/yr";
- tap "switch off at 18:00" as a SmartThings automation.

**AI/IoT**
- Anomaly detection learns each device's normal "occupied vs empty" profile and flags night and weekend base-load.
- An LLM turns the findings into a weekly one-paragraph report for the director and a class-by-class challenge.
- IoT: SmartThings plugs, cloud API and automations. Note the PAT 24 h expiry, so use an OAuth SmartApp or refresh the token. [verified]

**Mini-pilot by 6 Nov**
2 weeks of baseline, then 2 weeks of actions (auto-off automations + student "energy patrol"), giving a before/after kWh and € for the plugged devices. Also get the school's monthly bill from the facilities manager, and a letter from the director or municipality about a 50/50 pilot.

**Audience and reach**
Schools and their municipal owners. The 50/50 split gives the municipality a reason to roll it out. Possible partners are Ignitis education and the Kaunas "Žaliasis kursas" programme.

**Impact number**
"kWh (and €) our school wastes when empty, cut by X%". The benchmark is Energy Sparks at −9% electricity.

**Objections**
1. *"Energy Sparks already does this."* Yes, and it works (−9% electricity). No Lithuanian version exists that we know of, and ours is plug-level, so it names the *specific* culprit.
2. *"10 plugs is tiny vs heating."* Heating is the municipality's job. The plugs are the student-controllable part, and the 50/50 model scales to meters later.
3. *"Is the AI necessary?"* Without it you get 10 graphs nobody reads. The AI turns them into "3 things to switch off tonight".

---

### #3 Heart-rate PE: grade the effort, not the sprint (Σ 17, sport option)

**Pitch.** "In PE, the fast kids get the 10s and the rest give up and get sick notes. We used Galaxy Watch heart-rate sensors so that everyone is graded on effort in *their own* heart-rate zone."

**Relatable problem + LT evidence**
- Only **about 5%** of Lithuanian grade 9–13 students get enough daily activity, among the 5 least active countries in Europe. [verified: local-data.md / HBSC via MadeinVilnius]
- Doctors report kids asking for "preparatory group" certificates to avoid running and push-ups. [verified: local-data.md, tv3.lt / ve.lt]
- More than 50% of non-sporty kids "don't see the point". [verified: local-data.md, NSA]

**Proven model abroad**
**Naperville, Illinois.** Since the 1990s ("Learning Readiness PE"), students have been graded on time in their target heart-rate zone (150–185 bpm) using Polar GoFit monitors, with HR shown live on an iPad. [verified: naperville203.org, iphionline.org case study, ihtusa.com] It is a well-known, widely copied model.

**Prototype and demo**
A Galaxy Watch app (Health Sensor SDK in developer mode, continuous heart rate) streams to a teacher's Galaxy tablet or phone dashboard. Each student's tile shows their personal zone, which the AI calibrates from resting HR and age.

On stage: a team member does 30 seconds of jumping jacks and their tile moves from blue to green. The end-of-class report shows "Minutes in zone: 18/20 → grade 10" for a non-athlete versus a sprinter who coasted.

**AI**
- Personal zone calibration and fatigue/recovery estimates (like Samsung's own Running Coach).
- Anomaly detection for dangerously high HR.
- An LLM summary per student for parents.

**Mini-pilot**
3–5 Galaxy Watches (borrowed or from Samsung devices) rotated through 2 PE classes over 3 weeks. Measure the average % of class time in the moderate-to-vigorous zone, and survey motivation before and after (n ≈ 50).

**Reach**
PE teachers and schools, through LSU (Sports University) or the national PE teacher network. The Samsung device prize would fund class kits.

**Impact number**
"% of PE lesson spent in the heart-healthy zone, and the number of pupils who stop seeking exemptions".

**Objections**
1. *Cost of watches* → rotate 5 per class, and use cheap BLE straps as a fallback.
2. *Privacy of health data* → developer mode, on-device only, no names on the teacher view, parental consent.
3. *"Isn't this a wearable points app?"* No points and no steps. It changes the *grading rule* in PE, which is a policy change the jury can take to the ministry.

**Caveat.** The team prefers sustainability, and this is sport. It is the strongest Samsung-native sport option because the Watch is essential to the idea, not decoration.

---

### #4 Stalčiaus telefonai → gamtos sensoriai (Drawer phones → nature sensors) (Σ 15)

**Pitch.** Collect the school's drawer phones and turn each into a solar-powered bird-song station in parks and schoolyards. On-device AI identifies species and builds a live biodiversity map for the town.

**Evidence**
- 53% of Lithuanians keep old phones in a drawer and 9% recycle them. [verified: LRT via local-data.md]
- Rainforest Connection upcycles old phones into solar acoustic "Guardians" (about 3 km² coverage each, up to 2 years' run). With Huawei AI, its chainsaw detection reached 96%, and it won the GSMA GLOMO 2021. [verified: huawei.com case pages]
- The BirdNET app had 31 million submissions in 2020, giving 5.8 million quality observations across Europe and North America. It identifies 984 NA/EU species by sound. [verified: PLOS Biology 2022 / Cornell]

**Demo**
Play a blackbird recording and the phone labels it live. The map fills with pilot detections.

**Pilot**
5 phones × 3 weeks. However, October is poor for birdsong [unverified: seasonal assumption], which weakens the pilot numbers.

**Why it ranks lower**
- It is less relatable to a generalist jury.
- The impact number ("species detected") is soft.
- Autumn timing hurts the pilot.
- It is best merged as the *"second life"* of the phones collected for #1.

### #5 Vampyrų medžioklė (Vampire Hunt), home standby hunt (Σ 15)

A one-week take-home SmartThings plug kit. The AI reports each family's biggest standby device and the € per year it costs.
- Evidence: standby is 3–10% of residential electricity [verified], and Samsung's charger standby is < 0.005 W [verified: Galaxy for the Planet].
- Pilot: 20 families.

It works as a **home extension of #2**, not as a standalone idea. The proven model is weaker, and savings per home are small.

---

## Summary / recommendation from this angle

1. **Oro sargas (18/18)** is the best fit.
   - Every juror remembers stuffy classrooms, and it has a strong Lithuanian statistic (5,152 ppm vs 1,500 norm).
   - A proven foreign model exists (CO2 traffic lights: −19.5% CO2, >90% → <10% time over 1,000 ppm).
   - The stage demo is breathing into the sensor.
   - It has a natural Samsung story (Galaxy Upcycling brought to Lithuanian schools, with old phones collected by students).
   - A heating-season pilot is possible before Nov 6.
2. **Energy Detectives (17)** has the strongest proven model (Energy Sparks, Euronet 50/50) and the clearest SmartThings use. It can be merged with #1 into one "classroom guardian" (air + energy).
3. **Heart-rate PE (17)** is the best Samsung-native *sport* option, with the Galaxy Watch essential to it and the Naperville model behind it.

Open verification items:
- the date and sample of the Lithuanian CO2 study (emokykla.lt);
- a Lithuanian source for the burst-ventilation heat-loss claim;
- whether any Lithuanian school joined Euronet 50/50;
- the current SmartThings compatibility of cheap Wi-Fi energy plugs in the EU.
