---
hide:
  - toc
hide_git_info: true
---

# Changelog

All notable changes to the HearAdvisor methodology are documented here. Each entry includes what changed, which pages were affected, and whether published scores were impacted.

Every page also shows its last-updated date with a link to its full edit history on GitHub. For a line-by-line diff of every change, see the [commit history](https://github.com/asabin/hearadvisor-methods/commits/main).

---

## Hearing Devices

### August 2026 — Speech Perception Benefit adds listener-rated component

The Speech Perception Benefit score is now the average of two components: the existing HASPIv2-derived intelligibility score and a new machine-learning metric trained on 100,000+ blind consumer ratings collected through the Blind Listening Challenge. The intent is a score influenced half by intelligibility research and half by real user preference. The new component is described in full in [Sabin et al. (2026), arXiv:2606.26342](https://arxiv.org/abs/2606.26342).

**Scores affected:** Yes — speech sub-scores (and therefore SoundScores) were recomputed for all hearing devices.

| Area | Description | Pages |
|---|---|---|
| Speech Perception | Published score is now the unweighted mean of the \(\Delta\)HASPIv2 component and a listener-rated ease-of-understanding component predicted by a model trained on Blind Listening Challenge ratings. The listener-rated component is linearly rescaled to match the distribution of the scaled \(\Delta\)HASPIv2 component across all tested devices; both components are bounded below at 1.0 before averaging. | [Speech Perception](hearing-devices/metrics/speech-perception.md) |
| References | Added Sabin, Taddei, & Bailey (2026), describing the listener-rating dataset and predictive model. | [References](hearing-devices/references.md) |
| Results | Refreshed summary statistics following the recompute. The results page now counts the 109 fully evaluated devices listed on hearadvisor.com: average SoundScore 3.8 (was 3.4), with 48 devices (44%) meeting the 4.0 Expert Choice threshold. Because both speech components are bounded below at 1.0, no tested device now grades below C. Earplug metrics are unaffected. | [Devices](hearing-devices/results.md) |

---

### July 2026 — Weight correction, normalization documentation, and score rounding

One scoring-weight correction, one normalization clarification, and one score-rounding clarification.

**Scores affected:** Yes — all hearing device SoundScores were recomputed.

| Area | Description | Pages |
|---|---|---|
| SoundScore | Corrected the component allocation to match the combined survey weights: 0.15 for "Does Not Squeal" and 0.12 for "Own Voice Not Boomy." Per-fit, across-fit, and SoundScore values were recomputed for every device. | [SoundScore](hearing-devices/metrics/soundscore.md) |
| SoundScore | Documented normalization as a catalog-wide offset equal to 5.0 minus the highest raw across-fit score, recalculated when the leading raw score changes, rather than a permanently fixed +1.1. The offset was +1.1 at first publication; the behavior it describes is unchanged. | [SoundScore](hearing-devices/metrics/soundscore.md) |
| SoundGrade | Defined the public SoundScore as the calculated score rounded to one decimal using half-up rounding, with SoundGrade and Expert Choice assigned from that same value. A calculated score of 3.95 therefore displays as 4.0 and receives an A. | [Hearing devices](hearing-devices/metrics/soundscore.md), [Earplugs](earplugs/metrics/soundscore.md) |
| Results | Refreshed summary statistics to the current catalog: 117 hearing devices and 57 earplug conditions across 32 earplugs. Under the corrected weights and shared rounding rule, 45 hearing devices and 20 earplug conditions receive an A. | [Devices](hearing-devices/results.md), [Earplugs](earplugs/results.md) |

---

### May 2023 — Initial Publication

First public documentation of HearAdvisor's hearing device evaluation methodology.

**Scores affected:** N/A (initial publication)

| Area | Description | Pages |
|---|---|---|
| Laboratory | 8-speaker ring, KEMAR 45BA manikin, treated test room | [Lab Setup](hearing-devices/laboratory-setup.md) |
| Recordings | 72 acoustic scenes (ARTE database), custom speech, music streaming | [Recordings](hearing-devices/recordings.md) |
| Device Settings | N3 audiogram, NAL-NL2 targets, Initial and Tuned fit protocols | [Device Settings](hearing-devices/device-settings.md) |
| Speech Perception | HASPIv2-based, quiet/moderate and loud sub-scores | [Speech Perception](hearing-devices/metrics/speech-perception.md) |
| Occlusion | REOIG mapped to subjective ratings, AOC procedure | [Occlusion](hearing-devices/metrics/occlusion.md) |
| Music Streaming | HAAQI_LIN across 5 genres | [Music Streaming](hearing-devices/metrics/music-streaming.md) |
| Feedback | Blind listening test, 2 challenge cases | [Feedback](hearing-devices/metrics/feedback.md) |
| SoundScore | Survey-weighted composite (n=107 consumers, n=95 HCPs) + Expert Choice | [SoundScore](hearing-devices/metrics/soundscore.md) |

---

## Earplugs

### July 2024 — Initial Publication

First public documentation of HearAdvisor's earplug evaluation methodology.

**Scores affected:** N/A (initial publication)

| Area | Description | Pages |
|---|---|---|
| Laboratory | Shared lab with hearing devices (updated room measurements) | [Lab Setup](earplugs/laboratory-setup.md) |
| Recordings | Insertion gain/loss via pink noise at 90 dB LAeq, 10 recordings per device | [Recordings](earplugs/recordings.md) |
| Loudness Reduction | Moore-Glasberg loudness model (ISO 532-2), % reduction in Sones | [Loudness Reduction](earplugs/metrics/loudness-reduction.md) |
| Sound Quality | Tan & Moore spectral distortion metric *D* | [Sound Quality](earplugs/metrics/sound-quality.md) |
| SoundScore | Survey-weighted composite (n=55), letter grades, Expert Choice | [SoundScore](earplugs/metrics/soundscore.md) |
