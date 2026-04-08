# Combining Perceptual Metrics

## Consumer Survey

We conducted an online survey of earplug consumers to determine the relative importance of three dimensions: target loudness reduction, sound quality, and own-voice occlusion.

**55 respondents** were recruited using the comments section of HearingTracker YouTube videos evaluating earplugs. The survey used a constant-sum task in which users assigned relative importances that summed to 100.

**Table 1. Relative importances of perceptual dimensions.** Values reflect average (s.d.) importance rankings across 55 earplug consumers.

| Dimension | Rated Importance |
|---|---|
| The loudness of my environment is quieter when wearing earplugs | 47.8 (19.9) |
| The tone of my environment sounds natural when wearing earplugs | 37.1 (16.8) |
| The sound of my own voice is not boomy when wearing earplugs | 15.1 (11.9) |

Loudness reduction was rated as most important, closely followed by sound quality, and occlusion was a distant third. Due to its low rated importance and measurement complexity, we decided to **omit occlusion** for this generation of evaluation.

## SoundScore Computation

The average rated importances were used as weights to create the combined metric:

| Component | Weight |
|---|---|
| [Loudness Reduction](loudness-reduction.md) | 0.56 |
| [Sound Quality](sound-quality.md) | 0.44 |

\[
\text{SoundScore} = \frac{(w_{\text{loud}} \cdot s_{\text{loud}} + w_{\text{qual}} \cdot s_{\text{qual}})}{\text{max observed}} \times 5
\]

The resulting score is the earplug's SoundScore on a scale from 0 to 5 where 5 is best.

# SoundGrade and Expert Choice Award

## SoundGrade

We further simplify the SoundScore to a letter-grade **SoundGrade**. Letter grades are both easier to understand and more aligned with our intent to focus consumers on large differences between devices rather than small ones.

**Table 2. SoundScore to SoundGrade mapping.**

| SoundScore | SoundGrade |
|---|---|
| 4.0--5.0 | A |
| 3.0--3.9 | B |
| 2.0--2.9 | C |
| 1.0--1.9 | D |
| 0.0--0.9 | F |

For earplugs that allow for multiple levels of attenuation, the device's overall SoundScore and SoundGrade are the **maximum value** as measured across all practical levels.

## Expert Choice Award

Any earplug that achieves a SoundGrade of **"A"** wins the HearAdvisor Expert Choice award. This award recognizes earplugs that achieve a best-in-class balance between loudness reduction and sound quality. 
