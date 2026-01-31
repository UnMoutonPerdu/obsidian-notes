# Acute Training Load (ATL)

> **Also known as:** Fatigue, Acute Load
>
> **Sources:**
> - Coggan, A. R., & Allen, H. (2010). *Training and Racing with a Power Meter* (2nd ed.). VeloPress.
> - Friel, J. (2015). "The Performance Manager Chart." TrainingPeaks. [Link](https://www.trainingpeaks.com/learn/articles/the-performance-manager-chart/)
> - Banister, E. W. (1991). "Modeling Elite Athletic Performance." *Physiological Testing of Elite Athletes*. Human Kinetics.

**ATL** represents your **fatigue** — the short-term, acute training load accumulated over approximately the past week.

---

## The Concept

Think of ATL as your **fatigue debt:**
- Hard training = ATL spikes (you're tired)
- Rest days = ATL drops quickly (recovering)
- **Higher ATL = more acute fatigue = need more recovery**

ATL is calculated as an **exponentially weighted moving average** of your daily [[Training Stress Score|TSS]] over the past 7 days.

**Key insight:** ATL responds quickly to training changes. Do a big workout and ATL jumps. Take a day off and ATL drops. This makes ATL perfect for tracking short-term fatigue.

---

## The Mathematics

### Exponentially Weighted Moving Average (EWMA)

ATL is calculated using an EWMA with a **time constant of 7 days:**

$$ATL_{today} = ATL_{yesterday} + \frac{TSS_{today} - ATL_{yesterday}}{7}$$

This can also be written as:

$$ATL_{today} = ATL_{yesterday} \times \left(1 - \frac{1}{7}\right) + TSS_{today} \times \frac{1}{7}$$

Or more simply:

$$ATL_{today} = ATL_{yesterday} \times 0.857 + TSS_{today} \times 0.143$$

### What This Means

**Each day:**
- Yesterday's ATL decays by factor of 0.857 (loses ~14.3%)
- Today's TSS contributes 14.3% to new ATL
- Recent workouts dominate, older workouts fade fast

**Compare to [[Chronic Training Load|CTL]] (42-day time constant):**
- CTL daily decay: ~2.4%
- ATL daily decay: ~14.3%
- **ATL changes 6× faster than CTL!**

**This is why ATL is called "fatigue":** It tracks recent training stress that hasn't been absorbed yet.

### Decay Equation

If you stop training completely:

$$ATL_t = ATL_0 \times e^{-t/7}$$

Where:
- $ATL_t$ = ATL after $t$ days
- $ATL_0$ = initial ATL
- $e$ = Euler's number (2.71828...)
- $t$ = days without training

**Example:** ATL starts at 100
- After 1 day off: ATL = 100 × e^(-1/7) = 87
- After 2 days off: ATL = 100 × e^(-2/7) = 75
- After 3 days off: ATL = 100 × e^(-3/7) = 65
- After 7 days off: ATL = 100 × e^(-7/7) = 37
- After 14 days off: ATL = 100 × e^(-14/7) = 14

**ATL drops to ~37% after just one week without training!**

This is why:
- [[Taper Strategy|Tapers]] work (fatigue drops quickly)
- [[Recovery Week]] works (ATL drops while [[Chronic Training Load|CTL]] stays relatively high)
- A few rest days makes you feel fresh again

---

## ATL vs CTL: The Key Difference

| Metric | Time Constant | Represents | Changes | Purpose |
|--------|---------------|------------|---------|---------|
| **CTL** | 42 days | Fitness (chronic load) | Slowly | Long-term training status |
| **ATL** | 7 days | Fatigue (acute load) | Quickly | Short-term recovery needs |

**The relationship:**
$$TSB = CTL - ATL$$

Where **[[Training Stress Balance|TSB]]** (Training Stress Balance) represents your current form/freshness.

**Graphically:**
```
High ATL, Low CTL → Overreaching (fatigued, low fitness)
High ATL, High CTL → Training hard (productive but tired)
Low ATL, Low CTL → Detrained (fresh but unfit)
Low ATL, High CTL → Race ready (fit and fresh!)
```

---

## ATL Ranges and Interpretation

**Absolute ATL numbers are less meaningful than:**
1. ATL relative to CTL (Acute:Chronic ratio)
2. ATL trends (rising, stable, falling)
3. How you feel vs. what ATL shows

**Typical ATL during training:**

| Phase | ATL Range | Interpretation |
|-------|-----------|----------------|
| Easy week | 30-60 | Low fatigue, recovering |
| Moderate week | 60-100 | Building fitness, manageable fatigue |
| Hard week | 100-150 | High fatigue, need recovery soon |
| Peak week | 150-200+ | Very high fatigue, can't sustain long |
| Taper | 20-50 | Shedding fatigue rapidly |

**These ranges depend heavily on athlete's CTL:**
- Elite athlete with CTL 150 can handle ATL 140
- Beginner with CTL 60 would be crushed by ATL 140

---

## Acute:Chronic Ratio (ACR)

**The most important relationship:**

$$ACR = \frac{ATL}{CTL}$$

This ratio indicates if your acute load is appropriate for your fitness base.

### ACR Zones

**< 0.8: Undertraining / Detraining**
- Acute load too low relative to fitness
- Risk of losing fitness
- Might feel stale
- Common during taper (intentional!)

**0.8 - 1.0: Maintenance**
- Acute load matches fitness
- Maintaining current fitness level
- Not really building or losing

**1.0 - 1.3: Optimal Training Zone**
- Acute load appropriately above fitness
- Building fitness through progressive overload
- Manageable fatigue
- **Sweet spot for training!**

**1.3 - 1.5: High Load**
- Acute load significantly above fitness base
- High fatigue accumulation
- Elevated injury/illness risk
- Should be short-term only (peak weeks)

**> 1.5: Danger Zone**
- Acute load far exceeds fitness base
- Very high injury/illness risk
- Overtraining warning
- Immediate recovery needed

### ACR Examples

**Example 1: Safe Training**
- CTL: 80
- ATL: 90
- ACR: 90/80 = **1.13** ✓ Optimal zone

**Example 2: Recovery Week**
- CTL: 80
- ATL: 55
- ACR: 55/80 = **0.69** ✓ Recovering (intentional)

**Example 3: Warning Sign**
- CTL: 70
- ATL: 110
- ACR: 110/70 = **1.57** 🚨 Danger zone!

**Example 4: Peak Week**
- CTL: 110
- ATL: 140
- ACR: 140/110 = **1.27** ⚠️ High but manageable for peak week (short duration)

---

## ATL Through Training Phases

### Loading Weeks

**Goal:** Accumulate training stress to build fitness

**ATL behavior:**
- Rises throughout week as workouts accumulate
- Peak ATL at end of week (weekend)
- Typically ATL > CTL (ACR > 1.0)

**Example [[Loading Week]]:**
- Monday: 75 TSS → ATL rises
- Tuesday: 120 TSS → ATL rises more
- Wednesday: 85 TSS → ATL continues rising
- Thursday: 110 TSS → ATL peaks
- Friday: 70 TSS → ATL stays elevated
- Saturday: 160 TSS → ATL at week maximum
- Sunday: 130 TSS → ATL very high

**By Sunday evening:** ATL might be 120, CTL is 85, ACR = 1.41 (high but acceptable for end of loading week)

---

### Recovery Week

**Goal:** Reduce fatigue while maintaining fitness

**ATL behavior:**
- Drops rapidly due to reduced training
- Falls below CTL (ACR < 1.0)
- By end of week, ATL much lower, CTL only slightly lower

**Example [[Recovery Week]]:**
- Monday: 40 TSS → ATL starts dropping
- Tuesday: 60 TSS → ATL continues dropping
- Wednesday: 50 TSS → ATL falling
- Thursday: 60 TSS → ATL low
- Friday: 30 TSS → ATL very low
- Saturday: 90 TSS → ATL still manageable
- Sunday: 75 TSS → End week with low ATL

**By Sunday evening:** ATL might be 60, CTL dropped from 85 to 82, ACR = 0.73 (recovered!)

**The magic:** ATL dropped 60 points (120→60), CTL only dropped 3 points (85→82).

**Result:** Much fresher (low fatigue) with nearly same fitness!

---

### Taper Period

**Goal:** Maximize freshness for race

**ATL behavior:**
- Plummets due to massive volume reduction
- Drops far below CTL (ACR << 1.0)
- Creates large positive [[Training Stress Balance|TSB]]

**Example 2-week taper:**

**Week -2 (first taper week):**
- Total weekly TSS: 350 (vs 750 in loading)
- ATL drops from 120 → 70

**Week -1 (race week):**
- Total weekly TSS: 200
- ATL drops from 70 → 35

**Race day:**
- ATL: 30-40 (very low fatigue)
- CTL: 95 (slightly dropped from peak 105, but still high)
- ACR: 35/95 = 0.37 (very fresh!)
- [[Training Stress Balance|TSB]]: +65 (extremely fresh!)

**This is why taper works: ATL tanks while CTL only dips slightly.**

---

## Managing ATL in Training

### Daily ATL Monitoring

**Each day, check ATL to answer:**
- Am I accumulating fatigue? (ATL rising)
- Am I recovering? (ATL falling)
- Is my fatigue appropriate for my fitness? (check ACR)

**Red flags:**
- ATL rising for 4+ days straight without planned recovery
- ACR > 1.4 for more than 1 week
- ATL subjectively feels higher than number shows (illness coming?)

### Weekly ATL Pattern

**Typical week structure:**

**Early week (Mon-Tue):**
- ATL relatively low (recovered from weekend)
- Good time for quality sessions

**Mid-week (Wed-Thu):**
- ATL moderate (accumulated some fatigue)
- Can still handle intensity if needed

**Late week (Fri-Sat):**
- ATL elevated (week's training accumulated)
- Friday often easier day

**Weekend (Sat-Sun):**
- Often long/hard workouts
- ATL peaks end of weekend

**Alternative pattern (if you work weekends):**
- Reverse this structure
- Long/hard weekouts during week
- Easier weekends

---

## ATL and Recovery Needs

### How Long to Recover?

**ATL decay equation tells us:**

Starting ATL of 140, how long until ATL drops to 70?

$$70 = 140 \times e^{-t/7}$$
$$0.5 = e^{-t/7}$$
$$ln(0.5) = -t/7$$
$$t = -7 \times ln(0.5) = 7 \times 0.693 = 4.85 \text{ days}$$

**~5 days of very easy training to cut ATL in half.**

**Practical implications:**
- After very hard week: 2-3 easy days brings ATL down significantly
- After moderate week: 1-2 easy days often sufficient
- [[Recovery Week]]: 7 days drops ATL dramatically

### Recovery Day ATL Change

**Zero training:**
$$ATL_{next\ day} = ATL_{today} \times 0.857$$

Starting at ATL 120:
- Day 1 off: 120 × 0.857 = 103 (-17)
- Day 2 off: 103 × 0.857 = 88 (-15)
- Day 3 off: 88 × 0.857 = 75 (-13)

**Three days completely off drops ATL by ~38%**

**Low-stress training (30-40 TSS):**
Slows ATL drop but still allows recovery.

---

## ATL in Multi-Sport Training

### Triathlon Considerations

**Different sports create different fatigue:**
- **Running:** High eccentric load, muscular damage, slower recovery
- **Cycling:** Less impact, faster recovery
- **Swimming:** Very low impact, often restorative

**100 TSS of running ≠ 100 TSS of cycling** in terms of actual fatigue.

**ATL doesn't distinguish!**

**Practical workaround:**
- Monitor ATL by discipline separately if possible
- Pay attention to run TSS especially (most fatiguing)
- Use subjective feel to supplement ATL data

**Example:**
- Total ATL: 95
  - Run ATL: 40 (high for running)
  - Bike ATL: 45
  - Swim ATL: 10

**Risk:** Total ATL looks fine, but run-specific fatigue might be excessive.

### Brick Workouts

**Bike-run bricks affect both disciplines:**
- Bike TSS accumulated first
- Run immediately after (on tired legs)
- **Run portion feels harder than ATL suggests**

**ATL won't capture "pre-fatigued" nature of brick run.**

Solution: Subjective assessment alongside ATL.

---

## ATL Mistakes to Avoid

### Mistake 1: Ignoring High ATL

**Problem:** "ATL is high but I feel fine, I'll keep training hard."

**Reality:** ATL is a leading indicator. You'll feel fine until suddenly you don't (illness/injury).

**Solution:** Respect high ATL (>1.3 ACR), schedule easier days proactively.

---

### Mistake 2: Chasing Yesterday's Fitness

**Problem:** After time off, trying to jump back to old training loads.

**Reality:** CTL dropped, but athlete tries to match old ATL levels → very high ACR → injury.

**Example:**
- Before time off: CTL 100, ATL 110 (ACR 1.10, felt fine)
- After 2 weeks off: CTL 80, ATL 55
- Returns with 750 TSS week → ATL 110
- ACR: 110/80 = **1.38** 🚨 Too high!

**Solution:** Build back gradually, accepting lower ATL initially.

---

### Mistake 3: Ignoring Sport-Specific Fatigue

**Problem:** Total ATL looks fine, but all fatigue is running → injury risk.

**Solution:** Track by discipline if possible, monitor subjective feel.

---

### Mistake 4: Too Much Freshness

**Problem:** Staying in low ATL (ACR < 0.8) too long outside of taper.

**Reality:** Not enough training stimulus → fitness stagnates or declines.

**Solution:** Most training should be ACR 0.9-1.3 range.

---

## ATL and Performance

### Training Performance

**High ATL = reduced performance (expected!):**
- Workouts feel harder at same power/pace
- Can't hit top-end efforts
- Recovery between intervals incomplete

**This is normal during [[Loading Week]].**

**When to worry:**
- Can't complete prescribed workouts multiple days in row
- Performance declining despite rest day
- Resting heart rate elevated >5 bpm
- [[Sleep and Recovery|Sleep]] disrupted

**Solution:** Extra recovery day(s), or full [[Recovery Week]].

### Race Day Performance

**Optimal race day ATL:** Low, but not zero

**Too high ATL (>0.9 ACR):**
- Still carrying fatigue
- Won't perform at potential
- Common mistake: insufficient taper

**Optimal ATL (0.5-0.8 ACR):**
- Fatigue mostly shed
- Still some training residue
- Peak performance zone

**Too low ATL (<0.5 ACR):**
- Extremely fresh
- Risk of "stale" feeling for some athletes
- Most athletes perform well here, but some need slight training stimulus

**Example race day metrics:**
- CTL: 95 (fitness high but not peak)
- ATL: 35 (low fatigue)
- ACR: 35/95 = **0.37** (very fresh)
- [[Training Stress Balance|TSB]]: +60 (positive form)
- **Result:** Peak performance likely!

---

## Advanced: The Physiology

### What Does ATL Actually Represent?

**Physiologically, ATL correlates with:**
1. **Glycogen depletion** (restored within 24-48h)
2. **Neuromuscular fatigue** (CNS fatigue, restored within days)
3. **Hormonal stress** (cortisol, inflammatory markers)
4. **Muscle damage** (especially from running, takes 3-7 days)
5. **Sleep debt** (not captured by ATL, but compounds it)

**ATL is a proxy for accumulated physiological stress not yet recovered from.**

### Why 7 Days?

**The 7-day time constant was empirically derived:**
- Matches typical recovery timelines for most athletes
- Most physiological systems recover within 3-10 days
- 7 days is middle ground

**Individual variation exists:**
- Fast recoverers: may need shorter time constant (5-6 days)
- Slow recoverers: may need longer (8-9 days)
- Most athletes: 7 days works well

**Custom time constants:**
Some software (WKO5, Golden Cheetah) allows custom ATL time constants. Experiment cautiously.

---

## ATL During Special Circumstances

### Illness/Injury

**During illness:**
- Stop training → ATL drops rapidly
- [[Chronic Training Load|CTL]] decays more slowly
- Large gap between CTL and ATL develops

**Returning from illness:**
- Don't try to immediately match old ATL
- Accept lower ATL for 1-2 weeks
- Rebuild gradually (ACR < 1.2)

**Example:**
- Before illness: CTL 90, ATL 95
- After 10 days off: CTL 70, ATL 15
- Week 1 return: 300 TSS → ATL 50, ACR = 0.71 (easy!)
- Week 2: 450 TSS → ATL 75, CTL 73, ACR = 1.03 (good)
- Week 3: 550 TSS → ATL 90, CTL 78, ACR = 1.15 (building safely)

### Life Stress

**ATL doesn't account for:**
- Work stress (big deadline, travel)
- Relationship stress
- Sleep deprivation
- Poor nutrition

**These add "invisible fatigue" on top of ATL.**

**Practical approach:**
- If life stress high, target lower ATL than usual
- If rested and low life stress, can push ATL higher

### Heat/Altitude

**Environmental stress compounds ATL:**
- Same workout at altitude feels harder
- Same workout in heat produces more fatigue

**ATL number doesn't increase, but physiological cost does.**

**Solution:**
- Reduce target ATL when adapting to heat/altitude
- Allow extra recovery time
- Use [[Intensity Factor|IF]] and RPE alongside ATL

---

## Practical ATL Targets

### During Training Blocks

**Week 1 of 3-week block:**
- Target ATL: CTL × 1.05 to 1.15
- Moderate load, building

**Week 2:**
- Target ATL: CTL × 1.10 to 1.20
- Higher load

**Week 3 (if doing 3-week build):**
- Target ATL: CTL × 1.15 to 1.25
- Highest load of block

**Week 4 (recovery):**
- Target ATL: CTL × 0.70 to 0.85
- Drop ATL significantly

**Example with CTL 80:**
- Week 1: Target ATL 88-92 (ACR 1.10-1.15)
- Week 2: Target ATL 92-96 (ACR 1.15-1.20)
- Week 3: Target ATL 96-100 (ACR 1.20-1.25)
- Week 4: Target ATL 56-68 (ACR 0.70-0.85)

### Leading Into Race

**3 weeks out:**
- Peak ATL (highest of training block)
- ACR can be 1.2-1.3

**2 weeks out:**
- Begin taper, ATL starts dropping
- ACR drops to ~1.0

**1 week out:**
- ATL dropping rapidly
- ACR drops to ~0.7

**Race day:**
- ATL very low
- ACR 0.4-0.6
- [[Training Stress Balance|TSB]] highly positive

---

## Tools and Software

**ATL tracking available in:**

1. **TrainingPeaks** (paid)
   - Industry standard
   - Performance Management Chart (PMC)
   - Shows CTL/ATL/TSB

2. **Golden Cheetah** (free)
   - Open source
   - Customizable ATL time constant
   - Full PMC functionality

3. **Intervals.icu** (free)
   - Modern web interface
   - Good PMC implementation

4. **WKO5** (paid)
   - Advanced analytics
   - Customizable models

5. **Today's Plan** (paid)
   - Similar to TrainingPeaks

**Most platforms calculate ATL automatically from uploaded workouts.**

---

## Further Reading

### Books
1. **Allen, H., & Coggan, A. (2019).** *Training and Racing with a Power Meter* (3rd ed.). VeloPress.
   - Detailed PMC explanations
   - ATL/CTL/TSB relationships

2. **Friel, J. (2016).** *The Triathlete's Training Bible* (4th ed.). VeloPress.
   - Practical applications for multisport

### Articles
1. **TrainingPeaks Blog.** "Managing Fatigue with ATL"
   - https://www.trainingpeaks.com/blog/managing-fatigue/

2. **TrainingPeaks Blog.** "Acute:Chronic Workload Ratio"
   - https://www.trainingpeaks.com/blog/how-to-use-acute-chronic-workload-ratio/

### Scientific Papers
1. **Gabbett, T. J. (2016).** "The training—injury prevention paradox." *British Journal of Sports Medicine*, 50(5), 273-280.
   - Acute:Chronic ratio research

2. **Mujika, I., & Padilla, S. (2003).** "Scientific bases for precompetition tapering strategies." *Medicine & Science in Sports & Exercise*, 35(7), 1182-1187.
   - Why ATL drops during taper lead to performance gains

3. **Busso, T. (2003).** "Variable dose-response relationship between exercise training and performance." *Medicine & Science in Sports & Exercise*, 35(7), 1188-1195.
   - Mathematical models of fatigue

---

## Summary

**ATL (Acute Training Load) is your fatigue:**

**The math:**
$$ATL_{today} = ATL_{yesterday} + \frac{TSS_{today} - ATL_{yesterday}}{7}$$

**Key concepts:**
1. **7-day exponentially weighted average** of daily TSS
2. **Higher ATL = more fatigue** (recent training stress)
3. **Changes 6× faster than CTL** (tracks short-term load)
4. **Acute:Chronic Ratio** (ATL/CTL) predicts injury risk:
   - 0.8-1.3 = safe training zone
   - >1.3 = elevated risk
5. **ATL drops quickly** during recovery (to ~37% after 7 days off)
6. **[[Taper Strategy|Taper]] works** because ATL plummets while [[Chronic Training Load|CTL]] stays high
7. **Race day target:** ATL = 0.4-0.6 × CTL (fresh!)

**The bottom line:** ATL tells you if you need recovery NOW. Monitor it daily, keep ACR in safe ranges, and respect high ATL values.

Related: [[Chronic Training Load]], [[Training Stress Balance]], [[Training Stress Score]], [[Recovery Week]], [[Taper Strategy]]
