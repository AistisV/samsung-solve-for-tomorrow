# Round 4 results: ideas built to *win*, not to be novel

**Process.** Six parallel scouts (proven abroad: green and sport; teens' own lives: green and sport; what wins; Samsung-native) generated about 140 ideas and scored each on the 9-point winning formula ([`BRIEF.md`](BRIEF.md)). Ideas that several scouts reached independently were merged into 10 finalists ([`SHORTLIST.md`](SHORTLIST.md)). A 3-judge panel then scored all 10:
- **A**, a Samsung Solve for Tomorrow juror ([`judge-A-samsung-juror.md`](judge-A-samsung-juror.md));
- **B**, the real users: teacher, director, parent, PE teacher, child ([`judge-B-target-user.md`](judge-B-target-user.md));
- **C**, the 16-year-old team that has to build it ([`judge-C-team.md`](judge-C-team.md)).

About 180 web searches were used in total. Claims are tagged verified/unverified in the source files.

## Panel scores

| # | Finalist | Formula /18 (A · B · C) | Juror gut /10 (A) | Real adoption /10 (B) | Buildability /10 (C) | Panel rank |
|---|---|---|---|---|---|---|
| F1 (+F5 +F2) | **Oro sargas: classroom air & heat coach** | 17 · 17 · 17 | 6.5 → **8 as hybrid** | **7** | **9** | **1** (B #1, C #1, A #2) |
| F8 | **HeartSquad: CPR in sport/PE** | 17 · 17 · **18** | **8** (theme risk) | **7** | 8 | **2** (A #1, B #2, C #2) |
| F6 | **RecessBox: break-time kit locker** | 17 · 17 · 15 | 7.5 | 6 | 5 | **3** (A #3, B #3) |
| F3 | **ShowerCoach: live € shower meter** | 16 · 16 · 15 | 6 | 6 | 7 | **4** (B #4, C #3) |
| F9 | Whistle wristband for deaf players | 14 · 13 · 13 | 7 (8.5 with a partner) | 4 | 8 | 5, conditional |
| F5 | Smoke radar (standalone) | 14 · 13 · 14 | 7 | 3 | 8 | → merged into #1 |
| F4 | Heat detectives (thermal camera loan) | 16 · 14 · 16 | 6 | 5 | 8 | out: wrapper risk, a €230–300 camera |
| F10 | Heart-rate PE | 14 · 14 · 16 | 5 | 4 | 6 | out: already in LT schools (Polar); Samsung SDK needs partner approval |
| F2 | Energy detectives 50/50 (standalone) | 13 · 13 · 13 | 5 | 4 | 6 | → merged into #1 as the money mechanism |
| F7 | Walking bus | 12 · 13 · 15 | 4 | 3 | 5 | out: road rules expect adult escorts; weather |

**Vetoed despite high formula scores:** a canteen plate-waste camera (Minova won with food waste in 2022, and smart scales have run in Alytus-region canteens since Dec 2025).

---

## 🥇 1. Oro sargas ("Air Guard"): the classroom air-and-heat coach (Sustainability)

**What it physically is.**
- A small box on each classroom wall: an ESP32, a CO₂/temperature sensor, an LED ring and an optional magnetic switch on the window.
- Its display is **an old Galaxy phone collected from students' drawers**. It can also read a CO₂ meter the school already owns (Aranet, AirGradient, the meters Klaipėda schools are installing).
- **One outdoor smoke (PM2.5) sensor** per school.

**What the AI does.** It is a trade-off between three signals, not a threshold light:
1. It forecasts when the room will pass the legal 1,500 ppm and says **"air at the bell, fully open, 4 minutes"**, never mid-lesson unless it must.
2. It checks the **outside** air first: "don't open now, chimney smoke outside, air at the next break." Coal burning is banned in the big cities from 1 May 2026 [verified, judge A], but wood is not.
3. It catches the **window left tilted while the heating runs** and turns it into kWh and €. A weekly report goes to the director. The municipality returns 50% of the heat money saved, following the Euronet 50/50 model (500+ schools, ≥8% savings) [verified, scouts].

**Who uses it.**
- Teachers and a student "air captain" per class act on the light.
- The director gets an HN 21 compliance summary (lesson-average CO₂ ≤ 1,500 ppm is a legal norm [verified, judge B]).
- The municipality pays the heating bill and scales it. Its channels are the ~700-school health-promoting schools network and municipal education departments.

**Why a jury would love it.**
- Every juror has sat through the sixth-lesson headache. A Vilnius school reached 5,152 ppm against a 1,500 limit [verified, scouts].
- 18% of Lithuanians can't keep their home warm, against ~9% for the EU [verified, Eurostat via scout].
- Upcycled Galaxy phones make it *Samsung's own idea*: Galaxy Upcycling was a real Samsung programme, and 53% of Lithuanians keep an old phone in a drawer [verified, local-data]. The pitch line is **"We stop our school from heating the street, and we finished Samsung's idea for Lithuanian schools."**

**The proven models it adapts.**
- CO₂ traffic lights (Germany/Austria; one study found −19.5% CO₂).
- SAMHE (UK, ~2,000 classrooms).
- Euronet 50/50 (EU, 500+ schools).
- AsthmaSense (the 2025/26 UK & Ireland Solve for Tomorrow winner, an air-quality early warning).

**The demo (2 minutes).**
1. A presenter breathes into a clear jar over the box. The ring goes amber and the phone says "red in ~3 min, air at the bell for 4 min".
2. Lift the jar and the graph falls.
3. Open a plywood mini-window next to a hair dryer, and the "€ lost this hour" counter starts ticking.
4. Light incense near the outdoor sensor: "don't open now, smoke outside".

**The mini-pilot by Nov 6.** 6 classrooms, week 2 as a hidden baseline, weeks 3–5 with the coach on, plus a 200-student survey. It measures rooms, not people, so only the director's signature is needed and no parental consent. The heating season starts in October [verified, judge C].

**The impact number.** The share of lesson time above 1,500 ppm, before vs after (proven models: from >90% to <10%). A secondary figure is the kWh/€ of heat saved, which is modelled; present it as an estimate.

**Build plan (6 weeks, ~€160–260).**

| Week | Work |
|---|---|
| W1 (Sep 28–Oct 4) | Order 6 sensors + 1 genuine reference sensor + 2 PM sensors from EU shops. Director's letter. Measure our own chemistry room as the pitch number. |
| W2 | Build 6 nodes + 1 outdoor node, calibrate side by side, start the hidden baseline. |
| W3 | First forecast model; **idea form Oct 16** with the baseline graph. |
| W4–5 | Coach on; smoke and heat-€ rules; dashboard; old-phone display app; ask the municipality for a support letter. |
| W6 (Nov 2–6) | Before/after numbers, a backup demo video, the concept and the English pitch. |

**Risks.**
- **Déjà vu.** "A CO₂ monitor" is a classic school project. Never pitch it as one: lead with € and heat, the outside-air check and the upcycled phones.
- **The AI is thin** if the smoke and heat trade-off is dropped.
- **Directors may fear data** that proves the school breaks HN 21. Keep reports internal and framed as improvement.
- **Cheap clone sensors.** Calibrate against one genuine reference sensor.
- **"Why not just buy an Aranet?"** Answer: it works *with* the Aranet; the value is the decision layer.

---

## 🥈 2. HeartSquad: every team a lifesaver squad (Sport & tech, framed as "safe sport")

**What it physically is.** A home-built CPR training torso (~€35–55): plywood plates and springs, a depth sensor and load cells, and an ESP32 talking by Bluetooth to a phone. The phone camera runs pose AI (MediaPipe) that checks locked elbows and shoulders over hands. A PE lesson or team training becomes 20 minutes of CPR practice with a score.

**Who uses it.** PE teachers and youth sport coaches with their teams. The channels are schools, sports schools and clubs, the Red Cross or first-aid trainers, and the Health Ministry's push to put defibrillators in schools and sports halls.

**Why a jury would love it.**
- It starts with a moment everyone remembers: Christian Eriksen collapsing on the pitch at Euro 2020 (details to verify).
- The Health Ministry says Lithuania needs ~10,000 defibrillators and is missing ~9,400 [verified, scout: Alkas.lt Nov 2025]. A defibrillator is useless if nobody starts CPR.
- Teachers have mandatory first aid every 5 years, but **there is no mandatory CPR programme for pupils** [verified absence, judges A/B].
- **The jury itself takes part:** a juror presses, scores 62%, gets coached, scores 90%.

**The proven model it adapts.** Denmark made CPR training mandatory in schools in 2005. Bystander CPR rose from ~20% to 77%, and 30-day survival from ~4% to 16% [verified, scout]. DIY Arduino CPR-feedback devices exist (Hackster, PCBWay), so it is buildable [verified, judge C].

**The demo.** "Who here has done CPR this year?" A juror presses for 20 s. The live gauge shows depth and rate, the AI says "lock your elbows, faster", and the second try scores higher. It needs no network and no water, which makes it the most reliable demo on the list.

**The mini-pilot.** 100–150 students in PE: a pre-test, a 20-minute AI-coached lesson, then a post-test logged automatically with anonymous IDs. Video is processed live and never stored.

**The impact number.** The share of compressions at the correct depth and rate, before vs after, plus a "would you start CPR?" confidence score.

**Build plan.**

| Week | Work |
|---|---|
| W1 | Chest mechanism until ~5 cm ≈ 40–50 kg of force (bathroom-scale test); sensors to a phone web app. |
| W2 | Manikin 1 calibrated; pose checks; 200-student survey. |
| W3 | Manikins 2–3; score formula; **idea form** with a video. |
| W4–5 | PE-lesson pilot; train a small classifier ("leaning", "bouncing", "too shallow") on ~2,000 labelled compressions. |
| W6 | Results and pitch. |

**Risks.**
- **Theme fit.** A juror may say "first aid is not sport". Anchor it on sports halls, teams and athletes' sudden cardiac arrest, and ask the organisers or a mentor before Oct 16.
- **Getting the spring feel right.**
- **The team leans sustainability.** Only pick this if they're genuinely excited.
- **Unverified:** the figure that ~4 in 10 Lithuanians can do CPR.

---

## 🥉 3. RecessBox (PertraukųDėžė): the break-time kit locker (Sport & tech)

**What it physically is.** A lockable box in the schoolyard or lobby (plywood, 12 V solenoid locks, an NFC/QR reader, an ESP32) stocked with balls, ropes and frisbees, ideally donated outgrown gear. An old tablet is the screen. Students open it with their student card or a code.

**What the AI does.** It is not a talking "game master"; judges A and B both called that a gimmick. The AI **learns from the borrowing log** which games and kit actually get used, by which age groups and in what weather. It suggests 3 games that fit ("4 players, corridor, soft ball"), rotates the stock, and gives the school its first real data on active breaks, split by girls and boys.

**Why a jury would love it.**
- **From 1 Sep 2026 every Lithuanian school must have a phone-use procedure, and it bites hardest at breaks** [verified, judge A]. The pitch: **"This September phones left our breaks. Nothing replaced them."**
- A Baltic neighbour hook: Estonia's Schools in Motion covers 46% of Estonian schools; schools offering ≥20 min of active recess rose from 37% to 67% [verified, scout; self-reported].
- Finland's Schools on the Move is in 90%+ of schools; active play at recess rose from 30% to 49% [verified, scout].
- It is a physical object, not another steps app.

**Reach.** The ~700-school health-promoting schools network ("Aktyvi mokykla") and municipal public-health offices [verified, judge B].

**The demo.** A juror taps a card, the screen suggests a game for "4 of us, indoors, raining", and a door clicks open.

**The pilot and impact number.** The share of students observed moving at break, before vs after 2–3 weeks, plus borrowings per day and the share of girls.

**Risks.**
- **Heaviest build of the top 4:** carpentry, locks and an NFC reader (buildability 5/10). Start building in W1 and aim to have it in the corridor by W3.
- **Liability and breakages.** Run it with student "kit captains", outdoors or in the lobby.
- **Weak Samsung link** unless the lock opens with Galaxy phone/Watch NFC and a Galaxy tablet is the screen.
- **Sport**, which the team is lukewarm about.

---

## 4. ShowerCoach (DušoSargas): the shower that shows you the bill (Sustainability, home)

**What it physically is.** A sealed, battery-powered clip-on between the shower hose and the tap: a flow sensor, a temperature probe, an ESP32 and an LED ring or display. It shows litres, kWh and **euro cents ticking up live**, with a forecast after 60 s: "this shower will cost €0.38".

**Why a jury would love it.** Every family has the "get out of the shower!" argument. Hot water costs €6.88–7.99/m³ in Lithuania [verified, scouts]. **The proven model:** a large Swiss field study with the amphiro device found live feedback cut shower water and energy use by **22%**, and the effect didn't fade [verified, scout].

**The pilot.** 6–8 families: a week with the display covered, then two weeks with it on.

**Reach.** Heat utilities and municipal energy-poverty programmes handing devices out, or school library loans. Retail failed: amphiro stopped selling its consumer device [verified, judge B].

**Risks.**
- **The AI is thin.** Keep the per-second cost forecast and an LLM-written weekly tip. **Drop "AI recognises which family member is showering"**: it's a privacy deal-breaker for teens (judge B).
- **Leaks and dead batteries** in real bathrooms.
- **Water on stage:** use a bucket-and-pump rig.
- **Small € per family** (~€2–5/month, unverified). Pitch the percentage and the total for the whole city.

---

## Conditional 5th: the whistle wristband (Sport & tech, inclusion)

A €25 wristband (XIAO ESP32-S3 with a built-in mic) runs a tiny on-device AI trained to hear any referee's whistle over crowd noise and vibrates for deaf and hard-of-hearing players. Earlier solutions (eWhistle, Enforcer) need special referee hardware; this one doesn't.
- **Hook:** Lithuania's men's deaf basketball team won Deaflympics gold in Tokyo 2025 [verified, judge A].
- **Demo:** stadium noise plays, a whistle blows, the juror's wrist buzzes.
- **Go/no-go:** only if the Lithuanian deaf sports association (LKSK) or a deaf athlete partners with the team in week 1. Without that, the team story is not credible.

---

## What changed vs round 3 and why

- Round 3 picked adult, institutional problems (moose, garbage trucks, drainage satellites).
- Round 4's winners are problems **the team lives every day**: the stuffy classroom, empty phone-free breaks, the family shower argument, "none of us could do CPR".
- Each finalist has a **proven model abroad with a number**, a **reliable live demo**, and a **pilot that fits before Nov 6**.

## Verify before the Oct 16 idea form

| Idea | Check | Why |
|---|---|---|
| All | The 2025/26 Baltic 1st and 2nd places (still not found after ~6 searches). The Baltic site suggests last season was sport-themed ("Milano Cortina") [unverified] | If a CO₂ box or CPR kit placed recently, that idea drops sharply |
| Oro sargas | Our own classroom's CO₂ in week 1; whether the town has Sensor.community PM nodes for training data; ask Klaipėda schools that already bought meters | The pitch number; the smoke model; the partner |
| Oro sargas | A source for "short full airing loses less heat than a tilted window" (German Stoßlüften guidance) | The core of the € claim |
| HeartSquad | Ask the organisers/a mentor whether "safe sport / CPR in PE" counts as Sport & tech; verify the "4 in 10 can do CPR" figure and the Eriksen details | Theme risk |
| RecessBox | The share of students with NFC student cards; the school's break lengths; the director's view on liability | Build and pilot feasibility |
| ShowerCoach | Whether any shower-feedback device is sold in LT; the share of flats with individual hot-water meters | Novelty and impact |
| Whistle | Contact LKSK in week 1 | Go/no-go |
