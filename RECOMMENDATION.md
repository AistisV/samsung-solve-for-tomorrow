# Recommendation (round 3: 8 scouts + 4 red-team reviewers)

**Process:** 8 parallel research scouts (energy, water/agri, waste, nature, mobility, sport, global winners, LT policy/deadlines) generated ~200 ideas and filtered them against the team's hard criteria ([`research/round3/BRIEF.md`](research/round3/BRIEF.md)). The top 9 were then attacked by 3 red-team reviewers, each from 4 angles: a skeptical Samsung juror, the real customer, a domain scientist, and the 16-year-old team building it. A 4th "gem hunter" searched all 200 for overlooked ideas and hybrids.

⚠️ **Caveat:** the session's web-search budget (200 calls) ran out mid-research, so parts of the scout reports rely on search snippets or background knowledge. Every file tags claims as verified/unverified. **The "verify this week" lists below matter.**

---

## The final 3

### 🥇 BriedisStop: the thermal-AI "fence-end sentinel" (Sustainability → biodiversity/roads)
**What it physically is:** a pole-mounted box with a thermal camera + an on-device AI (Raspberry Pi/Jetson class) placed where a wildlife fence *ends* or at an underpass. It sees warm bodies day and night, classifies moose/deer/boar, and (stage 2) lights a warning sign **only when an animal is actually there**. Every crossing is logged.

**Who uses it and why:** **Via Lietuva** (the state road agency) spends millions on fences (≈90 km more in 2026) and green bridges, but **doesn't know which ones leak** or where animals go around the fence end. Stage 1 answers that; stage 2 prevents the collision exactly there. One customer, dozens of hotspot units: no "box on every tree".

**Why it's strong:** collisions rose **342 → 1,000/yr (2017→2025)**, €5M+ insured damage, moose ≈ ⅔ of deaths. Animal-detection systems are proven abroad (US, Sweden); ours is a cheap AI version + monitoring. Nature ✔ hardware ✔ AI+IoT ✔ unforgettable demo: *a warm "moose" walks into view → AI labels it → a mini road sign lights up.*

**Honest weaknesses (from the red team):**
- Cheap thermal sensors (MLX90640) are useless beyond ~15 m. You need a 160–256 px core (Lepton 3.5 / 256-px module, ~€200–300, price unverified) aimed at a short, known zone.
- Signs alone reduce speed only a few km/h unless paired with a variable speed limit, so the pitch leads with *monitoring*, then *smart warning + 70 km/h*.
- A 6-week pilot can't show fewer collisions (too rare per site). It shows detection accuracy and false alarms per night.
- **Must check:** does Via Lietuva (or Estonia) already run animal *detection*? If yes, the novelty drops to "cheaper AI + monitoring".

→ [`research/round3/scout-nature.md`](research/round3/scout-nature.md), [`redteam-C-roads.md`](research/round3/redteam-C-roads.md)

### 🥈 HopperGuard: fire alarm for garbage trucks (Sustainability → waste/batteries)
**What it physically is:** a ~€300 box on a garbage truck: a **thermal camera over the hopper** (where waste is compacted) + **cheap gas/heat sensors in the load body**. Crushed lithium batteries and vapes start to smoulder; the box warns the driver before the truck (or later the sorting plant) catches fire. Fire events are mapped by route, showing the city where to put battery collection boxes.

**Who uses it and why:** waste operators (Ecoservice, regional waste centres) whose trucks and plants burn. A few hundred trucks nationally, fitted like a reversing camera.

**Why it's strong:** battery-related fires **12 → 21 → 33 (2023–2025)**, a burned sorting plant (~7,500 m²), a Kaunas CHP bunker fire and a Vilnius truck fire in 2025. EU Battery Regulation: **63% portable-battery collection by 2027**. Proven: Goodyear, AZ uses thermal cameras on trash trucks (2025 safety award). The cleanest collapse test of all: nobody can see inside a compacting hopper. Demo: a hidden warm "battery" in a bin → red alarm.

