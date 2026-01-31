# Normalized Power (NP)

**NP** is a metric that solves the problem inherent to Average Power (**AP**).

---

## The Problem with Average Power

**AP** is nothing more than:
$$AP = \frac{1}{T}\sum P(t)$$

Globally it's just the average power you generated during your workout. But let's take a look at some workout examples:

- **Ride A:** Steady 200W for one hour
- **Ride B:** 30s at 350W, 30s at 50W, for one hour

$$\rightarrow$$ Same average power for a **completely** different fatigue.

**Why is this a problem?**

Physiological cost increases **non-linearly** with intensity. A few seconds at 350W costs you much more than the "recovery" at 50W gives you back.

**AP doesn't take into account the non-linearity of body response to power.**

---

## What is Normalized Power?

An easy way to understand Normalized Power is to think about the question:

> _"What constant power would have caused the same physiological stress as this variable effort?"_

**NP** is a **steady-state equivalent power**. It takes into account power variability and the fact that **power spikes** cost much more than you think.

### The Formula

$$NP = \sqrt[4]{\frac{1}{T}\sum P_{30s}(t)^4}$$

where $P_{30s}(t)$ is the power average over 30 seconds.

**Why the 4th power?**
- Raising power to the 4th power heavily weights high-intensity efforts
- The 4th root brings it back to watts
- The 30-second rolling average smooths out noise

**NP gives much more weight to high power spikes.** Short intense intervals matter a lot in this metric, which is not the case with AP!

---

## Practical Example

### Ride A: Steady Effort
- **Duration:** 1 hour
- **Power:** Constant 200W
- **AP:** 200W
- **NP:** 200W
- **NP/AP ratio:** 1.00 (perfectly steady)

### Ride B: Interval Effort
- **Duration:** 1 hour
- **Power:** 30s @ 350W, 30s @ 50W (alternating)
- **AP:** 200W (same as Ride A!)
- **NP:** ≈ 235W
- **NP/AP ratio:** 1.18 (very variable!)

**Same average power, but Ride B costs ~17% more energy!**

This is why you feel destroyed after interval sessions even if "average power" looks moderate.

---

## Comparing Workout Types

It is now much easier to compare different types of workouts:

- **Steady ride** → NP ≈ AP (ratio ~1.00-1.05)
- **Punchy / hilly / draft-heavy ride** → NP > AP (ratio ~1.05-1.15)
- **Intervals** → NP can be _much_ higher than AP (ratio 1.15-1.25+)

**Example comparisons:**

| Workout Type | Duration | AP | NP | Ratio |
|--------------|----------|----|----|-------|
| Flat TT | 60 min | 250W | 252W | 1.01 |
| Hilly ride | 90 min | 210W | 235W | 1.12 |
| VO₂max intervals | 60 min | 215W | 255W | 1.19 |
| Criterium race | 60 min | 220W | 270W | 1.23 |

---

## Variability Index (VI)

**Variability Index** measures how variable your power output was:

$$VI = \frac{NP}{AP}$$

### VI Interpretation

- **VI = 1.00-1.05:** Very steady (ideal for time trial/Ironman bike)
- **VI = 1.05-1.10:** Moderately steady (good for most racing, acceptable for long course)
- **VI = 1.10-1.20:** Variable (hilly ride, group ride, sub-optimal pacing)
- **VI > 1.20:** Very choppy (poor pacing, too many surges, criterium racing)

### Why VI Matters for Racing

**Lower VI = better energy management**

For time trials and triathlon:
- Goal is to maintain steady power
- Every surge above steady state costs you disproportionately
- High VI = wasted energy = slower run (in triathlon)

**Example - Olympic distance bike split:**
- **Athlete A:** AP 240W, NP 245W, VI 1.02 → Smooth pacing, great run
- **Athlete B:** AP 240W, NP 265W, VI 1.10 → Surged too much, struggled on run

Both averaged same power, but Athlete B's variable pacing cost them on the run!

**Training tip:** Practice keeping VI low during race-pace efforts. Aim for VI < 1.05 in time trial position.

