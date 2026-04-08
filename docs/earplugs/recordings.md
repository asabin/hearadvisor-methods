# Recordings

## Insertion Gain/Loss Measurement

To measure the earplugs we computed the difference at the manikin's eardrum between the open ear and earplug-inserted conditions (i.e., insertion gain/loss).

**Stimulus:** Uncorrelated pink noise presented from each speaker in the array such that a calibrated measurement mic (MicW i437L) in the ring center read 90 dB LAeq.

## Insertion Protocol

To reduce any contribution of a particular earplug insertion, **five separate recordings** were made for each pair of earplugs. This generated a total of 10 recordings (5 insertions &times; 2 ears). Between recordings:

- Earplugs were removed
- Alternated between ears
- Reinserted

Hearing protection devices with a specific ear designation were only removed and reinserted (not alternated).

Each earplug was inserted in a manner intended to reflect a good seal at a realistic depth. In some cases this meant changing the size of the ear coupling to ensure a tight seal. Small amounts of water-based lubricant are used when there is friction between the earplug and the manikin ear canal. 

The final computed metrics reflect the **median value** across the 10 recordings.

## Diffuse Field Equalization

All recordings were diffuse field equalized using the same standard procedure described in our [hearing device evaluation protocol](../hearing-devices/recordings.md#post-processing).

## Listening Simulations

These recordings were also used to create earplug listening simulations on [HearAdvisor.com](https://hearadvisor.com). To create these simulations:

1. A FIR filter was fit to the measured attenuation (earplug-inserted minus open) of the device, computed at &#8531; octave spacing
2. The filter was applied using a forward/reverse technique that does not add any delay
3. The output was used to create audio files in two versions:
    - **(a) Unprocessed:** No additional processing (demonstrates full earplug effect)
    - **(b) Loudness-matched:** Broadband linear gain applied after filtering to match the loudness of the open ear condition (allows the listener to focus on sound quality irrespective of loudness)
