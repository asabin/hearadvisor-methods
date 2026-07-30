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

### July 2026 — Weight correction and normalization documentation

Two corrections. Neither changes the methodology as designed; both bring the implementation and the documentation into line with the published survey weights.

**Scores affected:** Yes — all hearing device SoundScores were recomputed.

| Area | Description | Pages |
|---|---|---|
| SoundScore | Corrected an implementation mismatch in which the component weights for "Does Not Squeal" (0.15) and "Own Voice Not Boomy" (0.12) were swapped in the scoring code. Table 2 was and remains correct. Per-fit, across-fit, and SoundScore values were recomputed for every device. | [SoundScore](hearing-devices/metrics/soundscore.md) |
| SoundScore | Documented normalization as a catalog-wide offset equal to 5.0 minus the highest raw across-fit score, recalculated when the leading raw score changes, rather than a permanently fixed +1.1. The offset was +1.1 at first publication; the behavior it describes is unchanged. | [SoundScore](hearing-devices/metrics/soundscore.md) |
| Results | Refreshed summary statistics to the current catalog: 116 hearing devices (was 106) and 57 earplug conditions across 32 earplugs (was 56 across 31). The hearing device SoundGrade distribution reflects the corrected weights and current normalization -- 39 devices now meet the 4.0 Expert Choice threshold, down from 52, and the average SoundScore is 3.4 rather than 3.7. Component metric summaries were refreshed for the expanded hearing-device catalog; all earplug metrics are unchanged. | [Devices](hearing-devices/results.md), [Earplugs](earplugs/results.md) |

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
