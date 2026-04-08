# SoundScore

## Overview

For each device, we reduce the full set of five component metrics for two fits down to a single number -- the **SoundScore**. We take a three-step approach:

1. Compute a single **per-fit score** (weighted average of component metrics)
2. Combine those scores **across fits** to make the device's overall score
3. Apply a **normalization factor** to place the final scores into a familiar range

## Step 1: Per-Fit Score (Component Weights)

The per-fit score is a weighted average across all 5 component metrics. The weights were derived from a custom survey of hearing aid consumers (n = 107) and hearing care professionals (n = 95). Each participant ranked the relative importance of our 5 metrics on a 0 to 4 scale (higher is better).

*Table 2. Rated importance of each component dimension.* Group average rated importance from 0 (lowest) to 4 (highest). Bottom row: two-group average, normalized to sum to 1.

| | Speech Benefit (Quiet/Mod) | Speech Benefit (Noisy) | Own Voice Not Boomy | Does Not Squeal | Streaming Music Quality |
|---|---|---|---|---|---|
| **Consumers** Avg Rank | 3.2 | 3.1 | 1.1 | 1.3 | 1.3 |
| **HCPs** Avg Rank | 3.5 | 2.7 | 1.4 | 1.7 | 0.7 |
| **Combined** Normalized | **0.34** | **0.29** | **0.12** | **0.15** | **0.10** |

The ranks show reasonably nice agreement across groups, indicating that this weighting is largely replicable. We combined the two groups to create an overall average importance rating (bottom row).

The per-fit score is:

\[
\text{Per-Fit Score} = \sum_{i} w_i \cdot s_i
\]

## Step 2: Across-Fit Score (Initial vs. Tuned Weights)

The across-fit score is a weighted average of the Initial Fit and Tuned Fit per-fit scores. These weights were derived from a separate survey.

257 hearing aid consumers were asked to rate: *"How Important Is It That Your Hearing Aids Sound Good With Minimal Effort?"* on a 5-point scale. We intended this question to be a proxy for the importance of the quality of the initial fit.

*Table 3.* Percentage of hearing aid consumers responding to: "How Important Is It That Your Hearing Aids Sound Good With Minimal Effort?"

| Not-At-All Important (0.0) | Slightly Important (0.25) | Moderately Important (0.5) | Very Important (0.75) | Extremely Important (1.0) |
|---|---|---|---|---|
| 1% | 4% | 15% | 37% | 43% |

When responses were normalized to a 0--1 range, the group average is **0.77**. Therefore:

| Fit Condition | Weight |
|---|---|
| Initial Fit | 0.77 |
| Tuned Fit | 0.23 |

!!! note
    Perhaps coincidentally, this proportion is similar to the estimated proportion of hearing aids fit with real ear measures[[23]](../references.md)[[24]](../references.md)[[25]](../references.md).

## Step 3: Normalization

The observed overall scores had a maximum of 3.9 and an average of 2.3. These values could be misleading to users because in other products, the star rating of the best performing devices is usually very close to 5.0 (a score of 3.9 might be seen as mediocre).

With this in mind, we added **1.1** to all devices' scores -- placing the top scorer at 5.0. The resulting value is the device's **SoundScore**.

!!! note
    This normalization is a presentation choice to align with consumer expectations for star-rating scales, not a scientific transformation. The underlying weighted scores are preserved in the data.

# Expert Choice Award

We curate a list of devices with SoundScores near the top of the observed range. We give an **Expert Choice** award to any device whose overall score is within 1.0 of the maximum SoundScore (i.e., SoundScore \(\geq\) 4.0).
