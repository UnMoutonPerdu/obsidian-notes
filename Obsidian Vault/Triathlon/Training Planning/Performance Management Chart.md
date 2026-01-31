# Performance Management Chart (PMC)

> **Sources:**
> - Coggan, A. R., & Allen, H. (2010). *Training and Racing with a Power Meter* (2nd ed.). VeloPress.
> - Friel, J. (2015). "The Performance Manager Chart." TrainingPeaks. [Link](https://www.trainingpeaks.com/learn/articles/the-performance-manager-chart/)
> - Allen, H., & Coggan, A. (2006). "Training and racing using a power meter: an introduction." *Cycling Coaching*.

**The Performance Management Chart (PMC)** is a systematic approach to training planning that uses three metrics to optimize fitness, manage fatigue, and predict performance.

**The three metrics:**
1. **[[Chronic Training Load|CTL]]** - Chronic Training Load (Fitness)
2. **[[Acute Training Load|ATL]]** - Acute Training Load (Fatigue)
3. **[[Training Stress Balance|TSB]]** - Training Stress Balance (Form)

---

## The Foundation: The Banister Model

The PMC is based on Dr. Eric Banister's **Fitness-Fatigue model** (1975):

$$Performance = Fitness - Fatigue + Baseline$$

**Key insight:** Training creates two simultaneous effects:
1. **Positive effect (Fitness):** Builds slowly, decays slowly
2. **Negative effect (Fatigue):** Builds quickly, decays quickly

**Net performance** depends on the balance between these two effects.

### Mathematical Model

$$p(t) = p_0 + k_1 \sum w(t-i) \cdot e^{-(t-i)/\tau_1} - k_2 \sum w(t-i) \cdot e^{-(t-i)/\tau_2}$$

Where:
- $p(t)$ = performance at time $t$
- $p_0$ = baseline performance
- $w(t-i)$ = training load on day $i$ (TSS)
- $k_1$ = fitness gain coefficient
- $k_2$ = fatigue impact coefficient
- $\tau_1 = 42$ days (fitness time constant)
- $\tau_2 = 7$ days (fatigue time constant)

**In PMC terms:**
- First term with $\tau_1 = 42$ → **CTL** (fitness)
- Second term with $\tau_2 = 7$ → **ATL** (fatigue)
- Difference → **TSB** (form)

**The genius:** Two exponentially weighted moving averages with different time constants capture the dual nature of training adaptation.

---

## The Three Metrics Explained

### CTL: Chronic Training Load (Fitness)

$$CTL_{today} = CTL_{yesterday} + \frac{TSS_{today} - CTL_{yesterday}}{42}$$

**Represents:** Long-term training load (≈6 weeks)

**Key characteristics:**
- Slow to build, slow to decay
- Higher CTL = more fitness
- Safe ramp rate: +5 to +8 per week
- Dangerous ramp rate: >+12 per week

**Think:** Your fitness bank account.

📖 **Full details:** [[Chronic Training Load]]

---

### ATL: Acute Training Load (Fatigue)

$$ATL_{today} = ATL_{yesterday} + \frac{TSS_{today} - ATL_{yesterday}}{7}$$

**Represents:** Short-term training load (≈1 week)

**Key characteristics:**
- Fast to build, fast to decay
- Higher ATL = more fatigue
- Changes 6× faster than CTL
- Safe zone: ATL/CTL ratio 0.8-1.3

**Think:** Your fatigue debt.

📖 **Full details:** [[Acute Training Load]]

---

### TSB: Training Stress Balance (Form)

$$TSB = CTL - ATL$$

**Represents:** Current form/freshness

**Key characteristics:**
- Negative TSB = fatigued (training mode)
- Positive TSB = fresh (racing mode)
- Target for racing: +15 to +35
- Target for training: -15 to -35

**Think:** The net effect - are you ready to perform?

📖 **Full details:** [[Training Stress Balance]]

---

## Visual Representation

The PMC displays all three metrics on one chart:

```
             PMC Example
TSS
200 |     ●                    ← Daily TSS (bars)
150 |   ● ● ●
100 | ● ● ● ● ●
 50 |● ● ● ● ● ●
────┼────────────────────────
CTL |      ↗↗↗↗↗              ← CTL (blue line, slow rise)
100 |    ↗
 80 |  ↗
 60 |↗
────┼────────────────────────
ATL |    ↗↗↗ ↘↘               ← ATL (pink line, quick changes)
120 |   ↗   ↘
100 | ↗       ↘
 80 |↗         ↘
────┼────────────────────────
TSB |     ↘↘↘ ↗↗              ← TSB (yellow line, inverse of ATL trend)
+20 |          ↗
  0 |        ↗
-20 |     ↘↘
-40 |   ↘
────┴────────────────────────
    Training → Recovery
```

**Reading the chart:**
- **TSS bars:** Daily training stress (input)
- **CTL line:** Fitness trend (slow-moving)
- **ATL line:** Fatigue trend (fast-moving)
- **TSB line:** Form (CTL - ATL)

---

## Using the PMC for Training Planning

### Annual Training Plan Structure

**Off-Season (8-12 weeks):**
- **Goal:** Rest, recover, maintain base fitness
- **CTL:** Let drop 20-30% from peak season
- **ATL:** Low and variable
- **TSB:** Mostly positive

**Base Phase (12-16 weeks):**
- **Goal:** Build aerobic foundation
- **CTL:** Steady increase (+4 to +6/week)
- **ATL:** Moderate, following 3:1 loading pattern
- **TSB:** Slightly negative (-10 to -25)

**Build Phase (8-12 weeks):**
- **Goal:** Add intensity and specificity
- **CTL:** Continue building (+6 to +8/week)
- **ATL:** Higher, more variable (quality sessions)
- **TSB:** Moderately negative (-20 to -35)

**Peak Phase (2-4 weeks):**
- **Goal:** Maximum training stimulus
- **CTL:** Highest of season
- **ATL:** Very high
- **TSB:** Most negative (-30 to -50)

**Taper (1-3 weeks):**
- **Goal:** Shed fatigue, maintain fitness
- **CTL:** Small decline (5-15 points)
- **ATL:** Rapid decline
- **TSB:** Rise to positive (+15 to +35)

**Race:**
- **CTL:** Near peak (95-105% of peak)
- **ATL:** Low (30-50)
- **TSB:** Positive (+15 to +35)

---

## The 3:1 Loading Pattern

**Most effective training structure:**

**3 weeks progressive loading + 1 week recovery**

### Week-by-Week Breakdown

**Week 1 (Load):**
- TSS: 700
- CTL: 75 → 80 (+5)
- ATL: 85 → 95
- TSB: -10 → -15

**Week 2 (Load):**
- TSS: 750
- CTL: 80 → 86 (+6)
- ATL: 95 → 105
- TSB: -15 → -19

**Week 3 (Load - Highest):**
- TSS: 800
- CTL: 86 → 93 (+7)
- ATL: 105 → 115
- TSB: -19 → -22

**Week 4 (Recovery):**
- TSS: 450
- CTL: 93 → 91 (-2, small drop)
- ATL: 115 → 75 (large drop!)
- TSB: -22 → +16 (big improvement!)

**Result after 4-week block:**
- CTL increased: 75 → 91 (+16 over 4 weeks)
- TSB recovered: Ready for next block
- Average ramp rate: +4/week (safe and sustainable)

### Why 3:1 Works

**3 weeks loading:**
- Provides sufficient stimulus for adaptation
- Accumulates fatigue progressively
- Builds CTL steadily

**1 week recovery:**
- ATL drops rapidly (7-day time constant)
- CTL barely drops (42-day time constant)
- TSB improves dramatically
- Supercompensation occurs

**Pattern can be repeated multiple times** through season.

---

## Practical Example: 16-Week Build to Race

**Starting point:** CTL 60, off-season maintenance

**Goal:** Peak at CTL 100-105, race at TSB +25

### Weeks 1-4: Base Block 1

| Week | Weekly TSS | CTL | ATL | TSB | Ramp Rate |
|------|-----------|-----|-----|-----|-----------|
| 1 | 500 | 60→66 | 75 | -9 | +6 |
| 2 | 550 | 66→72 | 82 | -10 | +6 |
| 3 | 600 | 72→78 | 90 | -12 | +6 |
| 4 | 350 | 78→77 | 60 | +17 | -1 |

**Block summary:** CTL +17, ready for next block

---

### Weeks 5-8: Base Block 2

| Week | Weekly TSS | CTL | ATL | TSB | Ramp Rate |
|------|-----------|-----|-----|-----|-----------|
| 5 | 600 | 77→84 | 85 | -1 | +7 |
| 6 | 650 | 84→91 | 93 | -2 | +7 |
| 7 | 700 | 91→98 | 102 | -4 | +7 |
| 8 | 400 | 98→96 | 68 | +28 | -2 |

**Block summary:** CTL +19, now at 96

---

### Weeks 9-12: Build Block (With Intensity)

| Week | Weekly TSS | CTL | ATL | TSB | Ramp Rate |
|------|-----------|-----|-----|-----|-----------|
| 9 | 700 | 96→103 | 98 | +5 | +7 |
| 10 | 750 | 103→110 | 108 | +2 | +7 |
| 11 | 800 | 110→118 | 118 | 0 | +8 |
| 12 | 450 | 118→115 | 78 | +37 | -3 |

**Block summary:** CTL +19, peak CTL 118

---

### Weeks 13-16: Peak + Taper

| Week | Weekly TSS | CTL | ATL | TSB | Notes |
|------|-----------|-----|-----|-----|-------|
| 13 | 750 | 115→120 | 108 | +12 | Peak week |
| 14 | 500 | 120→116 | 85 | +31 | Taper begins |
| 15 | 300 | 116→110 | 55 | +55 | Deep taper |
| 16 | 150 | 110→105 | 35 | +70 | Race week |

**Race day:** CTL 105, ATL 35, TSB +70

**Analysis:**
- Peak CTL: 120 (week 13)
- Race CTL: 105 (-15 from peak, acceptable)
- Race TSB: +70 (very fresh, might be slightly over-tapered for some)
- Alternative: Could do 400 TSS in week 15 → TSB +50 on race day

---

## Reading PMC Patterns

### Pattern 1: Healthy Training

```
CTL: Steadily rising with slight dips in recovery weeks
ATL: Sawtooth pattern (rise and fall with loading/recovery)
TSB: Oscillates negative (loading) to less negative (recovery)
```

**This is ideal.** Progressive overload with adequate recovery.

---

### Pattern 2: Overtraining Risk

```
CTL: Rising very steeply (>+10/week sustained)
ATL: Consistently above CTL
TSB: Increasingly negative (<-50), no recovery
```

**Red flags:**
- Excessive ramp rate
- No recovery weeks
- TSB deeply negative for extended period

**Action needed:** Immediate recovery week or time off.

---

### Pattern 3: Detraining

```
CTL: Declining
ATL: Low or declining
TSB: Positive and rising
```

**Could indicate:**
- Off-season (intentional)
- Injury/illness (unintentional)
- Insufficient training stimulus

**If unintentional:** Need to increase training load.

---

### Pattern 4: Perfect Taper

```
CTL: Slight decline (5-15 points)
ATL: Rapid decline
TSB: Sharp rise from negative to positive
```

**Exactly what you want before race!**

---

## Acute:Chronic Workload Ratio

**Critical metric derived from PMC:**

$$ACR = \frac{ATL}{CTL}$$

### ACR and Injury Risk

Research (Gabbett, 2016) shows strong correlation between ACR and injury:

| ACR Range | Injury Risk | Interpretation |
|-----------|-------------|----------------|
| < 0.8 | Low | Undertraining/detraining |
| 0.8 - 1.0 | Low | Maintenance |
| 1.0 - 1.3 | Low-Medium | Optimal training zone |
| 1.3 - 1.5 | Medium-High | Elevated risk |
| 1.5 - 2.0 | High | High risk |
| > 2.0 | Very High | Extreme risk |

**The "sweet spot":** ACR between 1.0 and 1.3

**At this ratio:**
- Acute load appropriately above chronic base
- Progressive overload achieved
- Injury risk minimized

### Managing ACR

**During loading weeks:**
- ACR will rise (1.1-1.3)
- Acceptable for 2-3 weeks
- Monitor for exceeding 1.3

**During recovery week:**
- ACR drops (<1.0, often 0.7-0.9)
- Resets the ratio
- Prepares for next loading block

**During peak week:**
- ACR may spike to 1.3-1.5
- Short duration (1 week max)
- Taper follows immediately

**Red flag:** ACR > 1.5 for more than 1 week

---

## PMC for Multi-Sport Athletes

### Triathlon Challenges

**Three sports = three TSS sources:**
- Bike TSS (most precise, power-based)
- Run TSS (estimated from pace/HR)
- Swim TSS (estimated from pace)

**Problem:** Not all TSS is equal
- 100 run TSS ≠ 100 bike TSS in terms of actual fatigue
- Running creates more muscular damage
- Swimming is less fatiguing than running

### Workarounds

**Option 1: Total TSS (Most Common)**
- Sum all three sports
- Simple, single PMC
- Doesn't distinguish sport-specific fatigue

**Option 2: Sport-Specific PMC**
- Separate CTL/ATL/TSB for each sport
- More complex but more accurate
- Can identify sport-specific overload

**Option 3: Weighted TSS**
- Multiply run TSS by 1.2-1.5 (higher impact)
- Multiply swim TSS by 0.8-0.9 (lower impact)
- Keep bike TSS as 1.0
- More accurate total load

**Most triathletes use Option 1** (total TSS) with awareness of limitations.

---

## Common PMC Mistakes

### Mistake 1: Chasing Numbers

**Problem:** Fixating on hitting specific CTL targets without considering overall readiness.

**Reality:** CTL 100 with poor recovery << CTL 90 with good recovery.

**Solution:** Use PMC as guide, not gospel. Factor in subjective markers:
- [[Sleep and Recovery]] quality
- Resting heart rate
- Mood and motivation
- Workout performance

---

### Mistake 2: Ignoring Sport Differences

**Problem:** 800 TSS week looks fine, but 400 is running.

**Reality:** Run-heavy load = higher injury risk than bike-heavy equivalent TSS.

**Solution:** Monitor distribution. Don't spike run TSS >10% per week.

---

### Mistake 3: No Recovery Weeks

**Problem:** "I feel fine, I'll skip recovery week."

**Reality:** Cumulative fatigue masked by day-to-day variance. Eventually crashes.

**Solution:** Schedule recovery weeks proactively (every 3-4 weeks), even if you "feel good."

---

### Mistake 4: Over-Reliance on PMC

**Problem:** PMC says TSB +25, must be ready to race!

**Reality:** PMC doesn't know about:
- Recent illness
- Life stress
- Poor sleep
- Nutrition issues

**Solution:** PMC + subjective feel + other metrics = complete picture.

---

## Software and Tools

### Commercial Options

**TrainingPeaks** (industry standard)
- Full PMC functionality
- Integration with all devices
- Coaching features
- $60-130/year

**Today's Plan**
- Similar to TrainingPeaks
- Good PMC charts
- $10-20/month

**WKO5**
- Advanced analytics
- Customizable models
- One-time $129-229

### Free Options

**Golden Cheetah**
- Open source
- Full PMC functionality
- Customizable time constants
- 100% free

**Intervals.icu**
- Web-based
- Clean PMC implementation
- Free tier available

**Strava** (limited)
- Shows fitness/fatigue (similar to CTL/ATL)
- Less detailed than dedicated tools
- Free/premium

---

## Setting Up Your PMC

### Step 1: Gather Historical Data

**Minimum:** 6 weeks of training data
**Better:** 12+ weeks
**Ideal:** 6+ months

**Upload past workouts** to establish baseline CTL/ATL.

---

### Step 2: Establish FTP/CSS

**Critical for accurate TSS:**
- [[FTP Test Protocol|Test FTP]] for cycling
- [[Critical Swim Speed|Test CSS]] for swimming
- Estimate threshold for running

**Without accurate thresholds, TSS is meaningless.**

---

### Step 3: Review Current Status

**Check your current numbers:**
- CTL: What's your fitness level?
- ATL: Are you fatigued?
- TSB: Are you fresh or tired?
- Ramp rate: How fast have you been building?

---

### Step 4: Plan Forward

**Work backwards from race:**
- Race date: Target TSB +20 to +30
- 1 week before: Start taper
- 2-3 weeks before: Peak CTL
- 12-16 weeks before: Progressive build

**Use 3:1 pattern** for loading/recovery structure.

---

### Step 5: Monitor and Adjust

**Weekly review:**
- Did you hit target TSS?
- Is ramp rate appropriate?
- How do you feel vs. what PMC shows?
- Adjust next week if needed

---

## Advanced: Individual Response

### Personalizing Time Constants

**Standard:**
- CTL: 42 days
- ATL: 7 days

**Some athletes respond better to:**
- Faster CTL decay: 35-38 days (build/lose fitness faster)
- Slower CTL decay: 45-50 days (maintain fitness longer)
- Faster ATL decay: 5-6 days (recover quickly)
- Slower ATL decay: 8-10 days (need more recovery)

**Experiment cautiously.** Standard values work for 90% of athletes.

---

### Modeling Performance

**Advanced software (WKO5) can predict performance** from PMC:

$$Performance\ Index = k_1 \times CTL - k_2 \times ATL + baseline$$

Where $k_1$ and $k_2$ are individualized coefficients derived from your past performance data.

**Example:**
- Race PRs occurred at: CTL 95-105, TSB +20 to +30
- Model learns: optimal performance = CTL ~100, TSB ~+25
- Predicts future performance at different CTL/TSB combinations

**Requires significant data** (multiple races across different CTL/TSB points).

---

## Integration with Training Plan

### Macro Level (Annual Plan)

**PMC guides periodization:**
1. Off-season: CTL decline by design
2. Base: CTL building (volume focus)
3. Build: CTL continues (add intensity)
4. Peak: CTL maximum
5. Taper: ATL drops, TSB rises
6. Race: Optimal CTL/ATL/TSB balance

---

### Meso Level (Monthly)

**PMC guides 3:1 pattern:**
- 3 weeks: TSB negative (building)
- 1 week: TSB less negative (recovering)
- Repeat with rising CTL

---

### Micro Level (Weekly)

**PMC guides daily decisions:**
- TSB very negative: Easy day
- TSB moderately negative: Train as planned
- TSB positive: Good for quality

---

## Further Reading

### Books

1. **Allen, H., & Coggan, A. (2019).** *Training and Racing with a Power Meter* (3rd ed.). VeloPress.
   - Definitive guide to PMC
   - Chapter dedicated to CTL/ATL/TSB

2. **Friel, J. (2018).** *The Cyclist's Training Bible* (5th ed.). VeloPress.
   - Annual Training Plan using PMC

3. **Friel, J. (2016).** *The Triathlete's Training Bible* (4th ed.). VeloPress.
   - Multisport applications

### Scientific Papers

1. **Banister, E. W., Calvert, T. W., Savage, M. V., & Bach, T. (1975).** "A systems model of training for athletic performance." *Australian Journal of Sports Medicine*, 7, 57-61.
   - Original fitness-fatigue model

2. **Busso, T. (2003).** "Variable dose-response relationship between exercise training and performance." *Medicine & Science in Sports & Exercise*, 35(7), 1188-1195.
   - Refinements and validation

3. **Gabbett, T. J. (2016).** "The training—injury prevention paradox: should athletes be training smarter and harder?" *British Journal of Sports Medicine*, 50(5), 273-280.
   - Acute:Chronic workload ratio research

4. **Mujika, I., & Padilla, S. (2003).** "Scientific bases for precompetition tapering strategies." *Medicine & Science in Sports & Exercise*, 35(7), 1182-1187.
   - Taper research (why TSB rise works)

### Online Resources

1. **TrainingPeaks University**
   - https://university.trainingpeaks.com/
   - Free courses on PMC

2. **TrainingPeaks Blog - PMC Series**
   - https://www.trainingpeaks.com/blog/category/performance-management/
   - Articles by Coggan, Friel, Allen

3. **Golden Cheetah Wiki**
   - https://github.com/GoldenCheetah/GoldenCheetah/wiki
   - Technical documentation

---

## Summary

**The Performance Management Chart is a systematic framework for training optimization:**

### The Three Metrics

1. **[[Chronic Training Load|CTL]]** (Fitness)
   - 42-day exponentially weighted average
   - Build at +5 to +8 per week
   - Higher = more fitness

2. **[[Acute Training Load|ATL]]** (Fatigue)
   - 7-day exponentially weighted average
   - Changes 6× faster than CTL
   - Higher = more tired

3. **[[Training Stress Balance|TSB]]** (Form)
   - CTL - ATL
   - Negative during training (building fitness)
   - Positive for racing (fresh)

### The Formula for Success

**Build CTL gradually** (3:1 loading pattern)
↓
**Manage ATL carefully** (ACR 0.8-1.3 most of the time)
↓
**Manipulate TSB strategically** (taper for positive TSB)
↓
**Race at optimal point** (high CTL, low ATL, positive TSB)
= **Peak Performance**

**The PMC doesn't guarantee performance, but it does guarantee systematic, data-driven training progression.**

Related: [[Chronic Training Load]], [[Acute Training Load]], [[Training Stress Balance]], [[Training Stress Score]], [[Loading Week]], [[Recovery Week]], [[Taper Strategy]]
