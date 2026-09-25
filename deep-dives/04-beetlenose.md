# BeetleNose (*Miško nosis*): sensor nodes that smell and hear a bark-beetle attack before the forest dies

**Theme:** Sustainability · **One-liner:** *"By the time a spruce turns brown, the beetles have already left for the next ten trees. Our €30 sensor smells them in the first week."*

---

## 1. The problem

| Fact | Source |
|---|---|
| The spruce bark beetle (*žievėgraužis tipografas*) destroyed **~1.0 million m³** of Lithuanian spruce in 2023 and ~0.7 M m³ in 2024. | [AM](https://am.lrv.lt/lt/naujienos/zievegrauzis-tipografas-dar-aktyviai-grauzia-egles-del-sausu-oru-dar-tinkamas-metas-jas-isvezti/), [LRT](https://www.lrt.lt/naujienos/mokslas-ir-it/11/2529680/siemet-prognozuojama-dar-didesne-zievegrauzio-tipografo-populiacija) |
| Traps averaged 3,810 beetles each, second only to the 2014 record. The second generation has grown **4 years in a row**; hot, dry summers (climate change) favour new records. | [LRT](https://www.lrt.lt/naujienos/mokslas-ir-it/11/2529680/siemet-prognozuojama-dar-didesne-zievegrauzio-tipografo-populiacija) |
| **255,000 private forest owners** hold ~38% of forests, averaging 3.4 ha. 87% own under 5 ha and manage them only occasionally, so nobody is watching. | [jp.lt](https://jp.lt/lietuvoje-jau-975-tukst-hektaru-privaciu-misku-bet-ne-visi-jie-priziurimi-tinkamai/), [PMSA](https://www.pmsa.lt/apie/privatus-miskai/) |
| **Timing is everything:** young beetles leave a tree 6–10 weeks after the attack. If you remove the tree before that, you kill the brood. If you notice only when the needles turn brown, it's too late. | [Fraunhofer IDMT](https://www.idmt.fraunhofer.de/en/institute/projects-products/projects/detection-bark-beetle-infestation-acoustic-analysis.html) |
| **Satellites see it too late**: freshly attacked "green attack" trees often look unchanged, and vegetation indices can't map them. | [Frontiers 2024](https://www.frontiersin.org/journals/forests-and-global-change/articles/10.3389/ffgc.2024.1445094/full), [review](https://www.sciencedirect.com/science/article/pii/S0378112723008290) |

**The gap:** the tech that sees an attack *early* (sniffer dogs, lab chemistry, trained foresters walking every stand) doesn't scale. The tech that scales (satellites) is late.

## 2. The science we build on (why it's not sci-fi)

1. **Smell.** An attacked spruce releases *several times more* defence volatiles (e.g. α-pinene), and the beetles release an aggregation pheromone to call others. A 2024 Czech study (Frontiers in Forests & Global Change) found **electronic noses can detect the start of an attack within 1 week**, including with the **Bosch BME688**, a ~€20 AI gas-sensor chip. ([Frontiers](https://www.frontiersin.org/journals/forests-and-global-change/articles/10.3389/ffgc.2024.1445094/full))
2. **Sound.** Fraunhofer IDMT recorded infested vs healthy trunks: **168 acoustic events per minute in infested trunks vs 2.6 in healthy ones**. The boring and chewing make "cracking" pulses that AI can pick out. ([Fraunhofer](https://www.idmt.fraunhofer.de/en/institute/projects-products/projects/detection-bark-beetle-infestation-acoustic-analysis.html), [DAGA 2025](https://pub.dega-akustik.de/DAS-DAGA_2025/files/upload/paper/624.pdf))

Both are **research results with no product** that a forest owner can buy. That's our gap.

## 3. The product

**A BeetleNose node** (~€30–40 in parts):
- **BME688** e-nose (gas-scan mode; an on-chip AI model trained on "healthy spruce / attacked spruce / pheromone").
- **MEMS microphone or piezo contact disc** strapped to the trunk; a tiny ML model counts beetle "cracks" per minute.
- ESP32 microcontroller + **LoRa** radio + a small solar panel and battery. Wakes a few times an hour. Runs all season.
- Weather-proof 3D-printed housing.

**Deployment (the clever part):** you don't need a sensor on every tree. Beetles attack **stand edges** (sunny, wind-thrown, freshly cut) and spread **outward from last year's hotspots**. So nodes go where risk is highest:
- the edges of last year's clear-cuts and damage (from the State Forest Service's own data),
- next to pheromone traps (see below),
- in private forests next to known outbreaks.

**Platform:**
- Map + push/SMS alerts to the owner or forester: *"Node #14: attack signature rising for 3 days. Check the 20 spruces within 30 m."*
- Owner walks there, confirms (bore dust at the base of the tree), and removes the tree **before the brood flies out**.
- Every confirmation becomes labelled training data, so the AI improves each season.
- **Bonus feature (a cheap, proven add-on):** a camera in the State Forest Service's pheromone traps automatically counts beetles, replacing manual counting and making the national monitoring network real-time.

## 4. The demo (this is where it wins the room)
- On stage: a spruce log or bark + a **commercial Ips typographus pheromone lure** (the same ones foresters use in traps) + our node.
- The node's display reads "healthy spruce", then we open the pheromone lure next to it, and within seconds to minutes: **"⚠️ bark beetle signature detected"**.
- Play the amplified sound of an infested log (our own recording, or from a partner's research data).
- Map on screen: alerts appear in a simulated forest.

## 5. Why it scores

| Criterion | Why |
|---|---|
| **Tech (38.1, 48.1)** | Collapses without the tech: humans can't smell ppb pheromones or hear larvae. |
| **AI + IoT (48.7)** | Both are core: on-device gas-classification AI + acoustic ML + a LoRa sensor network. |
| **Creativity + research (38.2)** | Turns two 2024–25 research results into a product. We can show we read the science, including its limits. |
| **Local relevance (38.4)** | A Lithuanian national problem: ~1 M m³ per year lost, a record risk, 255k passive private owners, state forests in the news every summer. |
| **Wider impact (38.6, 48.3)** | Carbon sinks, biodiversity, the timber economy. The beetle is devastating Czechia, Germany, Poland, Sweden and Latvia too, so it's instantly transferable across Europe. It could change how the State Forest Service monitors. |
| **Reach (48.6)** | Clear channels: Valstybinių miškų urėdija (state forests; one customer = half the forest), the Private Forest Owners Association, the State Forest Service. |
| **Memorable** | "The box that smells the beetle." |

## 6. Risks (red team) and answers

| Judge / mentor question | Honest answer |
|---|---|
| "Does it work in a real forest with wind and other smells?" | **Unproven at scale.** That's the research frontier (the Czech study says so: above-canopy detection isn't proven yet). That's why we mount nodes *on the trunk / under the canopy*, add acoustics as a second, independent signal, and plan a **spring 2027 field pilot** with foresters. We show the limits honestly. |
| "How many sensors per hectare? Too expensive?" | Targeted placement at risk edges, not a grid. Compare ~€35 per node with a mature spruce worth €100+ and an outbreak patch worth thousands. |
| "It's October. Beetles aren't active; how do you test?" | Lab demo with pheromone lures and fresh vs stressed spruce bark now. The field pilot happens in the flight season (Apr–Aug). Stage 2 judges a concept + prototype, not a finished product. |
| "Why hasn't anyone built it?" | Both detection methods were only published in 2024–25. Research groups publish; nobody has packaged it for a 3-ha owner. |
| "Battery life / connectivity in the forest?" | LoRa reaches kilometres; duty-cycling + solar is proven (LoRa weather stations). |

## 7. Plan & team

| When | What |
|---|---|
| By Oct 16 | Stage 1 form. Order BME688 dev boards (2–3 × ~€20–30), ESP32s, LoRa modules, MEMS mics, and a pheromone lure (from forestry suppliers, or ask the State Forest Service / a forestry district for one). |
| Oct 19–Nov 6 | Train BME688 classes in the lab: clean air / fresh spruce bark / pheromone lure / damaged bark. Build 2 nodes + a map dashboard. Record the acoustics of an infested log (dead and infested spruce is everywhere this year; ask a local forestry district). Email LAMMC Institute of Forestry (Girionys) or the VMU Agriculture Academy for a mentor/letter. |
| Stage 3 | Pilot agreement with a state forest district for spring 2027; improve the model; English pitch. |

**Team:** 1 hardware/firmware (ESP32, sensors) · 1 ML (BME688 AI Studio, acoustic classifier) · 1 app/map · 1 forestry partner + story lead.

**Budget:** ~€150–250 for 2–3 prototype nodes + lure.

## 8. Verdict
**87/100.** The strongest tech-first idea: real science, a real Lithuanian crisis, a hardware demo nobody else will have, and it passes the collapse test completely. Main risk: field performance is unproven. That's acceptable at the concept stage, as long as we say it openly.
