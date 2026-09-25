# Round 5 results: ideas someone would actually *want*

**Why this round:** the team called round 4's picks lame: "classroom CO₂ meter: seen it so many times", "CPR trainer: used once", "recess box: used by who?". Only ShowerCoach got an "I'd want that". Five new generators (online pain-mining, home and family, wow-demo hardware, Lithuanian nature, sport with edge) produced **~170 ideas**. This time they filtered for **WANT** (used repeatedly), **WOW** (a demo that makes people lean forward) and **NOT-SEEN** (not a science-fair staple), with the old winning formula as a tie-breaker ([`BRIEF.md`](BRIEF.md)).

Full lists: [`gen-online-pain.md`](gen-online-pain.md) · [`gen-home-want.md`](gen-home-want.md) · [`gen-wow-demo.md`](gen-wow-demo.md) · [`gen-lt-nature.md`](gen-lt-nature.md) · [`gen-sport-edge.md`](gen-sport-edge.md)

**The strongest signal:** two ideas were reached **independently by several generators**. Lake ice safety came from 3 of 5, and the Soviet-block hot-water detective from 3 of 5. When different angles converge, the problem is real.

---

## 🥇 A. Ledo sargas ("Ice Guard"): live ice thickness for Lithuanian lakes (Sport & outdoor safety)

**What it physically is.** A €40 stake that freezes into the lake ice. A string of ~30–40 cheap digital thermometers every 2 cm reads the temperature profile. Ice, water and snow have different temperature signatures, so the stake can tell where the ice ends. A LoRa radio sends readings every 10 minutes to a public map: **"Lake Kaunas, bay by the camp: 9 cm and growing. OK for one person, not for a group."**

**What the AI does.**
1. It turns noisy temperature profiles into a thickness reading.
2. It forecasts the next 3–5 days from the weather forecast (the ice-growth physics plus a learned correction).
3. It spreads the readings from a few stakes to whole lakes using weather and satellite ice-on dates.

A handheld version for anglers is optional: the "Ice Ear" pick, which estimates thickness from the sound of a tap, or a bite alarm with the sensor in its stem.

**Who wants it, repeatedly.** Ice anglers (a huge hobby in Lithuania), skaters on natural ice, parents whose kids go on the pond, and rescuers. They check it every winter weekend.

**Why it's good.**
- People fall through the ice every winter [verified: LRT]. The official rule is ≥7 cm for one person and ≥12 cm for a group [verified: Environmental Protection Dept / Fire and Rescue Dept].
- Today people guess, drill test holes, or ask in Facebook groups.
- **The proven model:** SmartICE in Canada uses exactly this thermistor-string approach in 40+ Arctic communities [verified, generator].
- A 2023 study got acoustic ice thickness within 5–10% of drilled holes [verified: Cold Regions Sci. & Tech.].
- Nothing like it found in Lithuania [unverified absence].

**The demo.** Three trays of ice, 3, 6 and 10 cm thick, frozen in a freezer. The stake or pick reads each one: "3 cm: STOP", "6 cm: one person only", "10 cm: safe". The live lake map is on the screen behind.

**Timing (the honest catch).** There is no natural ice before Nov 6.
- **Stage 2 (Nov 6):** a lab prototype and accuracy tests on freezer ice (predicted vs ruler); a survey in angler Facebook groups; a letter from an angler club or the Fire and Rescue Department.
- **The December Baltic final** may coincide with first ice on small ponds [unverified], which would give real field data.

**Themes:** Sport & tech (safe winter sport and outdoor activity), with a nature and climate angle: warmer winters make ice less predictable [unverified framing].

**Risks.**
- **Liability:** "your map said safe". The map shows measurements and the official rule, never "safe".
- A stake can be vandalised or lost.
- The thermistor-string accuracy needs a week-1 test.
- The pilot season doesn't match the contest calendar.

---

