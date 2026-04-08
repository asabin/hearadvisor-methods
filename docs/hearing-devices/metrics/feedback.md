# Feedback

## Overview

We considered the degree to which feedback ("squealing") was a problem -- another common complaint from hearing aid users[[16]](../references.md).

There is already some influence of the device's feedback properties in the [Speech Perception Benefit](speech-perception.md) score, because we only considered stable settings (without audible squeals) to be appropriate. However, we additionally tested the quality of the feedback canceller in two challenging cases.

## Challenge Cases

The following provocations were performed while the library scene was played in the background to ensure that the devices were amplifying:

1. **Near-Ear Hand Motion:** Repeatedly moving hands near the device for 10 seconds
2. **Cupping:** Using a hand to cup the ear 10 times in a row

We recorded from the manikin during both cases.

## Blind Listening Test

Trained listeners performed blind listening tests to subjectively rate each recording on a 0--3 scale:

| Score | Description |
|---|---|
| 3 | No feedback |
| 2 | Mild feedback |
| 1 | Moderate feedback |
| 0 | Strong feedback |

### Inter-Rater Agreement

Three expert raters each performed two repetitions:

- **Perfect agreement** (same score): 77% of trials
- **Strong agreement** (all scores within 1 point): 100% of trials

Given this high agreement, we simply averaged the scores across raters for each challenge case.

## Final Metric

The final metric was computed by summing the points across a device's 2 challenge cases and scaling to a 5-point scale.

- **5** = no audible feedback in either challenge case
- **0** = strong feedback in both cases

