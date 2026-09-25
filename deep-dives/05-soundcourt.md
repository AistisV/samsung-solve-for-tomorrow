# SoundCourt: AI that lets blind kids play ball games with their sighted classmates

**Theme:** Sport & tech (accessibility) · **One-liner:** *"Lithuania's blind goalball team are Paralympic champions, yet most blind kids sit on the bench in PE. Our phone turns every ball, hoop and teammate into sound."*

---

## 1. The problem
- Children with visual impairments are **significantly less physically active** than their sighted peers, with lower balance and motor skills. Physical activity is exactly what improves their navigation and independence. ([PMC 2024](https://pmc.ncbi.nlm.nih.gov/articles/PMC11282890/), [PMC 2021](https://pmc.ncbi.nlm.nih.gov/articles/PMC8068618/))
- In Lithuania, there's a lack of adapted sport, and kids with disabilities are "still left on the bench" ([Sportas.lt](https://www.sportas.lt/naujiena/542471/vaiku-su-negalia-sporto-uzkulisiai-trenere-atvirai-prabilo-apie-issukius)). Most blind/low-vision kids attend **mainstream schools**, where the PE teacher has no tools; the national centre (LASUC) can only advise them.
- Existing blind sports (goalball, beeper balls) need **special equipment, special courts and all-blind teams**. They separate blind kids from their class instead of including them.
- Local pride hook: **Lithuania's men's goalball team won Paralympic gold (Rio 2016)** and the blind hockey team has multiple Paralympic medals. Blind sport is something Lithuania is great at. ([LRT](https://www.lrt.lt/naujienos/sportas/10/148643/lietuvos-vyru-golbolo-rinktine-parolimpiniu-zaidyniu-cempione))

## 2. The product
- The blind player wears a **phone in a chest harness** (camera forward) and **earbuds with head tracking** (e.g. Galaxy Buds via the Android Spatializer head-tracking API).
- Real-time vision AI (YOLO-class model on the phone) detects the **hoop/goal, the ball and each teammate**, and estimates direction and distance.
- **Spatial audio** places a distinct sound *at* each object in 3D space. Head tracking keeps sounds anchored in the room as the player turns their head. The hoop "hums" where the hoop is; the ball "ticks" faster as it gets closer; teammates have their own tones.
- **Shot feedback:** after a throw, the camera sees where the ball went: *"20 cm left, a little short"*. That's something a beeper on the rim can never do.
- **Mode for PE teachers:** adapted versions of normal games (passing, shooting, tag, relay) that the *whole class* plays with one blind player included. No special court or equipment.

**Collapse test:** a beeper on the rim covers only the static hoop. Moving things (the ball, teammates) and feedback on where your shot went are impossible without the AI. ✅

## 3. Prior art (38.2)
- Navigation sonification for blind people: lots of research (EchoSee, Mobilio in Nature BME 2026, WorldScribe) ([Nature BME](https://www.nature.com/articles/s41551-026-01772-x), [EchoSee](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11351581/)).
- Google **Project Guideline**: AI guides blind runners along a painted line (running only).
- Beeper balls, audio goals: low-tech, static.
- **Gap:** real-time spatial audio for *team ball games in mainstream PE*. We found no product doing this.

## 4. The demo (unforgettable)
**Blindfold a judge. Hand them the ball. They hear the hoop, shoot, and get feedback.** Then a sighted teammate moves and the blindfolded judge passes to them by sound.

## 5. Risks

| Risk | Severity / answer |
|---|---|
| **Latency**: catching a fast ball needs <100 ms end to end. | High for catching. Start with shooting, passing to a stationary teammate, rolling-ball games and running lanes; catching comes later. |
| **Safety**: running blind in a gym full of kids. | Medium: collision warnings are a core feature (the nearest person gets the loudest sound), plus teacher-run adapted rules. |
| Small user group in LT (hundreds of kids, not thousands). | Medium for 38.4. Answer: WHO estimates hundreds of millions of people with vision impairment worldwide; it's scalable everywhere and runs on a normal phone. |
| Monocular distance estimation is imprecise. | Medium: fine for "left/right/near/far"; a known hoop size gives distance. |
| Head-tracking API access: Android's Spatializer handles head tracking for *its own* spatialised playback; getting raw head pose for our own 3D audio engine may not be exposed on every device. | Medium: fall back to the chest phone's own gyroscope (body orientation) + standard binaural rendering. That's good enough for a prototype. |
| Hard to build in 6 weeks. | Medium: shooting mode (hoop + ball + spatial tone) is achievable; team mode is a stage 3 goal. |

## 6. Partners
LASUC (the national centre for blind and visually impaired children, Vilnius), the Lithuanian Blind Sports Federation / goalball team (an ambassador!), the Paralympic Committee, LSU (Sports University).

## 7. Verdict
**81/100.** The most emotional and demo-able sport idea, and the only sport idea that is truly tech-core *and* not obvious. Weaker on local scale (small user group) and harder to build. Pick it if the team is excited by real-time AI + audio and wants the "blindfolded judge" moment.