## 🥈 B. Gyvatuko detektyvas: the Soviet-block hot-water detective (Sustainability)

**It started from:** your dad being mad about wasted hot water.

**The problem, verified.**
- In old blocks you run the tap for ages before hot water arrives, and the water poured away in the meantime is billed as hot. Tauragė upper-floor residents drain "a bucket" [verified: kurjeris.lt].
- On top of that, every flat pays the **"gyvatukas" fee** for keeping hot water circulating. In the heating season it's a fixed amount per flat (e.g. 160 kWh/month) *whether or not the circulation works*. One 2022 example came to ~€40/month [verified: Kauno energija, Vilniaus šilumos tinklai, tv3; the current price is unchecked].
- The legal test: tap water must reach ≥50 °C after 1 minute of running, or Legionella can grow [verified: NVSC].

**What it physically is.** Three layers:
1. **At home:** a shower or tap unit shows litres and € live, plus **"litres wasted waiting for hot water today"**. A camera clipped onto the existing water meter can also read it, with no plumbing (open-source meter-reading models exist).
2. **In volunteer flats:** a €10 battery clip on the bathroom towel-rail coil (the "gyvatukas" itself) logs its temperature for months.
3. **Across the building:** a heat map by floor and pipe run. AI ranks the likely causes (pump off at night, one pipe run unbalanced, water set too cool) and writes a report for the building administrator and the heat utility.

**Why it's good.**
- Every family in a Soviet block knows the "wait for the hot water" ritual. It starts as one family's gadget and grows into a diagnosis of the whole building, then the city: a real "solve for tomorrow" scale.
- **Proven models:** amphiro showers (−22% in a Swiss field study) and amphiro/Oras building water monitoring for Legionella in AT/FI/DE/SE. That's sold to businesses; nobody sells it to residents.

**The demo.** Hot water "arrives" on stage: the counter shows "38 s, 4.2 L wasted, €0.03". The building map then lights up the top-floor pipe run in red: "circulation failing here; you paid €X for it this month".

**Pilot by Nov 6:** yes. The heating season is starting. Run 5–10 flats in 1–2 blocks: shower units plus coil clips.

**Kill test in week 1.** Use a thermometer and a bucket in the team's own flats. How long until the tap reaches 50 °C? If no block shows failing circulation, it shrinks back to a nice gadget.

**Risks:**
- The shower unit only sees mixed water, so the building story rests on the coil and pipe clips.
- Waterproofing.
- Building administrators may not want to hear it.

---

## 🥉 C. BackTrack (Grybų švyturys): the way home for mushroom pickers (outdoor activity and safety)

**What it is.** A €20 clip or fob for grandparents: three buttons, an LED arrow, and a LoRa radio with a second unit left in the car, so it needs no phone signal.
- One press marks the car; then the arrow always points back along your own track.
- It also keeps a **private diary of your mushroom spots**, which is why grandpa carries it every trip.

**The AI.** It notices "lost-like" walking (loops, slowing pace, dusk approaching) and offers to lead you back. If you don't respond, it alerts the family with your track, and rescuers get a probability map of where to search.

**Why it's good.**
- Police got **100+ reports of lost mushroom pickers** in one season; in August alone 16 people got lost in Kaunas county forests. Searches use drones, dog teams and firefighters [verified: diena.lt, 15min.lt].
- **The only top idea you can pilot right now:** the season runs through October. Give it to 10 grandparents.

**Risks.**
- The jury may ask "isn't this just GPS?". Answer: grandparents don't use phone GPS, and there's no signal in the forest.
- The **theme fit is the weakest**: it has to be framed as safe outdoor activity for seniors.
- The users are grandparents, not students. You could flip that into the pitch: "we built it for our grandparents".

---

## 4. Kiemo Karalius / Court Ear: the street basketball hoop that knows (Sport)

