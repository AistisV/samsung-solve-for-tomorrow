# Judge C: the team that has to build it

**Point of view:** we are 3–5 sixteen-year-olds and one teacher. We have exams, about €100–300, and 6 weeks (Sep 28 → Nov 6). We can write Python and JS, do a little Android, solder, and use ESP32, Arduino, Raspberry Pi and maybe a 3D printer. For each finalist we asked three things. Would we actually enjoy building it? Will it work on stage, first try, in 2 minutes? Can we have real pilot numbers by Nov 6?

**Searches used: 14 of 15.** They were mostly part prices and "has someone already built this?" checks. Tags: [verified: source] means a search result supports the claim. [unverified] means it is our estimate or background knowledge. All prices are for October 2026 orders. Cheap AliExpress parts take 2–3 weeks to ship, so any part the week-1 build needs must come from an EU or LT shop.

---

## 0. Facts that apply to every idea

| Fact | Consequence for us | Tag |
|---|---|---|
| From **Oct 1 2026** the LT heating season officially runs Oct 1 – Apr 30. It can start earlier if the outdoor temperature stays below 10 °C for 3 days. Each municipality decides for its schools. | Heating-season pilots (F1, F2, F4, F5) can start in early–mid October. We should still ask our municipality for the exact date, because the October 2026 weather decides it. | [verified: [kaipkada.lt](https://www.kaipkada.lt/namai-ir-buitis/kada-prasides-sildymo-sezonas-2026-m-lietuvoje-dalis-gyventoju-radiatorius-gali-ijungti-anksciau-239419/), [rinkosaikste.lt](https://rinkosaikste.lt/nuo-spalio-keiciasi-sildymo-tvarka-ka-butina-zinoti-gyventojams/), [vrsa.lt](https://vrsa.lt/titulinio-naujienos/424/vilniaus-rajono-svietimo-ir-gydymo-istaigose-pradedamas-sildymo-sezonas:5351)] |
| Oct 16 (idea form) is in **week 3**. | We need a working breadboard prototype plus one photo or graph *before* Oct 16, so the form shows we're serious. | — |
| Consent | Anonymous surveys and room sensors (no personal data) need only the director's OK. Anything personal needs a parent consent form: heart rate, family showers, home addresses, video of students. Under GDPR, heart rate is *health data*. | [unverified: our understanding of GDPR/school practice; ask the school's data-protection person in week 1] |
| An ESP32 dev board costs about €4–8 | This is the base for almost every build. | [verified: ~$4 AliExpress / $8 Amazon per [Bootloader blog / search summary](https://blog.kylemanna.com/hardware/sniffer-air-quality-monitor-aqi-using-esp32-pmsa003-bme680/)] |

---

## 1. Scores at a glance

Formula points (0–2 each): R relatable · T team authenticity · P proven model · W prototype in 6 weeks · A AI at the core · M mini-pilot by Nov 6 · Au audience/reach · I impact number · L local hook.
**Build** = buildability for us (1–10). **Excite** = how much we'd enjoy it (1–10).

| # | Finalist | R | T | P | W | A | M | Au | I | L | **/18** | Build | Excite | Kit cost (demo + pilot) |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| F1 | Klasės oras (classroom air & heat coach) | 2 | 2 | 2 | 2 | 1 | 2 | 2 | 2 | 2 | **17** | **9** | 6 (8 with the F5 hybrid) | €130–220 for 6 rooms |
| F2 | Energijos detektyvai 50/50 | 1 | 1 | 2 | 2 | 1 | 1 | 2 | 2 | 1 | **13** | 6 | 4 | €120–200 |
| F3 | DušoSargas / ShowerCoach | 2 | 2 | 2 | 2 | 1 | 1 | 1 | 2 | 2 | **15** | 7 | **8** | €200–280 for 8 units |
| F4 | Šilumos detektyvai (thermal camera) | 2 | 2 | 2 | 2 | 1 | 2 | 2 | 1 | 2 | **16** | 8 | 5 | €200–250 (one camera) |
| F5 | Dūmų radaras (smoke radar) | 1 | 1 | 2 | 2 | 2 | 1 | 1 | 2 | 2 | **14** | 8 | 7 | €130–180 for 5 nodes |
| F6 | RecessBox | 2 | 2 | 2 | 1 | 1 | 2 | 2 | 2 | 1 | **15** | 5 | 5 | €200–260 incl. €100 of kit |
| F7 | Traukinukas (walking bus) | 2 | 2 | 2 | 2 | 1 | 1 | 2 | 1 | 2 | **15** | 5 | 6 | €0–60 |
| F8 | HeartSquad (CPR in PE) | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | 2 | **18**\* | 8 | **8** | €100–170 for 3 manikins |
| F9 | Švilpukas ant riešo (whistle wristband) | 2 | 1 | 2 | 2 | 2 | 1 | 1 | 1 | 1 | **13** | 8 | 8 | €60–90 for 3 bands |
| F10 | Pulso kūno kultūra (heart-rate PE) | 2 | 2 | 2 | 1 | 1 | 2 | 2 | 2 | 2 | **16** | 6 | 5 | €150–250 (straps) |

\*F8 gets full formula marks, but the formula has no "theme fit" point. We would lose marks there: "is CPR *sport*?" That is the real risk and it isn't visible in this table (see §2 F8).

---

## 2. Each finalist, as the builders see it

### F1 Klasės oras: classroom air & heat coach (17/18 · build 9 · excite 6)

**Honest gut feeling:** this is the safest project to *win with* and the easiest to finish. It is also the least thrilling to *build*. A "CO₂ traffic light" is a classic Arduino beginner project, and the GitHub search results are full of them [verified: [karlduino/CO2monitorWifi](https://github.com/karlduino/CO2monitorWifi), [ESPHome SenseAir S8](https://vdbrink.github.io/esphome/co2_senseair_s8_sensor.html), [SFeli/ESP32_S8](https://github.com/SFeli/ESP32_S8)]. That's great for feasibility. It is dangerous for the "overused" feeling the team dislikes. What makes it *ours* is the parts on top: the prediction, the "window open while the heating runs" € counter, and ideally the smoke check from F5 (see the hybrid in §5).

**We noticed it ourselves:** the 6th-lesson headache. We can measure our own chemistry room in week 1 and open the pitch with that number. The verified 5,152 ppm Vilnius peak backs it up (scout-teen-green).

**BOM (per classroom node)**

| Part | Price | Tag |
|---|---|---|
| ESP32 dev board | €5–8 | [verified, see §0] |
| CO₂ sensor: **SCD40/SCD41** module, *or* **SenseAir S8** | SCD4x: from €5 on eBay (a clone risk) to $50 for Adafruit/Seeed/SparkFun breakouts. SenseAir S8: about $40 retail, cheaper on AliExpress. | [verified: [eBay €4.99](https://www.ebay.com/itm/403870487186), [DigiKey SCD41 chip $20.54](https://www.digikey.com/en/products/detail/sensirion-ag/SCD41-D-R1/13684000), [karlduino S8 ≈ US$40](https://karlduino.org/CO2monitorWifi/)] |
| WS2812 LED ring (12 LEDs) | €2–4 | [unverified] |
| Reed switch + magnet for the window | €1–2 | [unverified] |
| 3D-printed case, USB PSU, cable | €5–8 | [unverified] |
| **Total per node** | **about €20–35** (€60 with a branded breakout) | |

- For **6 rooms, about €130–220.** That fits the budget.
- **Advice from us:** buy **one genuine sensor** (Sensirion/Adafruit/SenseAir) as the reference. Put every cheap node next to it for a day to check them. We've read that there are fake or poorly calibrated SCD40s around [unverified]. The "old Galaxy phone as the display" idea is a nice extra, but it adds an Android app to finish. Only do it if someone in the team already writes Android.

**AI approach (finishable in time)**
1. **Minutes-to-1,500-ppm forecast.**
   - Inputs: the last 10 min CO₂ slope, the timetable (class size), the room volume and time since the last airing.
   - Model: start with linear regression / gradient boosting in scikit-learn on our own logged data. Two weeks of 6 rooms at 1 reading/min is about 120k points, which is plenty.
   - It runs on a Raspberry Pi or laptop server, or even as a formula pushed to the ESP32.
2. **Airing-length advice.** Fit each room's CO₂ decay curve after a window opens against outdoor temperature (free weather API). Output: "open fully for 4 min".
3. **Heat-waste detector.** A rule plus a classifier on the reed-switch and temperature traces, looking for "window open more than 15 min during heating". Convert that to kWh and € with a simple physics formula.
4. **Optional:** an LLM writes the Friday one-paragraph report for the director.

All of it can be trained with data we collect ourselves, and none of it needs deep ML skills. It is *useful*: a threshold light only reacts once the air is already bad, and the forecast tells you to air at the *next break* instead of mid-lesson.

**Demo trick:**
1. A team member breathes into a clear jar over the node. The ring goes amber and the screen says "red in ~3 min, air at the bell for 4 min".
2. Lift the jar and the live graph drops.
3. A little plywood "window" with the reed switch, opened next to a hair dryer, starts the "€ lost this hour" counter ticking.

Reliability is very high: breath is about 40,000 ppm, so the sensor reacts within seconds [unverified figure, standard physiology].

**Mini-pilot:** very feasible.
- Rooms, not people, so we only need the director's signature. No parent forms.
- Heating starts in October [verified].
- Plan: a week-2 baseline with the light hidden, then weeks 3–5 with the light on, plus a 200-student anonymous survey.

**Biggest risk to Nov 6:** being boring. Technically the risk is sensor quality (clones) and teachers ignoring the light. Mitigate with a student "air captain" per class.

---

### F2 Energijos detektyvai 50/50 (13/18 · build 6 · excite 4)

**Gut feeling:** a good idea for adults. For us:
- We don't pay the bill and can't *feel* the kWh.
- **Minors cannot open the school's electrical switchboard.** A CT clamp on the main feed needs the school electrician [unverified: common safety rule; certainly the director will insist].

That leaves smart plugs on a few projectors, which is small and dull.

**BOM:**
- 5 × Shelly Plug S Gen3 (power metering, ESPHome-compatible) at about €20–25 each [product verified: [Shelly](https://www.shelly.com/products/shelly-plug-s-gen3), [ESPHome devices](https://devices.esphome.io/devices/shelly-plug-s-gen3/); price unverified]
- 1 × Shelly EM Gen3 with 2 clamps, installed by an electrician (€50–70) [product verified: [Shelly EM Gen3](https://www.shelly.com/products/shelly-em-gen3); price unverified]
- **Total: €120–200.**

**AI:** anomaly detection on the load curve compared with the timetable. It is solid, but the jury never sees it happen live.

**Demo:** plug in a "forgotten" kettle and the dashboard flags it. It works, but nobody will remember it.

**Pilot:** 2 weeks of baseline plus 2 of action. Getting a 50/50 letter from the municipality within 6 weeks is unlikely.

**Biggest risk:** access to the switchboard, and a demo that looks like a Shelly app screenshot.

**Verdict:** fold its best part (heat-waste €) into F1 and drop it as a standalone.

---

### F3 DušoSargas / ShowerCoach (15/18 · build 7 · excite 8)

**Gut feeling:** this is the one we'd laugh about and *want* to build ("my mum yells at me"). The amphiro evidence (−22–23%) is strong. Existing DIY shower and hot-water flow meters on ESP32 with a YF-B5 plus an OLED show the electronics are easy [verified: [goblingift/WaterFlowMeter](https://github.com/goblingift/WaterFlowMeter), [Hackster Smart Water Meter](https://www.hackster.io/Pedro52/smart-water-meter-58d99d), [CircuitDigest](https://circuitdigest.com/esp32-based-smart-diy-iot-water-flow-meter)].

The hard parts are not electronic:
- **Waterproofing and power in a bathroom.** It needs a battery; mains in the shower is out.
- **Installing it in 8–10 families' showers**, most of which are rented or parents' flats.
- **Water on a stage.**

**BOM (per unit)**

| Part | Price | Tag |
|---|---|---|
| ESP32-C3 or ESP32 | €4–8 | [verified base price, §0] |
| Brass G1/2" flow sensor YF-B5 / YF-B6. It fits a standard shower hose thread; use brass, not the plastic YF-S201, because it's hot water. | €6–12 | [unverified price; YF-B5 ESP32 use verified in the goblingift repo] |
| DS18B20 waterproof temperature probe (or a thermistor in a T-piece) | €2–3 | [unverified] |
| 0.96" OLED or WS2812 ring | €3 | [unverified] |
| 18650 cell + holder + TP4056 charger | €6–8 | [unverified] |
| IP65 box, G1/2 adapters, PTFE tape | €5–7 | [unverified] |
| **Total per unit** | **about €26–38** | |

**8 units: about €210–300.** That is the whole budget, so maybe build 6.

**AI approach:**
- Per-person recognition from (time of day, flow, temperature, duration) with k-means or a small decision tree. Honestly this is *thin*, and "who is showering" is a bit creepy. It also only works with 3+ weeks of data.
- Better and more honest: **forecast "this shower will cost €0.40 if you keep going"** from the first 60 s, plus personal goals.
- An LLM weekly family report is easy, but the jury may call it a wrapper.

AI scores 1: the device works without it.

**Demo trick:** a 12 V pump in a bucket pushes warm water through a real shower hose into a second bucket. The display counts litres and euro cents, and the ring goes green → red. It is very memorable.
- **Venue risk:** the organisers may not allow water and electronics on stage.
- **Backup:** a pre-filmed shower video plus the device running with a small aquarium pump inside a transparent box.

**Mini-pilot:**
- Plan: 6–8 team or classmate families, 1 week with the display covered (baseline), then 2 weeks with feedback. Parent consent is easy because they're our own families.
- Problem: 3 weeks per family only ends by **~Oct 30** if everything is installed by Oct 9. Parts must be ordered from EU shops in week 1.
- Six households is small, but "−X% in our families" plus a 200-student "how long do you *think* you shower" survey is a strong slide.

**Biggest risk to Nov 6:** leaks, broken sensors and flat batteries in family bathrooms during the only 3 pilot weeks. One wet ESP32 costs us a household. Build 2 spares.

---

### F4 Šilumos detektyvai: heat detectives (16/18 · build 8 · excite 5)

**Gut feeling:** it's fun for one afternoon to point a thermal camera at your window. But the camera does 90% of the work and we just buy it. That is exactly the **"tech wrapper" pattern the team rejected** (photographing test strips).

The AI that would make it ours means classifying leak types in thermal images and ranking fixes by €. That needs labelled thermal images we don't have. It can't be trained well in 6 weeks: at most a few hundred of our own scans, and public thermal datasets are not confirmed [unverified]. The realistic version is a threshold-based cold-spot finder plus an LLM-vision report. That is a wrapper.

**BOM:** one InfiRay P2 Pro, about **€222–231** on eBay.de, or a Topdon TC001 (256×192, Android USB-C) in the $200–300 range [verified: [eBay.de P2 Pro](https://www.ebay.de/itm/364883646887), [allcom.se review](https://allcom.se/2023/12/31/infiray-p2-pro-and-topdon-tc001-thermal-cameras-capsule-review/), [Topdon TC001](https://www.topdon.com/products/tc001)].
- That is the entire budget for one camera.
- A cheap alternative is an MLX90640 32×24 sensor on an ESP32 (€40–60 [unverified]), but the images look poor on a projector.

**Demo:** point the camera at a plywood window frame with a hair dryer or ice pack behind a gap. The app circles the leak and says "seal tape €6, saves ~€X/winter". It is reliable.

**Pilot:** 20 classmates' flats in late October (the inside–outside ΔT needs to be about 10 °C or more, so it depends on the weather).
- Consent is simple.
- A before/after € saving is **not measurable** by Nov 6, hence I = 1.

**Biggest risk:** the jury asks "what did *you* build?" A warm October makes the images weak.

---

### F5 Dūmų radaras: smoke radar (14/18 · build 8 · excite 7)

**Gut feeling:** outdoorsy, nature and air, a map, a real forecast. It feels like science. The electronics are the most proven recipe on this list. Sensor.community's airrohr is a standard low-cost PM node, and there are forum comparisons of SDS011 vs PMS5003 [verified: [Sensor.Community forum](https://forum.sensor.community/t/sds011-vs-pms5003-vs-pmsa003i/2161), [Then Try This notes](https://thentrythis.org/notes/2021/09/17/notes-on-sensor-components-for-a-low-cost-air-quality-monitoring-device/)].

Two weaknesses:
- **Relatability** only works for teams from private-house districts or small towns. In a Vilnius block-of-flats school it's less "ours".
- **"Families of asthmatic kids"** means we need to find those families and get consent. That's hard in 6 weeks.

**BOM (per node)**

| Part | Price | Tag |
|---|---|---|
| SDS011 (about £12) or PMS5003 (under $20) | €12–20 | [verified: [Then Try This](https://thentrythis.org/notes/2021/09/17/notes-on-sensor-components-for-a-low-cost-air-quality-monitoring-device/) / search summary] |
| ESP32 | €5–8 | [verified] |
| BME280 temperature/RH (needed for humidity correction) | €3–5 | [unverified] |
| Weather shelter: 2 plant pots / drainpipe elbow, USB PSU | €6–8 | [unverified] |
| **Per node** | **about €26–40** | |

**5 nodes: about €130–180.**

**AI approach:** this has the best "AI at the core" of the sustainability ideas (A = 2). Six weeks of our own data is too little to train on, and here is the trick:
- **Download historical data from existing Sensor.community nodes in Lithuania** and hourly weather history, then train the "tonight's smoke hours" forecast (gradient boosting on hour, temperature, wind, inversion proxy, weekday) *before* our own nodes are even up.
- Then validate it on our nodes in October.

[unverified: that LT has enough Sensor.community nodes in our town. Check the map in week 1; it's free.]

**Demo trick:** an incense stick near the node makes PM spike and a phone alert pops up ("smoke episode, move PE indoors").
- **Risk:** some venues ban open flame.
- **Backup:** a jar pre-filled with incense smoke, lifted over the sensor.

**Pilot:** 5 nodes at team members' homes and the school from about Oct 5. Forecast accuracy on 4 weeks of evenings, plus an anonymous asthma/allergy survey (n ≥ 150).
- We should *not* promise "families used the alerts". That needs health-data consent.

**Biggest risk:** a warm, windy October gives few smoke episodes to show. The AI also needs enough historical LT data.

---

### F6 RecessBox (15/18 · build 5 · excite 5)

**Gut feeling:** carpentry plus 12 V solenoids plus NFC plus an LLM game master. It is a lot of mechanical work for a sport idea the team is lukewarm about.
- The "AI game master" is an LLM picking from a rulebook, which is wrapper-ish.
- Installing a lockable box in a corridor needs the director's approval and a caretaker's help.

**BOM:**

| Part | Price |
|---|---|
| Plywood + hinges | €40 |
| 3 × 12 V solenoid locks | €8 each |
| Relay board | €5 |
| PN532 NFC reader | €6 |
| ESP32 | €6 |
| 12 V PSU | €10 |
| Reed switches | €3 |
| Old tablet as screen | €0 |
| Balls/ropes/frisbees | €100 |
| **Total** | **about €200–260** [all unverified] |

**AI:** an LLM plus speech-to-text in Lithuanian (the Lithuanian speech-to-text quality is a risk).

**Demo:** a judge taps a card, gets a game and a door clicks open. It's good and tactile.

**Pilot:** 2–3 weeks in the corridor, feasible if the box is ready by week 3, which is tight.

**Biggest risk:** the physical build overruns, and the box doesn't exist yet when the pilot should start.

---

### F7 Traukinukas: walking/bike bus (15/18 · build 5 · excite 6)

**Gut feeling:**
- The tech is the easy bit: a phone in "leader mode" posting GPS to a web map, plus k-means route clustering on OpenStreetMap.
- The **pilot is the hard bit**: minors leading minors to school needs parent consent, possibly insurance, the director's blessing and a partner primary school [unverified: requirements].
- Our own lessons start at the same time as the walk.
- November mornings are dark.

It is realistic to *run 2–3 test walks*, not 3 weeks of daily lines.

**BOM:** €0 if we use a phone. A dedicated tracker (ESP32 + GPS + LTE-M) costs €40–60 [unverified] and adds risk for no stage value.

**AI:** route clustering plus a safety score from injury hotspots. That is real but modest.

**Demo:** a team member walks across the stage in a hi-vis vest and the judge's phone gets "arriving at your stop". GPS indoors in a conference hall **will not work**, so the demo needs a simulated track. That is a bit fake.

**Biggest risk:** consent and logistics. The pilot numbers could end up being only a parent survey.

---

### F8 HeartSquad: CPR in PE (18/18 formula, theme risk · build 8 · excite 8)

**Gut feeling:** the most exciting stage moment on the list. A jury member does CPR, scores 62%, gets coached, then scores 90%. It has a strong "we realised none of us could do this" story, and **every part has a DIY precedent**:
- Arduino CPR feedback devices measuring depth, rate and recoil exist: a Hackster/Arduino Project Hub build, a research paper and an FSR-based device [verified: [Hackster](https://www.hackster.io/daescobar/arduino-powered-cpr-feedback-device-58e6bd), [ResearchGate 2025](https://www.researchgate.net/publication/395701223_Design_and_Implementation_of_an_Arduino-Powered_CPR_Feedback_Device), [PCBWay CPRmeter](https://www.pcbway.com/project/shareproject/CPRmeter_CPR_Feedback_Device_6bbb5104.html)].
- MediaPipe Pose runs in a browser or on Android for free [unverified: background knowledge, very well known].

**The catch is the theme.** The team leans sustainability, and "Sport & tech" is about *getting students active / making sport meaningful*. We'd have to frame it as "safe sport: every team and every PE class knows CPR", anchored on sports halls and SAM's AED plan [verified in scout-teen-sport]. A sceptical jury member could still say "this is first aid, not sport".

**BOM (per manikin)**

| Part | Price | Tag |
|---|---|---|
| ESP32 (BLE to the phone) | €5–8 | [verified] |
| Depth: VL53L0X/VL53L1X ToF looking up at the chest plate | €4–10 | [unverified: my VL53L0X price search returned no price] |
| Force: 4 × 50 kg half-bridge load cells + HX711 kit | €3–10 | [verified: kits widely listed on [eBay](https://www.ebay.com/itm/182899653153) / [Alibaba $0.23–3.5 wholesale](https://www.alibaba.com/showroom/50kg-load-cell-hx711.html)] |
| Chest mechanism: 2 plywood plates + 4 compression springs (about 5–6 cm travel at ~40–50 kg) or a foam block; a stuffed hoodie torso | €15–25 | [unverified: getting the spring stiffness right is the real engineering task] |
| Buzzer/LED metronome, USB power bank | €5 | [unverified] |
| **Per manikin** | **about €35–55** | |

**3 manikins: €100–170.** An optional cheap commercial CPR torso shell costs €30–50 [unverified].

**AI approach:**
1. Signal processing on ToF + load cell gives depth, rate and full recoil. This is mostly maths, not ML, and that's fine.
2. **MediaPipe Pose** on the phone camera gives elbow angle (locked arms), shoulders over hands and hand position. It is off-the-shelf, and all we add are the angle thresholds.
3. A small classifier on the stroke waveform ("leaning", "bouncing", "too shallow") trained on our own ~2,000 labelled compressions [unverified: count; easily collected in one PE lesson].

This is a real, visible AI job a teacher can't do by eye (A = 2).

**Demo trick:** "Who here has done CPR this year?" A judge presses for 20 s, the live gauge shows the score, the AI says "lock your elbows, faster", and the second try scores higher. There's no water, no fire and no network needed (BLE only). **It is the most reliable live demo on the list.**

**Mini-pilot:**
- 100–150 students in PE lessons, weeks 4–5, logged automatically before/after (anonymous IDs).
- Camera use: process the video live and store no video. That avoids parental consent for video [unverified: confirm with the school].
- Needs the PE teacher on board, which is one conversation.

**Biggest risk:** the spring/torso mechanics (it must feel roughly like a chest and give 5–6 cm), and the theme-fit question at the local jury.

---

### F9 Švilpukas ant riešo: whistle wristband (13/18 · build 8 · excite 8)

**Gut feeling:** the coolest *tech* to learn (TinyML!), with a very clear 5-second demo. The tooling is well trodden: Edge Impulse keyword spotting on an ESP32-S3 with an INMP441, and data capture through the Edge Impulse data forwarder [verified: [Hackster KWS ESP32-S3 + INMP441](https://www.hackster.io/amy/keyword-spotting-on-esp32-s3-with-inmp441-and-max7219-c3de33), [CircuitDigest](https://circuitdigest.com/microcontrollers-projects/esp32-offline-voice-recognition-using-edge-impulse), [Edge Impulse ESP32 docs](https://docs.edgeimpulse.com/hardware/boards/espressif-esp32)].
- Someone already did "faucet ON" sound classification on an ESP32 + INMP441, the same kind of non-speech sound event [verified: [EI forum](https://forum.edgeimpulse.com/t/audio-classification-using-esp32-and-inmp441-microphone-to-detect-faucet-on-training-on-edgeimpulse-using-mfcc-and-keras-classifier/17182)].
- No whistle-specific tutorial turned up [verified absence in 2 searches].

**But:**
- We don't know a deaf athlete (T = 1).
- It's sport, not sustainability.
- The audience is small, and the pilot depends on finding a deaf-sport club in time.

**BOM (per band)**

| Part | Price | Tag |
|---|---|---|
| Seeed XIAO ESP32S3 Sense (mic onboard, tiny) | $14.90 | [verified: [Seeed](https://www.seeedstudio.com/Seeed-Studio-XIAO-ESP32S3-Sense-Pre-Soldered-p-6335.html)] |
| *or* ESP32-S3 dev board + INMP441 | €8 + €3 | [unverified] |
| Coin vibration motor + transistor, LED | €2 | [unverified] |
| 300–500 mAh LiPo | €5 | [unverified] |
| 3D-printed case + watch strap | €4 | [unverified] |
| **Per band** | **about €22–30** | |

**3 bands: €60–90.** This is the cheapest serious build.

**AI:** an Edge Impulse MFCC/spectrogram CNN. Classes: whistle / crowd / sneaker squeak / talk / clap. Target: 200+ whistle clips and 200+ noise clips, recorded in our own gym in weeks 1–2. It is trainable in days.

**Demo:** stadium noise from a speaker, a judge wears the band, a team member blows a whistle and the band buzzes. Talking and clapping don't trigger it.

**Pilot:** a lab accuracy/latency test (easy), plus one session with deaf or hard-of-hearing players (partner unknown [unverified]).

**Biggest risk:** no deaf partner by Nov 6, which kills authenticity. Loudspeaker acoustics at the venue could also cause false triggers or misses.

---

### F10 Pulso kūno kultūra: heart-rate PE (16/18 · build 6 · excite 5)

**Gut feeling:** "PE grades are unfair" is instantly relatable. But the Samsung Watch route has a verified blocker:
- **Samsung Health Sensor SDK developer mode needs an access key that Samsung shares only after a partnership approval.** Without approval, the app works only in developer mode, and that mode itself needs the key [verified: [Samsung Developer: developer mode](https://developer.samsung.com/health/sensor/guide/developer-mode.html), [app creation process](https://developer.samsung.com/health/sensor/process.html)].
- We cannot count on getting that in 6 weeks.
- The fallback is standard BLE chest straps, which any phone or Web Bluetooth can read (standard HR service): Coospo H6, BLE + ANT+, CR2032 battery [verified product: [Coospo](https://www.coospo.com/products/h6-chest-strap-heart-rate-monitor); price unverified, about €25–30]. That means 6–8 straps at **€150–250**.

**AI:** the zones come from the Karvonen formula (arithmetic, not AI). Real ML would be personal fitness/recovery trends, which need weeks of data. A = 1.

**Demo:** jumping jacks turn the tile green. It's OK but generic, and it *looks* like a fitness app, close to the "wearable points" genre the team rejected.

**Pilot:** 2 PE classes over 3 weeks. Heart rate is **health data of minors**, so parent consent forms are needed for every student. It's doable but slow.

**Biggest risk:** the Samsung SDK access, and consent paperwork eating two of our six weeks.

---

## 3. Six-week build plans for our top 3

**Weeks:**

| Week | Dates |
|---|---|
| W1 | Sep 28–Oct 4 |
| W2 | Oct 5–11 |
| W3 | Oct 12–18 (**idea form Oct 16**) |
| W4 | Oct 19–25 |
| W5 | Oct 26–Nov 1 (autumn break for many LT schools [unverified dates]) |
| W6 | Nov 2–6 (**submission Nov 6**) |

### Plan A: Klasės oras + smoke check (F1 × F5 hybrid, see §5)

| Week | Hardware | Software / AI | Pilot and paperwork |
|---|---|---|---|
| W1 | Order 6 SCD4x/S8 + 1 genuine reference + 2 SDS011/PMS5003 from EU shops. Breadboard node 1 with borrowed parts. | ESP32 → MQTT/HTTP → Raspberry Pi/laptop with InfluxDB+Grafana (or Google Sheets). Weather API hookup. | Director permission letter; pick 6 rooms; write the 200-student survey. Measure our own chemistry room → the pitch number. |
| W2 | Build 6 indoor nodes + 1 outdoor PM node on a school window; 3D-print cases; co-locate for calibration for 1 day. | Log everything at 1/min; heat-season start check. | **Baseline:** lights hidden (tape over the ring). Run the survey. |
| W3 | Reed switches on windows; fix bugs. | First forecast model (CO₂ slope → minutes to 1,500) on baseline data; decay-curve fit per room. | **Submit the idea form (Oct 16)** with the baseline graph. |
| W4 | Lights on; spare node ready. | Rule "don't air now, outdoor PM high → air at the next break"; € heat-waste counter; dashboard. | **Intervention weeks.** Brief teachers + "air captains". |
| W5 | Stage demo kit: jar, mini window with reed switch + hair dryer. | Evaluate the forecast (MAE in minutes); LLM Friday report. | Keep logging (the break may pause lessons; note it). Ask the municipality for a support letter. |
| W6 | Film the backup demo video. | Final numbers: % lesson time above 1,500 ppm before/after; open-window heating minutes; € estimate. | Visual presentation + concept doc; rehearse the English pitch. |

### Plan B: HeartSquad (F8)

| Week | Hardware | Software / AI | Pilot and paperwork |
|---|---|---|---|
| W1 | Order springs, load cells + HX711, ToF, ESP32. Prototype the chest mechanism (plates + springs) and test it with a bathroom scale until ~5 cm ≈ 40–50 kg. | Read HX711 + ToF over BLE; phone web app (Web Bluetooth) with a live depth gauge. | PE teacher + director on board; ask the Red Cross/first-aid trainer for a supporting quote. |
| W2 | Manikin 1 done; calibrate depth against a ruler, rate against a metronome. | MediaPipe Pose in the browser: elbow angle, shoulders over hands. | Survey 200 students "would you start CPR?" (1–5). |
| W3 | Manikins 2–3. | Score formula (depth, rate, recoil, arms) → 0–100%. | **Idea form Oct 16** with a video of manikin 1 working. |
| W4 | Durability fixes (springs, cable strain relief). | Collect ~2,000 labelled compressions; train a small waveform classifier. | **PE lessons:** pre-test → 20 min AI-coached lesson → post-test (anonymous IDs, no stored video). |
| W5 | Spare manikin parts. | Coaching prompts in LT + EN; certificate screen. | More classes → n = 100–150. |
| W6 | Stage kit. | Results: % correct depth before/after; confidence before/after. | Concept + presentation; frame the theme as "safe sport". |

### Plan C: DušoSargas / ShowerCoach (F3)

| Week | Hardware | Software / AI | Pilot and paperwork |
|---|---|---|---|
| W1 | Order 8 brass YF-B5/B6 + probes + batteries from **EU** shops (AliExpress is too slow). Bench-test one unit with a tap. | ESP32 deep-sleep, wake on flow pulse; log to flash, upload over Wi-Fi after the shower. | Recruit 6–8 families; one-page parent consent; the 200-student "how long do you shower?" survey. |
| W2 | Build 8 units in IP65 boxes; leak-test each for 1 h under hot water. | Litres/°C → kWh → € with the family's own tariff. | **Install by Oct 9.** Baseline week with the display covered. |
| W3 | Fix failures (expect 1–2). | Display on: live € and ring. | **Idea form Oct 16** with baseline data from real showers. |
| W4 | — | "Cost-of-this-shower" forecast after 60 s; per-person clustering once data exists. | **Feedback weeks** (Oct 16–30). |
| W5 | Demo rig: bucket + 12 V pump + hose inside a clear tray. | Weekly family report (LLM, optional). | Collect units; compute % litres/shower change. |
| W6 | Film the backup demo in a real shower. | Final numbers vs amphiro's −22%. | Concept + presentation. |

---

## 4. Demo trick ranking (what the jury will remember)

1. **F8:** the judge does CPR and gets coached live, and the score jumps. It involves the jury, needs no network and is very reliable.
2. **F9:** the whistle over crowd noise buzzes the judge's wrist. Instant, but the venue acoustics add risk.
3. **F3:** water runs through a real shower hose while euro cents tick up. Fun, but a water/stage risk.
4. **F1 (+F5):** breath in a jar turns the light red; lifting the lid brings the CO₂ down; the "window" and hair dryer start the € counter. Reliable, a bit familiar.
5. **F5:** incense → PM spike → alert. Open-flame risk.

Weaker: F4 (point a camera), F6 (card tap + door), F10 (jumping jacks), F2 (plug in a kettle), F7 (simulated GPS dot).

---

## 5. Merge / hybrid proposals

**Recommended: "Oro sargas" = F1 + F5 (+ the F2 heat-€ counter).** The same ESP32 classroom node, plus **one outdoor PM node per school**. The AI decides *when* to air using three signals:
1. indoor CO₂ trend (the forecast)
2. outdoor smoke (PM2.5 now, and the evening-smoke forecast trained on Sensor.community history)
3. heat loss (outdoor temperature, window reed switch)

Output: "Air now for 4 min", or "Don't open now: chimney smoke outside, air at the next break", or "Window open 20 min with heating on: €0.60 lost".

Why it's better for us:
- It kills the "CO₂ monitors already exist" objection, because no classroom monitor also checks the *outside* air before telling you to open the window [unverified: absence not searched].
- It makes the AI genuinely needed: a trade-off between three signals, not a threshold.
- It adds the nature/air story the team likes.
- It costs only about €30–40 more (1–2 PM nodes).

It also keeps F1's easy, consent-free pilot.

**Not recommended for 6 weeks:** F3 + F4 "home energy kit". That's two different builds (plumbing plus a thermal camera) and two pilots at once. Keep ShowerCoach alone if chosen.

**Possible:** F9's TinyML skill could later add "clap/whistle to acknowledge" to F1. It's a gimmick; skip it.

---

## 6. Our ranked top 5 (the builders' view)

1. **F1 Klasės oras, as the F1+F5 "Oro sargas" hybrid.** Formula 17, build 9, excitement 8 with the smoke twist.
   - Near-certain to work by Nov 6. The pilot needs only the director's signature. The heating season starts during our build [verified]. Cheapest per room.
   - The hybrid fixes its only weakness (it's "just a CO₂ light").
2. **F8 HeartSquad.** Formula 18 (theme risk), build 8, excitement 8.
   - The best live demo and the strongest AI-that-helps. It is cheap and has no weather dependence.
   - Rank it #1 instead if the team is happy to pitch under *Sport* and a quick check with the organisers or a mentor says "safe sport / CPR in PE" fits the theme.
3. **F3 DušoSargas / ShowerCoach.** Formula 15, build 7, excitement 8.
   - The most fun to pitch ("my mum yells at me") and a great proven number (−22%).
   - But the AI is thin, and a 6–8-household pilot in bathrooms is the most fragile logistics of our top 3.
4. **F5 Dūmų radaras (standalone).** Formula 14, build 8, excitement 7.
   - Real forecasting AI with a data trick (Sensor.community history), but a weaker "we feel it" hook for city teams. Its best use is inside #1.
5. **F9 Švilpukas ant riešo.** Formula 13, build 8, excitement 8.
   - The coolest TinyML build and the cheapest, but it's go/no-go on finding a deaf athlete partner in week 1.

**Just outside:**
- F4: a wrapper risk; the camera eats the budget.
- F10: the Samsung SDK access key is a blocker [verified], and minors' health-data consent.
- F6 and F7: the build or pilot logistics are too heavy for 6 weeks.
- F2: switchboard access; dull demo.

**Decision rule for the team this week:**
- If you want the *safest route to the local top 5*, pick **#1 (hybrid)**.
- If you want the *most memorable stage moment* and are fine with Sport, pick **#2**.
- Either way, order parts from EU shops **this week**. Shipping time is the silent killer of every plan above.
