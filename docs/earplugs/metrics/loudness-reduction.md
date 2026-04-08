# Perceptual Loudness Reduction

## Overview

We use a standard model of auditory loudness perception to assess how well each earplug reduces perceived loudness. This is distinct from simple attenuation (dB reduction) because human loudness perception is nonlinear and frequency-dependent.

!!! warning "Passive Earplugs Only"
    This model is appropriate because passive earplugs act as linear filters. It may not be appropriate for active earplugs with nonlinear processing.

## Model

Recordings were scaled so that the open ear was equivalent to 100 dB SPL. Each recording was passed through the loudness model from Moore and Glasberg (1997)[[6]](../references.md), adopted as ISO 532-2[[7]](../references.md). Specifically, we used the `acousticLoudness` model in the MATLAB Audio Toolbox.

The model:

1. Divides the spectrum into critical bands
2. Applies a series of transformations including a compressive nonlinearity to mimic the cochlear response
3. Combines contributions from each critical band into an overall loudness level in **Sones**

We focus on Sones because of their linear relationship to perceived loudness -- a doubling of Sones corresponds to a doubling of perceived loudness.

## Computation

The perceptual loudness reduction for each earplug recording is calculated as the percentage reduction in Sones between the open ear and earplug-inserted conditions:

\[
\text{Loudness Reduction} = 100 \times \frac{\text{Open} - \text{Plugged}}{\text{Open}}
\]

The **median** reduction across the 10 earplug insertions is taken as the score for each device.

## Mapping to 0--5 Scale

Scores are normalized by the highest observed reduction (86% reduction in Sones) in our initial set of 24 measured earplug conditions and linearly scaled:

- **0** = no reduction
- **5** = maximum observed reduction

!!! note
    If a future earplug exceeds the normalization anchor, its score would exceed 5.0. In this case, we would update the anchor and re-normalize all scores.