**What it is.** A solar, **camera-free** box bolted behind any courtyard hoop. A beam sensor under the ring plus a vibration sensor and mic on the backboard classify swish, rim-in, clank or airball with on-board AI, and it works in the dark.
- For players: a button on the pole starts shooting challenges with a leaderboard for that court and battles between courts.
- For everyone: a live map shows which courts have a game on now.
- For the municipality: the first data on which courts it funds actually get used.

**Why it's good.** Basketball is Lithuania's religion. Lithuania's men won 3x3 bronze at Paris 2024 [verified: LRT]. Every teen who plays would want it on their court.

**The demo.** Shoot on stage: "SWISH +3", and the leaderboard updates.

**Honest prior art.** Smart outdoor courts exist in the US: RIMNET (camera at the hoop, 11 countries), HoopLink, huupe, Noah [verified]. So pitch it as camera-free, solar, cheap (~€100/hoop), with no phone needed and municipal usage data, not as "first ever".

**Risks:** separating makes from misses without a camera, vandalism, and fewer outdoor players in Oct–Nov.

---

## 5. Erkių radaras + TickBot: the tick-risk radar (Sustainability/health and outdoors)

**What it is.** A small rover (or a person) drags a white cloth through grass, the standard way ecologists sample ticks. A camera with AI counts the ticks on the cloth. The counts, ground-level temperature and humidity stakes and bite reports drive a daily risk map for trails, parks and school stadiums. A watch or phone nudges you: "check for ticks tonight".

**Why it's good.** Lithuania has the **highest tick-borne encephalitis rate in Europe**: 807 cases and 11 deaths in 2024 [verified: NVSC, ECDC, ulac.lt]. **The proven model:** Tekenradar (NL) [unverified details]. A tick-counting rover on stage is memorable.

**Risks.**
- Ticks fade by November, so field sampling is only possible in early October.
- The app alone is a wrapper; round 3 killed it. It only works with the hardware.

---

## Also worth a look (12–13/14)

| Idea | One line | Why not higher |
|---|---|---|
| StoveCoach (Malkų treneris) | A flue thermometer + AI coaches grandpa's wood stove: when to add logs or open the air, and when the wood is too wet. Less wood, less smoke; the first heating season under the 2026 coal ban | Smoke is less "felt"; needs a stove owner |
| Bark-beetle stethoscope | A contact mic hears larvae chewing inside spruce before the crowns turn red (168 events/min vs 2.6 healthy [verified: Fraunhofer]) | Beetles go quiet in autumn; needs infested logs |
| Siena | A €150 courtyard "Footbonaut": a 3×3 target wall that lights zones and trains your weak side | Commercial walls exist; a big build |
| Pelėsio sargas | A dew-point sensor in the coldest corner of a Soviet flat says "air now for 6 min" before mould starts | Close to the rejected CO₂ pattern |
| Ruonis | A clip-on for cold-water swimmers that detects the cold-fade in stroke rhythm and says "get out now" | Niche users |
| Electricity stethoscope | Reads the smart meter's blinking LED; AI names big appliances and their cost | Known among hobbyists |

---

## Our honest take

- **The two real contenders are A (ice) and B (hot water).**
  - **A** has the most wow and the most "nobody here has this". It saves lives and fits nature and outdoor life, which the team likes. Its weakness is the calendar.
  - **B** has the most authentic story ("my dad") and a pilot that fits right now, and it grows from one family to whole buildings. Its weakness is that the week-1 bucket test must show a real circulation problem.
- **C (BackTrack)** is the safe fallback if you want a pilot running this week.
- **D (Court Ear)** is the pick if the team would rather do sport and is into basketball.

**Next step:** pick 1–2 by gut, then run the week-1 kill tests:
- **A:** freeze ice in trays and check that the thermistor string reads thickness.
- **B:** a thermometer and a bucket in your own flats: seconds until the tap reaches 50 °C.
- **C:** do 3 grandparents want it?

About 10 web searches are left for the final fact checks.
