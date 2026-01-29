
**NP** is a metric that solves the problem inherent to Average Power (**AP**). 
**AP** is nothing more than $$AP = \frac{1}{T}\sum P(t)$$
Globally it's just the average power you generated during your workout. But let's take a look at some workout examples:
- Ride A: steady 200W for one hour
- Ride B: 30s at 350W, 30s at 50W, for one hour
$\rightarrow$ Same average power for a **completely** different fatigue.

Physiological cost increases **non-linearly** with intensity. Here's the problem with **AP**: it doesn't take into account the non-linearity of body response against power.

An easy way to understand Normalized Power is to think about the question:
> _“What constant power would have caused the same physiological stress as this variable effort?”_

**NP** is a **steady-state equivalent power**. It takes into account power variability and the fact that **power spikes** cost much more than you think. Below is the formula to compute this metric:
$$NP = \sqrt[4]{\frac{1}{T}\sum P_{30s}(t)^4}$$
where $P_{30s}(t)$ is the power average over 30 seconds.

NP gives a much more important weight to high power spikes. Short intense intervals matter a lot in this metric which is not the case with AP!

It is now much more easy to compare different types of workouts:
- **Steady ride** → NP ≈ AP
- **Punchy / hilly / draft-heavy ride** → NP > AP
- **Intervals** → NP can be _much_ higher than AP according the intensity and the duration of those intervals
