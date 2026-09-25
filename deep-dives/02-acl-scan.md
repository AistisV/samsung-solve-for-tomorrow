# KneeGuard (was "ACL-Scan") — AI coach that keeps teen athletes' knees intact

**Theme:** Sport & tech · **Working one-liner:** *"Every year ~1,000 Lithuanians tear an ACL, most of them young athletes. A 10-minute warm-up cuts that risk by up to 70% in under-18 girls, but nobody does it right. Our phone coach watches and corrects it."*

---

## 1. The problem (evidence)

| Fact | Source |
|---|---|
| ~**1,000 ACL injuries per year** in Lithuania, ~750 surgeries. Most common at ages 15–25; basketball is among the highest-risk sports. | [rimtautasgudas.lt](https://rimtautasgudas.lt/kryzminio-raiscio-plysimas/) |
| Female athletes have ~2–8× higher ACL risk. A Lithuanian example: youth national team player Dalia Belickaitė tore *both* ACLs within a year. | [Krepsinis.net](https://www.krepsinis.net/naujiena/dvieju-sunkiu-traumu-pakirsta-talentinga-lietuvos-krepsininke-bando-atsitiesti-fiziskai-ir-psichologiskai/243781) |
| Neuromuscular-training warm-ups reduce knee injuries in female athletes **≤18 by 72%** (OR 0.28). The effect vanishes after 18, so **the teen years are the window**. | [Myer et al. meta-analysis](https://pmc.ncbi.nlm.nih.gov/articles/PMC4160039/) |
| An ACL tear = surgery + 9–12 months out; many teens never return to sport. | general literature |

## 2. ⚠️ Critical research finding: the original idea is scientifically shaky

The original plan was "phone films a drop jump → AI measures knee valgus → flags high-risk athletes".

- 2D phone video of knee valgus is **reliable** (ICC 0.83–0.99) ([J Sport Rehab](https://pubmed.ncbi.nlm.nih.gov/22104115/)).
- **But** the largest prospective study (Krosshaug et al., 2016, 710 elite female football/handball players) concluded that **"the vertical drop jump is a poor screening test for ACL injuries"**: it does *not* predict who gets injured ([AJSM](https://doi.org/10.1177/0363546515625048)).

A sports-medicine mentor or judge who knows this literature would dismantle the "AI predicts your injury" pitch. So:

## 3. Pivot: coach the prevention, don't predict the injury

What *does* work is the **prevention warm-up itself**, but only when done often and with good technique. Real-world compliance and quality are the weak points: coaches skip it, and athletes do it sloppily.

**KneeGuard:**
1. The phone on a tripod at the side of the gym runs the 10–15 min team warm-up (open programmes such as FIFA 11+ / PEP-style exercises), with video cues.
2. **Pose-estimation AI (MediaPipe/BlazePose, on-device) watches up to 3–4 athletes at a time** and gives live cues: "knees over toes!", "softer landing", "hips back". It scores the landing quality of each repetition.
3. **Weekly "knee-control score"** per athlete: a trend line that shows improvement. That's motivating and educational ("I learned how to land").
4. A coach dashboard shows team compliance (how many sessions, quality trend), so clubs can prove they do injury prevention.
5. Privacy: video never leaves the phone. Only joint angles/scores are stored. Parental consent for under-14s.

## 4. Scoring (revised)

| | T | B | C | Q | L | I | R | D | S | Total |
|---|---|---|---|---|---|---|---|---|---|---|
| Original (screening) | 5 | 5 | 4 | **2** | 4 | 4 | 4 | 4 | 5 | 78 |
| Pivot (coaching) | 5 | 5 | 3 | 4 | 4 | 4 | 4 | 4 | 4 | **80** |

The pivot is more honest, but **novelty drops**: AI form-feedback fitness apps exist (Kemtai, Sency, etc.). The twist (youth *team* ACL prevention, multiple athletes at once, compliance data for clubs) is real but narrower.

## 5. Other weaknesses
- **Theme fit**: it serves kids who *already* do sport. It doesn't address Lithuania's headline problem (only 5% of teens active enough). It fits "safer/more educational sport" rather than "get inactive students moving".
- **Tracking several athletes at once** with phone pose estimation in a gym is hard (occlusion). A demo with one or two athletes is easy; a full team isn't.
- **Medical device regulation**: must be framed as training/education, never diagnosis.

## 6. Partners if chosen
Lithuanian Sports University (LSU, Kaunas; validation partner), Lithuanian Basketball Federation (LKF) youth leagues, sports schools (*sporto mokyklos*), the MKL school basketball league.

## 7. Verdict
**Score ~80.** A solid, impressive-tech sport option, and the best sport idea if the team really wants sport + computer vision. It no longer beats WellWatch: its local problem is narrower and its science had to be walked back.
