# Recommendation (round 2)

> Round 1 picked WellWatch (phone reads nitrate strips). Feedback: *"what's the tech help here?"* That was fair: it failed the **collapse test** (remove the tech and the idea mostly still works). Round 2 restarted from technology. See [`ideas/round2-tech-first.md`](ideas/round2-tech-first.md).

## 🥇 BeetleNose (*Miško nosis*): Sustainability
> *"By the time a spruce turns brown, the beetles have already moved on to the next ten trees. Our €30 sensor smells them in the first week."*

Solar sensor nodes strapped to spruces at high-risk stand edges. A **Bosch BME688 AI e-nose** smells the attack chemistry (tree defence volatiles + beetle aggregation pheromone), and a **microphone hears larvae boring** (168 vs 2.6 "cracks" per minute in infested vs healthy trunks). **LoRa** sends an alert to the forest owner, who removes the tree *before* the brood flies out.

- **What the tech does:** detects things humans physically can't (ppb smells, faint sounds). Satellites only see the damage weeks later. Collapse test ✅.
- **Real science:** a 2024 Czech study found e-noses (including the BME688) detect an attack **within 1 week**; Fraunhofer showed acoustic detection. **Nobody has turned it into a product** for the 255,000 Lithuanian private forest owners.
- **Real crisis:** ~1 million m³ of spruce lost in 2023; beetle populations near record levels.
- **Hardware demo:** open a commercial bark-beetle pheromone lure next to our box on stage and the alert fires.
- **Honest risk:** it isn't proven to work in a real, windy forest at scale. That's the research frontier. Mitigations: sensors sit on the trunk (not above the canopy), smell + sound as two independent signals, and a spring-2027 field pilot with foresters.

Full deep dive: [`deep-dives/04-beetlenose.md`](deep-dives/04-beetlenose.md)

## 🥈 WellWatch 2.0: Sustainability (keeps the original idea, adds real tech)
Instead of photographing strips, **build a €50–80 reagent-free UV-LED nitrate sensor** (nitrate absorbs deep-UV light; published low-cost designs exist). An in-well IoT probe gives continuous data, and a handheld version makes school campaigns precise. Keeps all of round 1's strengths (700k well users, 100% groundwater country, policy hook) and fixes the tech gap. The optics are harder to build, and the demo is less "wow" than BeetleNose.
→ [`deep-dives/01-wellwatch.md` §8](deep-dives/01-wellwatch.md)

## 🥉 SoundCourt: Sport (the best sport idea by far)
Phone camera + AI + **head-tracked spatial audio** turns the hoop, the ball and each teammate into sound, so **blind kids can play ball games with their sighted class**, not in a separate goalball league. Lithuania's blind goalball team are Paralympic champions (Rio 2016). The demo: **blindfold a judge, they shoot a basket by sound.** Weaker on local scale (small user group) and harder real-time engineering.
→ [`deep-dives/05-soundcourt.md`](deep-dives/05-soundcourt.md)

## Also strong: Ice-safe 2.0
Buoys + Stefan's-law physics model + Sentinel-1 satellite → estimated ice thickness for all ~3,000 lakes. Very tech-rich, but has liability and seasonality problems. → [`deep-dives/03-ice-safe.md`](deep-dives/03-ice-safe.md)

## Dropped in round 2
KneeGuard (AI checks exercise form; overused), microplastic scanner (cool tech, unclear "so what"), smoke fingerprinting (ethics), thermal fawn-rescue drones (already mature in Germany), and more. Reasons are in the round-2 table.

---

## How to choose between the top 3
| If the team… | Pick |
|---|---|
| wants the most original tech + a hardware demo + a national-scale problem | **BeetleNose** |
| wants the safest, most provable project (real data from real wells in October) with solid hardware | **WellWatch 2.0** |
| wants sport, emotion, and the most unforgettable live demo | **SoundCourt** |

## Next steps (stage 1 deadline: **Oct 16**)
1. Team picks one (or tells me what feels off, and I'll iterate).
2. I draft the stage 1 idea text (LT + EN).
3. Order parts (BeetleNose: 2–3 BME688 boards, ESP32s, LoRa modules, mics, a pheromone lure; ~€150–250).
4. Contact a mentor: LAMMC Institute of Forestry (Girionys) or VMU Agriculture Academy forestry faculty for BeetleNose; NVSPL/municipal public-health bureau for WellWatch; LASUC for SoundCourt.
