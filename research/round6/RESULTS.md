# Round 6 results: student-centric, shippable by Nov 6

Five researchers ([`BRIEF.md`](BRIEF.md)) produced **~145 ideas**:
- [`gen-school-green.md`](gen-school-green.md): sustainability in the school week
- [`gen-school-sport.md`](gen-school-sport.md): sport from students' own lives
- [`gen-winner-remix.md`](gen-winner-remix.md): remixes of past winners' shapes
- [`gen-younger-peers.md`](gen-younger-peers.md): built for younger kids and left-out classmates
- [`gen-teen-digital.md`](gen-teen-digital.md): hooked onto apps teens already use

Each had to check its top picks against existing products with Lithuanian-language searches.

## The convergence
- **AI lost-and-found with a reuse loop** was the #1 pick of **4 of 5 researchers**, each working independently: Radinukas, Pamestinukai, Radinių lentyna, Pamestukas.
- **"Nobody on the bench" in PE** was the #1 pick of **2 of 5**: Suolelis, Visi žaidžia.

---

## 🥇 Radinukas: the school's lost-and-found that never throws anything away (Sustainability)

**What it is:**
1. Once a week, the caretaker or a student photographs each item in the lost-property box.
2. AI writes an item card: type, colour, size, brand, distinctive marks.
3. Students and parents describe what they lost in plain Lithuanian ("pamečiau juodą Nike džemperį per kūno kultūrą"). The AI matches the description even when the words differ, and notifies them.
4. The link is shared through Tamo/e-dienynas or class chats.
5. **After 30 days, unclaimed items are routed to reuse:** a school swap rail, charity, an AI-written Vinted listing for the class fund, or the textile container. Every kilo is weighed.

**Why it fits the pattern that wins:** every student and parent has lost a hoodie, a bottle or a PE bag, and every school has an overflowing box that gets binned at the end of the year. It's a problem the team lives, with a working app and a channel (the school) built in.

**The demo:** put a real hoodie from your school's pile on stage. Type "lost a black hoodie with a white logo in PE", and it matches. Then show the counter: "this term: X items returned, Y kg kept out of the bin".

**What the AI really does:**
- photo → structured description (a vision model);
- matching of messy, free-text Lithuanian descriptions across different wording, which a keyword search can't do;
- an auto-written reuse listing.

**Build in 2 days:** a web app (Next.js or Flask) with a phone camera upload → a vision-LLM API for the item cards → embedding-based matching for the "I lost…" search → a simple admin page for the caretaker. Mask any name tags, because the ministry's AI guidelines say pupils' personal data should not be uploaded to AI tools [verified: smsm.lrv.lt].

**Traction by Nov 5:**
1. Catalogue your school's real box on Nov 3, and weigh and count it.
2. Send the link to 1–2 classes.
3. Count the claims.
4. Survey 100–150 students ("have you lost something this year? did you get it back?").
5. Get a quote from the caretaker or deputy director.

**Impact number:** the % of found items returned before vs after, plus kg of clothing kept in use.

**Prior art, honestly:**
- **Abroad:** **FindIt** (US) was built by a 15-year-old for a middle school in Bellevue (GeekWire 2025), and LostiFind and FoundFastApp also exist [from the researcher's searches]. They stop at returning the item.
- **Lithuania:** no school solution found in several Lithuanian searches. The searches were weak, so check Google.lt and the app stores yourselves.
- **Past Solve for Tomorrow:** no lost-and-found entry found [1 search; not exhaustive].
- **Your difference:** the reuse loop measured in kg, Lithuanian matching, and the Tamo channel.

**Development plan, which the criteria reward:** the same engine (photo → AI tags → matching → reuse) extends to:
- the **šimtadienis and prom outfit wardrobe** (Proginė spinta: last year's 12th graders lend to this year's);
- **outgrown sports gear** (Išaugau: skates and boots matched to younger kids in a club);
- the June locker clear-out and uniform hand-me-downs.

That makes it "a school circular shelf", not just a lost-property app.

**Risks:**
- **"Is this really sustainability?"** Lead with kg and items kept from waste, not convenience.
- **Small "wow".** The win comes from execution and real data from your own school.
- **The US prior art.** Cite it in your prior-research section (criterion 38.2) and show what you add.

---

## 🥈 Suolelis / Visi žaidžia: nobody on the bench in PE (Sport)

**What it is:** a PE teacher's tablet app.
- Students who can't do today's lesson tap their limitation: exempt, injured, back after illness, asthma, period, a cast, special PE group, little Lithuanian.
- AI picks an adapted variant or a real role (referee, scorer, timekeeper, a set throwing spot) from a teacher-approved list, within the doctor's limits.
- The teacher approves with one tap.
- Newcomers get the rules as a picture strip with Ukrainian audio.

**Why it's good:**
- Students "often sat on a bench or did unrelated tasks" in PE [verified: VGTU study].
- Not liking to change clothes is the first reason for negative attitudes to PE [verified: VU, n=150].
- Since 2024, schools must accept special-needs pupils when parents choose [verified: LRT].
- It's clearly not a "move more" app like last year's winners.

**Traction by Nov 5:** count benched students and minutes in a few PE lessons, survey students, then test the cards in one real lesson with the PE teacher.

**Impact number:** benched minutes per lesson.

**Prior art:** no Lithuanian app found. Teacher courses exist, and one from LSU (the sports university) calls ICT "an underused resource" in PE.

**Risks:**
- It needs the PE teacher on board this week.
- AI-adapted PE tools exist abroad, such as ConnectedPE's adapted-PE tool [from round 1]. Cite them and stress the "real role in the same game" angle.

---

## Other strong options

| Idea | One line | Why it isn't #1 |
|---|---|---|
| **Varva / Gedimų medžiotojai** | Students anonymously photograph waste in the building (running toilets, lights on in empty rooms, windows open with the heating on). AI sorts the reports, merges duplicates and estimates € per year, giving the caretaker a ranked fix list. Channel: Eco-Schools / "Tvari mokykla 2030" (87 schools) | The AI is sorting, not a forecast; close to the city app "Tvarkau miestą" |
| **Kodėl ne KK?** | Anonymous "why do you skip PE?" channel; AI groups the reasons (changing rooms, clothes, grading) into themes and suggests free fixes | The survey *is* the product (great traction), but the tech is thin |
| **Proginė spinta** | A šimtadienis and prom outfit lending wardrobe between grades, with AI matching | Once a year; best as #1's next step |
| **Jaunasis treneris / Kiemo kapitonai** | Teens run break-time games for grades 1–4, with AI game cards | Overlaps with Suolelis's engine |

## Killed in round 6
- A Vinted-alternatives browser extension: Faircado already does it.
- The canteen plate-waste or lunch forecast: Minova won with food waste, and Alytus-region canteens already use smart scales.
- An AI bin-sorting camera: everywhere already.
- A class Secret Santa: DrawNames and Elfster exist.

## Recommendation
**Radinukas.** Four independent researchers converged on it. It matches the pattern that won the last three years, can be built in 2 days, and the traction (your own school's pile) can start tomorrow. If the team would rather do sport, **Suolelis** is the clear alternative.
