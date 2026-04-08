# Music Streaming Quality

## Overview

Our goal was to estimate subjective sound quality of streamed music via acoustic measurement. We leveraged the Hearing Aid Audio Quality Index (HAAQI[[21]](../references.md)). This metric uses the same model of the impaired auditory system as our speech metrics[[14]](../references.md) and was designed to match subjective music sound quality ratings from individuals with hearing loss[[22]](../references.md).

## Why HAAQI_LIN

HAAQI attempts to capture the influence of both linear and nonlinear distortions. However, we observed that some primary nonlinear distortions (e.g., from streaming audio compression codecs) were not well captured by HAAQI. With this in mind, we report only the portion of the metric that quantifies **linear distortions** (HAAQI\_LIN).

## Computation

For each of the five music segments streamed to the hearing device (see [Music Streaming recording procedure](../recordings.md#music-streaming)):

1. HAAQI\_LIN is computed by comparing the eardrum recording against the original music file
2. Values are averaged across **both ears** and all five recordings

## Mapping to 0--5 Scale

The resulting HAAQI\_LIN values are scaled to our 5-point scale:

- **5** = transparent reproduction (the streamed music is nearly indistinguishable from the original)
- **0** = severe degradation
