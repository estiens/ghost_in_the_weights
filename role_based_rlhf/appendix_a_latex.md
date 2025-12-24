# Appendix A: The Bayesian Analysis (LaTeX Version)

For readers who want to verify the mathematical claims, here is the complete model. This version uses LaTeX notation for platforms that support math rendering (GitHub, Obsidian, etc.).

## Variable Definitions

**Harm side:**
- $p_d = P(\text{Police Dispatch} \mid \text{988 Call}) = 3.6\%$ average (range 0–17.3% by state)
- $p_s = P(\text{Shooting} \mid \text{Police Dispatch})$ = **Unknown. Not measured.**
- $p_f = P(\text{Fatality} \mid \text{Shooting}) = 65.2\%$ for wellness checks

**Benefit side:**
- $q = P(\text{Imminent Suicide} \mid \text{Incremental Caller})$ = base rate among banner-driven callers
- $r = P(\text{Suicide Averted} \mid \text{Call})$ = causal effectiveness of the call

## The Break-Even Equation

The intervention is justified only if expected benefit exceeds expected harm:

$$q \times r > p_d \times p_s \times p_f$$

Plugging in known values ($p_d = 0.036$, $p_f = 0.652$):

$$q \times r > 0.0235 \times p_s$$

## Sensitivity Analysis

| Assumed $p_s$ | Required lives saved per 1M calls to break even |
|-------------|------------------------------------------------|
| 1 in 100,000 ($p_s = 10^{-5}$) | 0.24 |
| 1 in 10,000 ($p_s = 10^{-4}$) | 2.35 |
| 1 in 5,000 ($p_s = 2 \times 10^{-4}$) | 4.70 |
| 1 in 1,000 ($p_s = 10^{-3}$) | 23.5 |

*Note: These figures assume the mortality benefit ($q \times r$) is achievable. RCT evidence for any of these effect sizes: zero.*

## The Full Harm Model

Lethal force is only one term. The complete expected value equation:

$$\text{EV}_{\text{net}} = (q \times r) - (p_d \times p_s \times p_f) - H_{\text{hold}} - H_{\text{chill}} - H_{\text{iatr}} - H_{\text{displace}}$$

Where:
- $H_{\text{hold}}$ = harm from involuntary psychiatric holds
- $H_{\text{chill}}$ = harm from chilling effects on future help-seeking
- $H_{\text{iatr}}$ = harm from iatrogenic (treatment-caused) effects
- $H_{\text{displace}}$ = harm from displacing users from better resources

Even if $(p_d \times p_s \times p_f)$ is small, the other terms compound. The burden of proof requires demonstrating that $(q \times r)$ exceeds the sum of all harm channels.

## What Would Have to Be True

For the intervention to be net-positive:

1. $p_s$ must be extremely low ($< 1$ in 10,000 dispatches escalate to shootings)
2. $q \times r$ must be non-trivial (the banner must cause calls that actually prevent deaths)
3. $H_{\text{chill}}, H_{\text{hold}}, H_{\text{iatr}}, H_{\text{displace}}$ must be bounded and smaller than benefit

Current evidence:
- $p_s$: Unknown (not measured)
- $q \times r$: Zero RCT evidence
- $H_{\text{chill}}$: 88% of trans respondents report concern; two-thirds of Black Americans distrust police
- $H_{\text{hold}}$: Documented employment/housing consequences
- $H_{\text{iatr}}$: 65% of high-urgency callers lost to follow-up
- $H_{\text{displace}}$: Trans Lifeline explicitly advises against 988

**The burden of proof has not been met.**
