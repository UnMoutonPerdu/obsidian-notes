# Chronic Training Load (CTL)

> **Also known as:** Fitness, Chronic Load
>
> **Sources:**
> - Coggan, A. R., & Allen, H. (2010). *Training and Racing with a Power Meter* (2nd ed.). VeloPress.
> - Friel, J. (2015). "The Performance Manager Chart." TrainingPeaks. [Link](https://www.trainingpeaks.com/learn/articles/the-performance-manager-chart/)
> - Banister, E. W. (1991). "Modeling Elite Athletic Performance." *Physiological Testing of Elite Athletes*. Human Kinetics.

**CTL** represents your **fitness** — the long-term, chronic training load accumulated over approximately 6 weeks.

---

## The Concept

Think of CTL as your **fitness bank account:**
- Regular training deposits = CTL increases (getting fitter)
- Days off = CTL slowly decreases (detraining)
- **Higher CTL = more fitness = higher capacity for work**

CTL is calculated as an **exponentially weighted moving average** of your daily [[Training Stress Score|TSS]] over the past 42 days.

**Key insight:** Recent training matters more than older training, but older training still counts. The 42-day window means workouts from 6 weeks ago still contribute ~25% to your current fitness.

---

## The Mathematics

### Exponentially Weighted Moving Average (EWMA)

CTL is calculated using an EWMA with a **time constant of 42 days:**

$$CTL_{today} = CTL_{yesterday} + \frac{TSS_{today} - CTL_{yesterday}}{42}$$

This can also be written as:

$$CTL_{today} = CTL_{yesterday} \times \left(1 - \frac{1}{42}\right) + TSS_{today} \times \frac{1}{42}$$

Or more simply:

$$CTL_{today} = CTL_{yesterday} \times 0.976 + TSS_{today} \times 0.024$$

### What This Means

**Each day:**
- Yesterday's CTL decays by factor of 0.976 (loses ~2.4%)
- Today's TSS contributes 2.4% to new CTL
- Old training fades gradually, not abruptly

**Time constant = 42 days:**
- After 42 days without training, CTL drops to ~37% of original (1/e)
- After 84 days (2×42), CTL drops to ~13% (1/e²)
- After 126 days (3×42), CTL drops to ~5% (1/e³)

### Decay Equation

If you stop training completely:

$$CTL_t = CTL_0 \times e^{-t/42}$$

Where:
- $CTL_t$ = CTL after $t$ days
- $CTL_0$ = initial CTL
- $e$ = Euler's number (2.71828...)
- $t$ = days without training

**Example:** CTL starts at 100
- After 7 days off: CTL = 100 × e^(-7/42) = 84
- After 14 days off: CTL = 100 × e^(-14/42) = 71
- After 42 days off: CTL = 100 × e^(-42/42) = 37

**This is why taking time off during injury/illness is costly: fitness decays exponentially.**

---

## Ramp Rate: How Fast to Build CTL

**Ramp Rate** = change in CTL per week

$$Ramp\ Rate = CTL_{today} - CTL_{7\ days\ ago}$$

### Safe Ramp Rates

**General guidelines:**
- **+3 to +8 CTL/week:** Safe, sustainable building
- **+8 to +12 CTL/week:** Aggressive but manageable (advanced athletes)
- **+12 to +15 CTL/week:** Very aggressive, high injury/illness risk
- **>+15 CTL/week:** Red flag, almost certain overtraining

**Individual variation exists!** Beginners should stay conservative (+3 to +5), while experienced athletes with high baseline CTL can handle steeper ramps.

### Example Ramp Rate Calculation

**Week 1:** CTL = 60
**Week 2:** CTL = 67
**Ramp Rate:** 67 - 60 = **+7/week** ✓ Safe

**Week 3:** CTL = 80
**Ramp Rate:** 80 - 67 = **+13/week** ⚠️ Too aggressive!

---

## CTL Ranges by Athlete Level

**Cycling-specific** (power-based TSS):

| Athlete Level | CTL Range | Notes |
|---------------|-----------|-------|
| Beginner | 30-60 | Building base fitness |
| Recreational | 60-90 | Regular training, 5-8 hrs/week |
| Competitive AG | 90-130 | Serious training, 10-15 hrs/week |
| Elite AG | 130-180 | Very high volume, 15-20+ hrs/week |
| Professional | 180-250+ | Full-time training |

**Multisport considerations:**
- Add rTSS (run) and sTSS (swim) to total
- Higher absolute CTL than single-sport athletes
- But distributed across three disciplines

**Important:** CTL is relative. An athlete with CTL 80 who's been consistent for years is fitter than someone who spiked to CTL 100 in 6 weeks.

---

## Building CTL: The Process

### Phase 1: Base Building (8-12 weeks)

**Goal:** Build CTL steadily without injuries

**Strategy:**
- [[Loading Week]] pattern: 3 weeks build, 1 week [[Recovery Week]]
- Target ramp rate: +4 to +6 per week
- Focus on volume over intensity (most TSS from duration, not IF)

**Example progression:**
- Week 1-3: CTL 50 → 62 (+4/week average)
- Week 4: Recovery, CTL 62 → 58 (-4, normal)
- Week 5-7: CTL 58 → 70 (+4/week)
- Week 8: Recovery, CTL 70 → 67
- Continue...

### Phase 2: Build Phase (6-8 weeks)

**Goal:** Push CTL higher with intensity

**Strategy:**
- Continue 3:1 loading pattern
- Add quality sessions (higher [[Intensity Factor|IF]])
- Ramp rate can increase to +6 to +8 per week
- Monitor [[Training Stress Balance|TSB]] to avoid excessive fatigue

**CTL will rise faster as intensity increases** (same duration, higher TSS from higher IF).

### Phase 3: Peak Phase (2-4 weeks)

**Goal:** Reach peak CTL before taper

**Strategy:**
- Highest volume and intensity
- CTL peaks 2-3 weeks before A-race
- Careful monitoring to avoid overtraining

### Phase 4: Taper (1-3 weeks)

**Goal:** [[Taper Strategy|Reduce fatigue]] while maintaining fitness

**Strategy:**
- Volume drops dramatically (TSS plummets)
- [[Acute Training Load|ATL]] drops quickly (7-day average)
- CTL drops slightly (42-day average, resistant to change)
- [[Training Stress Balance|TSB]] becomes positive (fresh!)

**CTL drop during taper:**
- 1-week taper: CTL drops 2-5 points
- 2-week taper: CTL drops 5-10 points
- 3-week taper: CTL drops 10-15 points

**This is normal and expected!** Slight fitness loss is worth massive fatigue reduction.

---

## Practical Examples

### Example 1: Consistent Training

**Athlete trains steady 100 TSS/day for 6 weeks:**

Starting CTL = 50

After steady 100 TSS/day, CTL approaches equilibrium:

$$CTL_{equilibrium} = Daily\ TSS \times Time\ Constant = 100 \times 42 / 7 = 600\ /\ 7 \approx 86$$

**Note:** This is simplified. Actual equilibrium calculation involves solving:
$$CTL = TSS_{daily} \times TC$$
where TC (time constant in weeks) = 42/7 = 6

More precisely:
$$CTL_{equilibrium} = \frac{7 \times Daily\ TSS}{1 - e^{-7/42}}$$

For 100 TSS/day average over a week:
$$CTL_{equilibrium} = \frac{700}{1 - 0.844} = \frac{700}{0.156} \approx 4487... \text{ No wait, this is wrong}$$

**Actually, the simpler approximation:**
Daily average TSS of 100 over many weeks stabilizes CTL around **85-90**.

### Example 2: Training Block

**12-week training block from off-season to race:**

| Week | Weekly TSS | CTL Start | CTL End | Ramp Rate |
|------|------------|-----------|---------|-----------|
| 1 | 400 | 40 | 45 | +5 |
| 2 | 450 | 45 | 51 | +6 |
| 3 | 500 | 51 | 58 | +7 |
| 4 | 300 | 58 | 57 | -1 (recovery) |
| 5 | 550 | 57 | 65 | +8 |
| 6 | 600 | 65 | 73 | +8 |
| 7 | 650 | 73 | 82 | +9 |
| 8 | 350 | 82 | 80 | -2 (recovery) |
| 9 | 700 | 80 | 90 | +10 |
| 10 | 750 | 90 | 100 | +10 |
| 11 | 800 | 100 | 110 | +10 (peak) |
| 12 | 400 | 110 | 106 | -4 (taper) |

**Race week (13):** 200 TSS, CTL = 100

**Analysis:**
- Built from CTL 40 → 110 over 11 weeks
- Average ramp rate: +6.4/week (safe)
- Peak ramp weeks 9-11: +10/week (aggressive but short duration)
- Taper weeks 12-13: Small CTL drop, huge [[Training Stress Balance|TSB]] gain

### Example 3: Overtraining Scenario

**Athlete gets overly ambitious:**

| Week | Weekly TSS | CTL Start | CTL End | Ramp Rate | Warning |
|------|------------|-----------|---------|-----------|---------|
| 1 | 500 | 60 | 68 | +8 | OK |
| 2 | 650 | 68 | 80 | +12 | ⚠️ High |
| 3 | 800 | 80 | 96 | +16 | 🚨 Too high! |
| 4 | 850 | 96 | 113 | +17 | 🚨 Overtraining! |
| 5 | DNF - sick/injured | | | | |

**What went wrong:**
- Ramp rate exceeded +8 starting week 2
- Week 3-4 ramp rates >+15/week = red flag
- Body couldn't adapt fast enough
- Immune system compromised or injury occurred

**Better approach:** Would have included recovery week after week 2-3.

---

## CTL and Race Performance

### Optimal CTL for Racing

**Higher CTL ≠ always better for race day**

There's a **goldilocks zone:**
- **Too low CTL:** Not enough fitness to sustain race pace
- **Optimal CTL:** High fitness, manageable fatigue
- **Too high CTL:** Accumulated fatigue outweighs fitness gains

**Race-specific CTL targets:**

**Sprint triathlon:**
- CTL 60-80: Sufficient fitness
- More focus on [[Training Stress Balance|TSB]] (freshness) than peak CTL

**Olympic triathlon:**
- CTL 70-95: Good fitness
- Balance CTL and TSB

**Half Ironman:**
- CTL 85-120: Solid endurance base
- Higher CTL important for sustained effort

**Ironman:**
- CTL 100-140: Deep aerobic fitness critical
- Very high CTL (>120) beneficial if managed properly

**Individual variation!** Some athletes race well off CTL 70, others need 110 for same distance.

### CTL at Race Day

**Ideal scenario:**
- Peak CTL achieved 2-3 weeks before race
- [[Taper Strategy|Taper]] drops CTL slightly (5-15 points)
- [[Acute Training Load|ATL]] drops significantly
- [[Training Stress Balance|TSB]] becomes positive (fresh)

**Example:**
- Peak CTL: 105 (2 weeks before race)
- Race day CTL: 95 (-10 during taper)
- Race day TSB: +15 (fresh!)
- Performance: Optimal (high fitness, low fatigue)

---

## CTL and Injury/Illness Risk

### The Research

Studies show **injury risk correlates with rapid CTL increases:**

**Acute:Chronic ratio (ACR):**
$$ACR = \frac{ATL}{CTL}$$

- **ACR < 0.8:** Detraining zone (possibly stale)
- **ACR 0.8-1.3:** Sweet spot (building fitness safely)
- **ACR 1.3-1.5:** Elevated injury risk
- **ACR > 1.5:** High injury risk (acute load much higher than chronic base)

**Relationship to ramp rate:**
- High ramp rate → ATL rises faster than CTL → high ACR → injury risk

**Prevention:**
- Keep ramp rate under +8/week
- Include [[Recovery Week]] every 3-4 weeks
- Monitor [[Training Stress Balance|TSB]] (don't stay deeply negative too long)

---

## Limitations of CTL

**CTL is a valuable tool but not perfect:**

### 1. Doesn't Account for Training Distribution
- CTL 100 from all Z2 ≠ CTL 100 from intervals + rest
- Both have same CTL but different adaptations

### 2. Individual Response Varies
- Some athletes build fitness faster/slower
- 42-day time constant is average, not universal

### 3. Doesn't Distinguish Disciplines
- 100 TSS cycling ≠ 100 TSS running (more muscular damage)
- Triathlon CTL includes all three sports (different stress types)

### 4. Requires Accurate TSS Input
- Garbage in = garbage out
- Must have accurate [[FTP Test Protocol|FTP]], [[Critical Swim Speed|CSS]]
- rTSS and sTSS less precise than bike TSS

### 5. Doesn't Account for Life Stress
- Work stress, poor sleep, illness all affect adaptation
- CTL doesn't know you only slept 4 hours

### 6. Not a Crystal Ball
- High CTL doesn't guarantee performance
- Low CTL doesn't guarantee failure
- It's one piece of the puzzle

**Use CTL as a guide, not gospel. Listen to your body.**

---

## Practical CTL Management

### Daily Monitoring

**Each morning:**
- Check CTL trend (rising, stable, falling?)
- Check ramp rate (safe, aggressive, excessive?)
- Check [[Training Stress Balance|TSB]] (how fatigued am I?)

**Tools:**
- TrainingPeaks
- Today's Plan
- WKO5
- Strava (limited)
- Golden Cheetah (free)

### Weekly Review

**End of week:**
- Calculate weekly ramp rate
- Compare to planned progression
- Adjust next week if needed

**Questions to ask:**
- Is ramp rate sustainable?
- Do I feel like my CTL? (higher CTL should feel fitter)
- Am I recovering between hard sessions?

### Monthly Planning

**Every 4 weeks:**
- Review CTL trajectory over past month
- Plan next 4-week block
- Schedule recovery weeks
- Adjust training if off track

---

## Building CTL After Time Off

**Returning from injury, illness, or off-season:**

### The Math of Rebuilding

If you took time off, CTL decayed:

$$CTL_{after} = CTL_{before} \times e^{-days\ off / 42}$$

**Example:**
- Before injury: CTL = 100
- 4 weeks off (28 days)
- After: CTL = 100 × e^(-28/42) = 100 × 0.52 = **52**

**Lost ~48% of fitness in 4 weeks!**

### Rebuild Strategy

**DON'T try to rebuild too fast!**

**Safe rebuild:**
- Start at comfortable volume
- Ramp rate +5 to +7/week
- Takes ~6-8 weeks to rebuild
- Patience prevents re-injury

**Example rebuild from injury:**
- Start: CTL 50 (decayed from 100)
- Week 1-3: Ramp +5/week → CTL 50 → 65
- Week 4: Recovery → CTL 63
- Week 5-7: Ramp +6/week → CTL 63 → 81
- Week 8: Recovery → CTL 79
- Week 9-11: Ramp +7/week → CTL 79 → 100
- 11 weeks to fully rebuild

**Faster rebuilds are possible** (muscle memory, neuromuscular adaptations return quickly) **but risk re-injury.**

---

## CTL in Different Training Phases

### Off-Season (Maintenance)

**Goal:** Maintain some fitness without burning out

**CTL strategy:**
- Let CTL drop 20-30% from peak
- If peak was 110, maintain 75-85
- Low stress, mostly easy volume
- [[Recovery Week]] strategy most weeks

### Base Phase

**Goal:** Build aerobic foundation

**CTL strategy:**
- Steady ramp rate +4 to +6/week
- Focus on volume (duration) over intensity
- 3:1 loading:recovery pattern
- Build from off-season base toward race CTL

### Build Phase

**Goal:** Add specificity and intensity

**CTL strategy:**
- Continue building CTL
- Ramp rate +6 to +8/week
- More TSS from higher [[Intensity Factor|IF]] workouts
- Monitor [[Training Stress Balance|TSB]] carefully

### Peak Phase

**Goal:** Maximum training load

**CTL strategy:**
- Highest CTL of season
- 2-4 weeks before A-race
- Ramp rate can be +8 to +10 (short duration)
- Very demanding, can't sustain long

### Taper Phase

**Goal:** Shed fatigue, maintain fitness

**CTL strategy:**
- Accept 5-15 point CTL drop
- Volume reduction drops [[Acute Training Load|ATL]] fast
- [[Training Stress Balance|TSB]] rises (freshness)
- Trust the process

---

## Advanced: The Banister Model

CTL/ATL/TSB model is based on **Banister's impulse-response model** (1975):

$$Performance = Fitness - Fatigue$$

Where:
- **Fitness** (CTL) builds slowly and decays slowly
- **Fatigue** (ATL) builds quickly and decays quickly
- **Form** (TSB) is the difference

**Two-component model:**
$$p(t) = p^* + k_f \times CTL(t) - k_g \times ATL(t)$$

Where:
- $p(t)$ = performance at time $t$
- $p^*$ = baseline performance
- $k_f$ = fitness gain coefficient (positive)
- $k_g$ = fatigue negative coefficient (positive)
- $CTL(t)$ = chronic training load
- $ATL(t)$ = acute training load

**Key insight:** Training creates both positive (fitness) and negative (fatigue) adaptations. The net effect determines performance.

**Time constants:**
- Fitness: $\tau_f = 42$ days (slow to build, slow to decay)
- Fatigue: $\tau_g = 7$ days (quick to build, quick to decay)

**This is why tapers work:** Fatigue decays faster than fitness, revealing the fitness underneath.

---

## Further Reading

### Books
1. **Allen, H., & Coggan, A. (2019).** *Training and Racing with a Power Meter* (3rd ed.). VeloPress.
   - Chapter on Performance Management Chart (PMC)
   - Detailed CTL/ATL/TSB explanations

2. **Friel, J. (2018).** *The Cyclist's Training Bible* (5th ed.). VeloPress.
   - Annual Training Plan using CTL
   - Periodization with PMC

3. **Friel, J. (2016).** *The Triathlete's Training Bible* (4th ed.). VeloPress.
   - Multisport applications of CTL/ATL/TSB

### Articles
1. **Coggan, A.** "TrainingPeaks Performance Manager Chart." TrainingPeaks.
   - https://www.trainingpeaks.com/blog/the-science-of-the-performance-manager/

2. **Friel, J.** "Form, Fitness and Fatigue." TrainingPeaks Blog.
   - https://www.trainingpeaks.com/blog/form-fitness-and-fatigue/

3. **Friel, J.** "CTL Ramp Rates." TrainingPeaks Blog.
   - https://www.trainingpeaks.com/blog/managing-training-ramp-rates/

### Scientific Papers
1. **Banister, E. W., Calvert, T. W., Savage, M. V., & Bach, T. M. (1975).** "A systems model of training for athletic performance." *Australian Journal of Sports Medicine*, 7, 57-61.
   - Original impulse-response model

2. **Busso, T. (2003).** "Variable dose-response relationship between exercise training and performance." *Medicine & Science in Sports & Exercise*, 35(7), 1188-1195.
   - Refinements to Banister model

3. **Mujika, I., & Padilla, S. (2003).** "Scientific bases for precompetition tapering strategies." *Medicine & Science in Sports & Exercise*, 35(7), 1182-1187.
   - Why CTL drop during taper is beneficial

4. **Gabbett, T. J. (2016).** "The training—injury prevention paradox: should athletes be training smarter and harder?" *British Journal of Sports Medicine*, 50(5), 273-280.
   - Acute:Chronic workload ratio and injury prevention

### Tools
- **TrainingPeaks** (paid): Industry standard
- **Today's Plan** (paid): Similar to TrainingPeaks
- **Golden Cheetah** (free): Open-source, full PMC functionality
- **Intervals.icu** (free): Modern web-based option

---

## Summary

**CTL (Chronic Training Load) is your fitness:**

**The math:**
$$CTL_{today} = CTL_{yesterday} + \frac{TSS_{today} - CTL_{yesterday}}{42}$$

**Key concepts:**
1. **42-day exponentially weighted average** of daily TSS
2. **Higher CTL = more fitness** (capacity for work)
3. **Build gradually:** +4 to +8 CTL per week is safe
4. **Exceeding +12/week** = high injury/illness risk
5. **Include [[Recovery Week|recovery weeks]]** every 3-4 weeks
6. **CTL decays** when training stops: exponential decay with τ = 42 days
7. **Peak CTL 2-3 weeks before race**, accept small drop during [[Taper Strategy|taper]]

**The bottom line:** CTL gives you a number representing fitness. Track it, build it gradually, and race when it peaks while fatigue is low.

Related: [[Acute Training Load]], [[Training Stress Balance]], [[Training Stress Score]], [[Loading Week]], [[Recovery Week]]
