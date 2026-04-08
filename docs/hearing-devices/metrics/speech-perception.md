# Speech Perception Benefit

## Overview

We quantify the expected improvement in speech intelligibility for each device/fit combination via acoustic measurement. For all recordings, we compute the Hearing Aid Speech Perception Index v2 (HASPIv2[[14]](../references.md)). We chose this metric because it models the impaired auditory system and predicts intelligibility for a wide range of acoustic environments.

## Computation

We compute HASPIv2 using the N3 audiogram ([Table 1](../device-settings.md#hearing-loss)) and RAU-transform[[15]](../references.md) the output. We average across both ears and compute the difference between unaided and aided recordings:

\[
\Delta\text{HASPIv2} = \text{HASPIv2}_{\text{aided}} - \text{HASPIv2}_{\text{unaided}}
\]

Positive values indicate the hearing aid improved speech intelligibility; negative values indicate degradation.

### Quiet/Moderate vs. Loud Environments

We report \(\Delta\)HASPIv2 separately for two environment categories:

| Sub-metric | Environment Criterion |
|---|---|
| Speech Perception Benefit (Quiet/Moderate, 5 background) | Background level < 70 dB SPL |
| Speech Perception Benefit (Loud, 7 background) | Background level > 70 dB SPL |

For each category, we average the \(\Delta\)HASPIv2 score across all qualifying acoustic scenes.

## Mapping to 0--5 Scale

The resulting values are mapped to our 5-point scale via linear scaling.

A ΔHASPIv2 of 0 (no benefit relative to the open ear) maps to 0 on our scale, with increasing benefit scaled linearly up to 5.