---

## How to Use NP in Training

### 1. Compare Workouts of Different Types Fairly

Don't compare AP between interval session and steady ride. Compare NP.

- Interval session: AP 200W, NP 240W
- Steady ride: AP 220W, NP 225W

The steady ride was actually harder (higher NP).

### 2. Evaluate Race Execution

**After a race, check your VI:**
- Low VI (< 1.05) = excellent pacing
- Moderate VI (1.05-1.08) = good pacing
- High VI (> 1.10) = poor pacing, wasted energy

**Goal for triathlon:** Smooth, steady power with VI as close to 1.00 as possible (while accounting for terrain).

### 3. Estimate Workout Intensity

Use NP (not AP) to calculate [[Intensity Factor|IF]]:

$$IF = \frac{NP}{FTP}$$

This gives accurate representation of physiological stress.

### 4. Identify Pacing Issues

**High VI indicates:**
- Too many surges
- Poor pacing strategy
- Reactive riding (responding to others)
- Excessive braking/accelerating

**Example:** Ironman bike with VI > 1.10 = you surged too much and will pay dearly on the run.

---

## NP in Different Scenarios

### Time Trial / Triathlon
- **Goal:** VI as close to 1.00 as possible
- Steady, sustainable power
- Every surge costs you

### Hilly Course
- **Expected:** VI 1.05-1.10 (unavoidable power variation)
- Minimize surges on climbs
- Don't overcook the hills

### Group Ride / Criterium
- **Expected:** VI 1.15-1.25+ (unavoidable with pack dynamics)
- Lots of accelerations and surges
- Why draft-legal racing is so different from TT

### Training Intervals
- **Expected:** VI 1.10-1.20 (depends on interval structure)
- High NP despite lower AP
- This is intentional (building specific fitness)

---

## Relationship to TSS

**NP is used to calculate [[Training Stress Score|TSS]]:**

$$TSS = \frac{(duration \times NP \times IF)}{FTP \times 3600} \times 100$$

**Why NP and not AP?**
- Because NP reflects true physiological cost
- TSS based on AP would underestimate interval workouts
- TSS based on NP accurately represents stress

**Example:**
- 60 min intervals: AP 200W, NP 240W, FTP 250W
- Using AP: TSS = 64 (too low!)
- Using NP: TSS = 92 (accurate!)

---

## Limitations of NP

**NP is excellent but not perfect:**

1. **Designed for cycling only** - doesn't apply to running or swimming
2. **Requires power meter** - can't calculate without power data
3. **Smooths very short efforts** (< 30s) - sprints aren't fully captured
4. **Doesn't account for fatigue state** - fresh vs. fatigued makes same NP feel different
5. **Assumes similar muscle recruitment** - climbing vs. flat uses muscles differently

**Despite limitations, NP is far superior to average power for understanding workout stress.**

---

## Practical Tips

### For Training
- Use NP to compare different workout types
- Track NP trends over time (are you getting stronger?)
- Set interval targets based on NP (not AP)

### For Racing
- Plan target NP for race (based on FTP and distance)
- Monitor VI during race (keep it low!)
- Review VI post-race to evaluate pacing

### For Analysis
- Always look at NP alongside AP
- High NP/AP ratio = variable effort
- Use NP to calculate IF and TSS

---

## Summary

**Key Takeaways:**
1. **Average Power lies** - doesn't account for non-linear physiological cost
2. **Normalized Power** reflects true physiological stress of variable efforts
3. **Variability Index (VI)** shows pacing quality - lower is better for triathlon
4. **Use NP** to calculate IF and TSS, not AP
5. **Practice steady pacing** - aim for VI < 1.05 in race-simulation efforts

**The formula to remember:**
$$NP = \sqrt[4]{\frac{1}{T}\sum P_{30s}(t)^4}$$

**The ratio to watch:**
$$VI = \frac{NP}{AP}$$

**Lower VI = better energy management = faster racing (especially in triathlon).**

Related: [[Intensity Factor]], [[Training Stress Score]], [[FTP Test Protocol]], [[Intensity]]