**Honest weaknesses:** thermal runaway can be delayed minutes to hours, hence the second stage (sensors in the load body). Many batteries are inside bags or devices. **Condition:** by ~Oct 20, a waste operator must share footage/fire data or allow a ride-along; otherwise it drops to MAYBE. Not a "nature" idea.

→ [`scout-waste-circular.md`](research/round3/scout-waste-circular.md), [`redteam-B-urban.md`](research/round3/redteam-B-urban.md)

### 🥉 DrainScope: "Fix or Rewet" (Sustainability → water/climate/farming)
**What it physically is:** software: free **Sentinel-1 radar + Sentinel-2** satellite images + AI that tracks how long every field stays waterlogged after rain/snowmelt. Many fields in one drainage system getting wet together = a **state ditch/collector failure → the municipality's repair list**. One wet field = a private drain → the farmer is notified + pointed to CAP repair grants. A failing system **on peat → "rewet, don't rebuild"** → climate win + EU Nature Restoration Law target.

**Who uses it and why:** municipal drainage specialists (legally must inspect state ditches every ≤3 yrs; the law already uses a ">7 days of pooling" failure sign). **Radviliškis municipality literally published a GovTech Lab challenge asking for this** (Sentinel + AI for drainage); no visible winner.

**Why it's strong:** 2.6 M ha drained, ~74% of drainage worn out; the official map shows 171k ha "poor" vs ~2 M ha per the ministry (a 10× blind spot). Uses 2017–2026 archive data, so a real pilot is possible now. Best policy hook of everything found.

**Honest weaknesses:** the demo is a map (fix: time-lapse + drone footage of a field the official map calls "good" sitting under water). Autumn ploughing confuses radar. **Must check:** was the Radviliškis challenge already solved? Is the state/private split as assumed? Test that a known flooded field actually shows up in the radar data (a 3-day test) before committing.

→ [`scout-water-agri.md`](research/round3/scout-water-agri.md), [`scout-policy.md`](research/round3/scout-policy.md), [`redteam-A-agri.md`](research/round3/redteam-A-agri.md)

---

## Also-rans worth knowing (from the gem hunter, [`redteam-D-gems.md`](research/round3/redteam-D-gems.md))
- **MedžiųSargas**: IR road thermometers on night vehicles map where streets actually freeze → salt only there; soil-salt survey at dying street trees (Vilnius trees dying; salt visible even in summer). Emotive, cheap, real October data. The headline salt number needs winter.
- **Dviračio radaras (ArtiMetras + ice)**: a bike box measures how close cars pass (the new 1 m rule is being debated now) + bike-path ice in winter. The best **sport-theme** option; proven (OpenBikeSensor, Germany).
- **Šernas 360**: hunting clubs' trail cameras + AI give a real wild-boar density (replaces a "pointless" census; African swine fever) + drone crop-damage reports. Strong single user, lower wow.

## Killed in round 3 (with reasons in the files)
ManureWatch (clouds and snow blind the satellite during the ban), ChimneyWatch (condensing boilers look "worst"; neighbour surveillance), SchoolGate (Telraam already exists; idling invisible to a camera), HeatTwin (the AI adds little; the maintainer has no incentive), ActiveLens (the "phone + AI in the gym" pattern), ŽalosDronas standalone (a human with QGIS does most of it), and more.

## Verify-this-week checklist (before the Oct 16 form)
| Idea | Check | Kill switch |
|---|---|---|
| BriedisStop | Via Lietuva already runs animal detection? · thermal core price/availability · a pilot site with deer traffic + power | Detection already deployed widely in LT |
| HopperGuard | An operator agrees to data/ride-along · fire service fire stats by cause · Goodyear details | No operator access by ~Oct 20 |
| DrainScope | Radviliškis challenge status · drainage map + peat layer access · 3-day radar test on a known flooded field | No radar signal / challenge already solved |
