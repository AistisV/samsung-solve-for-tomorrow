# LedoSargas / Ice-safe — IoT ice-thickness buoys for safe natural-ice skating

**Theme:** Sport & tech (accessibility) · **One-liner:** *"Lithuania has 3,000 lakes and free ice, but nobody knows if it's safe. Our solar buoys measure the ice every hour and put it on a map."*

## 1. Problem
- Frozen lakes are free, spectacular sport venues (skating, Nordic tour skating, cross-country skiing on ice), but every winter people fall through. Ice drownings make news each season; 46 drownings in H1 2026 overall ([tv3](https://www.tv3.lt/naujiena/lietuva/kol-lietuviai-pramogauja-ant-ledo-gelbetojai-praso-tik-vieno-ispeja-kada-pavojingiausia-n1488850), [jp.lt](https://jp.lt/panevezio-apskrityje-skaudi-pusmecio-statistika-gaisruose-zuvo-4-nuskendo-9-zmones/)).
- The official rule is ≥7 cm for one person and ≥12 cm for a group. **Nobody can see the thickness from the shore.**
- Climate change makes it worse: ice forms later, lasts shorter, and is more often thin and unpredictable ([tv3](https://www.tv3.lt/naujiena/lietuva/klimato-kaita-ezeruose-vanduo-kils-n801689)).

## 2. Solution
- A **solar-powered buoy frozen into the ice** with a **thermistor string** (temperature sensors every 2 cm). The ice/water boundary shows up in the temperature profile, giving thickness. This is the proven method used by Canada's SmartICE ([smartice.org](https://smartice.org/our-smart-technology/)).
- LoRaWAN/NB-IoT → hourly thickness → **public map**: green ≥12 cm, yellow 7–12 cm, red <7 cm, grey = no data.
- Crowd layer: skaters add photos and reports (like Sweden's Skridskonätet) + AI that flags risky patterns (rapid thaw forecast, inflowing streams).
- Distribution: municipalities, the Fire and Rescue Department (PAGD) safety campaigns, schools' winter PE days on the ice.

## 3. Strengths
- **Unforgettable**, visual, tangible hardware: judges will remember "the ice buoy team".
- IoT is the core, not a bolt-on (48.7). Real engineering.
- Both sport accessibility (free outdoor sport) and safety, with a climate-adaptation angle.
- Prior art exists abroad (SmartICE for Arctic sea ice; Skridskonätet for crowd reports), nothing in Lithuania. Good for 38.2.

## 4. Weaknesses (red team)
| Issue | Severity |
|---|---|
| **Liability**: a green map dot = an implicit "safe" promise. Ice varies across a lake; a buoy measures one point. | High. Must be framed as "measured here, at this time" + a rescue-service partnership. |
| **Season fit with the contest**: the final is in December, often before lakes freeze. A live demo on ice is unlikely; we'd demo in a freezer/ice bath. | Medium |
| **Shrinking winters** → judges may ask "why invest in ice?" | Medium. Answer: uncertainty is exactly the danger. |
| **Target group**: ice users are largely adult fishermen, not students. Weak on "get *students* active". | Medium–high |
| Hardware cost per buoy ~€80–150 DIY; a municipality would need dozens. | Low |

## 5. Verdict
**Score ~76.** The most memorable idea on the list and a great hardware showcase, but liability, seasonality and a weak link to *students'* activity hold it back. Worth keeping if the team is hardware-heavy and wants a "wow" project.
